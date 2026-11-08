# ZoneRanks — Configuration / Configuración (2026-11-08)

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 3.3.14 |
| Client / Cliente — retained / conservado | 3.3.6 |

## Commercial ranks / Rangos comerciales

Server-console commands / Comandos de consola:

```text
rangos tiendaversion
rangos compraruuid <player_uuid> <rank> mensual <order_line_uuid>
rangos compraruuid <player_uuid> <rank> permanente <order_line_uuid>
```

Supported commercial IDs: `dios`, `vampirico`, `cazador`, `almirante`, `domador`, `escolta`. These definitions must already exist. Delivery requires console permission level 4; players and command blocks cannot issue purchase receipts. / Los seis IDs deben existir; la entrega requiere consola nivel 4. Jugadores y bloques de comandos no emiten recibos.

The order-line UUID must be real, unique and retained across retries. The store must resolve it before sending commands; the current bridge substitutes only `{uuid}` and `{player}`. Send only after confirmed payment. Reusing a receipt with different player/rank/period fails. This command grants no coins, kits or items, and its idempotency does not cover other commands in a product bundle. / El recibo debe ser UUID real y conservarse al reintentar; la tienda lo resuelve antes de enviar. El puente sustituye solo `{uuid}` y `{player}`. Ejecuta tras pago confirmado. No entrega monedas/kits/objetos ni hace idempotentes otros comandos del paquete.

## Periods and persistence / Periodos y persistencia

- A month is a calendar month in `America/New_York`, including DST and end-of-month adjustment. Renew before expiry to extend from the existing deadline; renew after expiry to start from the new grant. / Mes calendario con cambio horario y ajuste de fin de mes; renovar antes extiende desde vencimiento, después desde nueva entrega.
- Commercial precedence: DIOS → VAMPIRICO → CAZADOR → ALMIRANTE → DOMADOR → ESCOLTA. Periods for different ranks run simultaneously. / Esa es la prioridad; los periodos de distintos rangos corren simultáneamente.
- A lower monthly rank never downgrades a higher permanent rank. Expiry falls back to the next valid monthly or retained permanent/base. / Un mensual inferior no rebaja permanente superior; al vencer se usa siguiente vigente o permanente/base.
- Permanent purchases retain the highest permanent and replace equal/lower temporary grants. Higher temporary grants keep their remaining time. / Permanente conserva el mayor y sustituye temporales iguales/inferiores; uno temporal superior mantiene tiempo.
- A player whose base is empty, one of the six commercial ranks, `usuario`, `booster` or `donador` can receive a supported commercial purchase. Other special/admin/custom base ranks reject the purchase without changing the assignment. / Bases vacías, uno de los seis rangos comerciales, `usuario`, `booster` o `donador` admiten una compra comercial compatible. Solo las demás bases especiales, administrativas o personalizadas la rechazan sin modificar asignación.

Back up `<world>/data/zoneranks.dat` and `config/ZONEMODS/zoneranks/`. Periods/receipts persist in world data; `jugadores/asignaciones.toml` retains permanent/base assignments rather than exporting temporary ranks as permanent. Permission checks immediately reject expired periods; presentation/commands refresh through an expiry queue once per second. No website request is needed at expiry. / Respalda mundo/configuración; periodos/recibos en datos del mundo y TOML mantiene base permanente. Permisos caducan por fecha; presentación se actualiza cada segundo, sin consultar web.

Administrative `asignar`, `asignaruuid`, `retiraruuid` or changed TOML assignment cancels the player's temporary periods. Reloading unchanged assignments preserves them; receipt history remains. A failed save or pending editor changes roll back the attempted grant in memory. / Esas asignaciones administrativas cancelan temporales, mientras recarga sin cambios los conserva. Historial permanece; fallo de guardado o edición pendiente revierte el intento.

Do not downgrade after using monthly grants: older versions do not understand the ledger. Keep products disabled until the installed server version and a controlled grant have been checked. / No vuelvas a versión anterior tras usar mensuales: no entiende el registro. Mantén productos desactivados hasta verificar versión instalada y entrega controlada.


## Files / Archivos

Server-owned files under `config/ZONEMODS/zoneranks/` / Archivos del servidor:

| Path / Ruta | Purpose / Uso |
|---|---|
| `rangos/creados.toml` | Rank IDs and display fields / IDs y apariencia de rangos |
| `permisos/rangos.toml` | Direct nodes in `[permisos.ID].nodos` / Nodos directos |
| `jugadores/asignaciones.toml` | Private UUID-to-rank assignments / Asignaciones privadas UUID-rango |
| `rangos/predeterminado.toml` | `activo` and existing `rango` for first assignment / Rango inicial existente |
| `rangos/orden.toml` | Display order only / Orden visual; no concede permisos |
| `titulos/catalogo.toml` | Title name, icon, description, purchase availability and price / Catálogo de títulos |

`config/zoneranks-common.toml` controls display color/name tags/chat. Preserve `<mundo>/data/zoneranks.dat` with the world. / El TOML común controla color, etiquetas y chat; conserva los datos del mundo.

`[rangos.ID]` creates the rank definition; adding only `[permisos.ID]` does not create one. Edit while stopped or apply valid rank edits with `/zoneranks reload`; titles use `/titulo reload`. Invalid TOML retains the active set. / La definición de rango se crea en `creados.toml`; una tabla de permisos sola no lo crea. Usa las recargas indicadas; un TOML inválido conserva los valores activos.

## Permission tools / Herramientas

- `/rangos permisos disponibles [pagina]`: published Forge/Core nodes / nodos publicados.
- `/rangos permisos buscar <texto> [pagina]`: filter the catalog / filtrar catálogo.
- `/rangos permiso listar <rango> [pagina]`: direct nodes / permisos directos.
- `/rangos permiso comprobar <jugador> <nodo>`: inspect an online player / comprobar jugador conectado.
- `/rangos permiso comparar <origen> <destino> [pagina]`: inspect missing direct nodes / comparar nodos directos.
- `/rangos permiso combinar <origen> <destino>`: add missing nodes without removing destination entries / añadir faltantes sin borrar destino.
- `/rangos clonar <origen> <nuevo>`: copy presentation and direct nodes, not player assignments / copiar aspecto y nodos, no asignaciones.

The optional `zoneranks.commands.usuario` node inherits the current USUARIO permission set without copying it. Nothing enables it automatically. Nodes not published by a mod cannot automatically appear in discovery. / El nodo opcional hereda USUARIO sin copiarlo y no se activa automáticamente. Los nodos no publicados por un mod no se pueden descubrir solos.

[Current release / Entrega actual](RELEASE-2026-11-08.md) · [README](README.md).
