# ZoneRanks — Configuration / Configuración (2026-11-06)

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 3.3.13 |
| Client / Cliente — retained / conservado | 3.3.6 |

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

[Current release / Entrega actual](RELEASE-2026-11-06.md) · [README](README.md).
