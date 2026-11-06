# ZoneRanks

Server ranks and permission management with custom titles, a title catalog and client editors.

Rangos y permisos del servidor con títulos propios, catálogo de títulos y editores de cliente.

## Current release / Entrega actual — 2026-11-06

Minecraft **1.20.1**, Forge **47.x** (47.4.x for this release set), Java **17**. File availability follows CurseForge approval. / Disponibilidad de archivos según aprobación de CurseForge.

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 3.3.13 |
| Client / Cliente — retained / conservado | 3.3.6 |

**Protocol / Protocolo:** Ranks 5 / Titles 1.

[Downloads / Descargas](https://www.curseforge.com/projects/1738043/files) · [Release guide / Guía de novedades](RELEASE-2026-11-06.md) · [Configuration / Configuración](CONFIGURATION.md)

## English — Requirements and quick start

Server: ZoneCore 2.1.0+. ZoneCrates 2.0.0+ is optional for the wallet used by title purchases. Keep the existing client 3.3.6; this update does not require a new client JAR.

Administrators can inspect ranks with `/rangos lista`, discover installed permission nodes with `/rangos permisos disponibles`, and reload rank edits with `/zoneranks reload`. LevelUp benefits are configured in LevelUp, not in the rank title text.

### What changed

- Server 3.3.13 exposes the current rank ID and rank catalog through a public query API retained in the protected build.
- ZoneLevelUp r55 can use real assigned ranks for automatic benefits; decorated titles do not replace stable rank IDs.
- Keeps the previous editor, permission catalog, explicit USUARIO inheritance and current network protocols.

## Español — Requisitos e inicio

Servidor: ZoneCore 2.1.0+. ZoneCrates 2.0.0+ es opcional para la cartera de compras de títulos. Conserva el cliente 3.3.6 existente; esta actualización no requiere un JAR cliente nuevo.

Los administradores consultan rangos con `/rangos lista`, descubren nodos con `/rangos permisos disponibles` y recargan con `/zoneranks reload`. Los bonos de LevelUp se configuran en LevelUp, no en el texto decorativo del rango.

### Novedades

- Servidor 3.3.13 expone la ID de rango actual y el catálogo mediante una API pública conservada en la compilación protegida.
- ZoneLevelUp r55 puede usar rangos reales asignados para beneficios automáticos; los títulos decorados no sustituyen IDs estables.
- Conserva editor, catálogo de permisos, herencia explícita de USUARIO y protocolos actuales.

## Updating / Actualizar

Stop the affected instance, back up world/configuration, replace only the previous same-mod/same-side JAR and retain player data. Never install the dedicated and client JARs of one mod together. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado conservando datos. Nunca instales juntos los JAR dedicado y cliente del mismo mod.

## Validation scope / Alcance de verificación

The r55 delivery checks the rank API, real rank IDs and assignments with LevelUp, and inspects preservation of the API in the protected build. It does not certify the full production modpack or a new visual client session.

La entrega r55 comprueba API, IDs y asignaciones con LevelUp y su conservación en el JAR protegido. No certifica el modpack completo de producción ni una sesión gráfica nueva.

## Rights / Derechos

Original ZONE code and assets © Elgochogms; existing licenses and third-party notices remain applicable. This repository provides public documentation. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Este repositorio contiene documentación pública.
