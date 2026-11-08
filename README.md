# ZoneRanks

Server ranks and permissions, custom titles, and client administration screens. This release adds calendar-month and permanent commercial rank grants with persistent receipts.

Rangos y permisos, títulos propios e interfaces administrativas. Esta entrega añade rangos comerciales por mes calendario o permanentes con recibos persistentes.

## Current release / Entrega actual — 2026-11-08

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 3.3.14 |
| Client / Cliente — retained / conservado | 3.3.6 |

**Protocol / Protocolo:** Ranks 5 / Titles 1.

[Downloads / Descargas](https://www.curseforge.com/projects/1738043/files) · [Release / Novedades](RELEASE-2026-11-08.md) · [Configuration / Configuración](CONFIGURATION.md)

## English

Minecraft 1.20.1, Forge 47.x, Java 17. Server requires ZoneCore 2.1.0+; ZoneCrates 2.0.0+ is optional for title purchases. Only the server changes: keep client 3.3.6.

Server 3.3.14 adds console-only monthly/permanent rank grants with unique order-line receipts. Replaying the same receipt does not add another month. Renewals use calendar months in America/New_York; different ranks keep independent expiry times and do not downgrade a higher permanent rank. `/rango vigencia` shows the player’s active and permanent/base rank and remaining periods. Expiry revokes only flight marked as granted by ZoneRanks. Preserve world data and receipts; do not downgrade after selling months without reconciling a coherent backup. Keep client 3.3.6, Ranks 5 / Titles 1; Core is required only on the server. No automatic recurring billing is added.

Players use `/rango vigencia`. Administrators verify `rangos tiendaversion` from the console before enabling monthly products. The existing rank editors and permissions remain available.

## Español

Minecraft 1.20.1, Forge 47.x, Java 17. Servidor requiere ZoneCore 2.1.0+; ZoneCrates 2.0.0+ es opcional para compras de títulos. Solo cambia servidor: conserva cliente 3.3.6.

Servidor 3.3.14 añade entregas mensuales/permanentes solo por consola, con recibos únicos por línea de pedido. Reintentar el mismo no suma otro mes. Renovaciones por mes calendario en America/New_York; rangos distintos conservan vencimientos independientes sin rebajar un permanente superior. `/rango vigencia` muestra rango activo, permanente/base y periodos. Al vencer se retira solo vuelo concedido y marcado por ZoneRanks. Conserva datos y recibos; no vuelvas de versión tras vender meses sin reconciliar un respaldo. Mantén cliente 3.3.6, Ranks 5 / Titles 1; Core solo es obligatorio en servidor. No añade cobros recurrentes automáticos.

Los jugadores usan `/rango vigencia`. Administración verifica `rangos tiendaversion` en consola antes de habilitar productos mensuales. Se conservan editores y permisos anteriores.

## Updating / Actualizar

Stop the affected instance, back up world/configuration and replace only the previous same-mod/same-side JAR. Keep one JAR per mod per instance and preserve player data. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado. Conserva un JAR por mod e instancia y los datos de jugador.

## Validation scope / Alcance de verificación

The delivery includes isolated receipt, renewal, expiry, persistence and protected-server checks. It does not establish real production purchases or full-modpack performance.

La entrega incluye pruebas aisladas de recibos, renovación, vencimiento, persistencia y servidor protegido. No acredita compras reales en producción ni rendimiento del modpack completo.

## Rights / Derechos

Original ZONE code/assets © Elgochogms; existing third-party licenses and notices remain applicable. Public documentation repository. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Repositorio de documentación pública.


## Previous documentation / Documentación anterior

[2026-11-06 release / Entrega 2026-11-06](RELEASE-2026-11-06.md). Version examples in historical releases remain historical. / Los ejemplos de versiones de entregas anteriores son históricos.
