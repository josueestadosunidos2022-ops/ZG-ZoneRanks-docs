# ZoneRanks

## Current builds / Versiones actuales — 2026-11-04

| Side / Lado | Version / Versión | File / Archivo |
|---|---|---|
| server | 3.3.12 | [zoneranks-server-3.3.12-protected.jar](https://www.curseforge.com/projects/1738043/files/9438567) |
| client | 3.3.6 | [zoneranks-client-3.3.6-protected.jar](https://www.curseforge.com/projects/1738043/files/9438605) |

Minecraft 1.20.1 / Forge 47.4.x / Java 17. Protected public Beta builds; availability depends on each file approval. / Betas públicas protegidas; disponibilidad según aprobación de cada archivo.

## English — What is new

Reworked rank/title editors with blue/purple/cyan styling, server-paged direct permissions, deletion confirmation, retained drafts and bitmap icons. Client 3.3.6 expands the logical editor to 450px and separates labels/fields/navigation to address clipping. Use SERVER 3.3.12 with CLIENT 3.3.6; RankNetwork 5 / TitleNetwork 1. The server file is unchanged from the local 3.3.12 delivery.

## Español — Novedades

Editores de rangos/títulos azul/morado/celeste, permisos directos paginados desde servidor, confirmación de borrado, borradores e iconos bitmap conservados. Cliente 3.3.6 amplía editor lógico a 450px y separa etiquetas/campos/navegación. Pareja SERVIDOR 3.3.12 + CLIENTE 3.3.6; RankNetwork 5 / TitleNetwork 1. Servidor idéntico a entrega local 3.3.12.

## Installation / Instalación

Use the exact server/client pair in the table. Do not mix earlier network revisions. / Usa la pareja exacta de la tabla; no mezcles revisiones de red anteriores.

Stop the affected instance, back up the world/config, remove only the previous same-mod/same-side JAR, and install the table version. Preserve character data, wallets and TOML. Do not put server-only dependencies on clients. / Detén la instancia, respalda mundo/config, sustituye solo el JAR anterior del mismo mod y lado, y conserva personajes, cartera y TOML. No instales dependencias exclusivas de servidor en el cliente.

## Dependencies / Dependencias

**server**: `zonecore` [2.1.0,) (required/obligatorio; SERVER); `zonecrates` [2.0.0,) (optional/opcional; SERVER).

**client**: No additional Zone requirement / Sin requisito Zone adicional.

[Full changes and usage / Novedades y uso](RELEASE-2026-11-04.md) · [Configuration / Configuración](CONFIGURATION.md) · [Historical releases / Entregas históricas](RELEASES.md).

## Validation / Verificación

Original release checks and isolated startup/command registration of the protected set were reviewed. Shared schemas: Essentials 35, Guardian 13 and Misions 4 classes, with no mapping differences. This does not certify a new graphical client session, two-player gameplay, full third-party modpack, hosting deployment or FPS/TPS. / Revisadas las verificaciones de entrega y el arranque/registro de comandos del conjunto protegido. Esquemas compartidos sin diferencias de mapeo: Essentials 35, Guardian 13 y Misions 4 clases. No certifica una nueva sesión gráfica, dos jugadores, modpack completo, hosting ni FPS/TPS.

## Ownership / Titularidad

Original ZONE code and visual assets © Elgochogms. Public documentation only: no mod sources, private obfuscation maps, credentials or production player data. Existing rights of earlier distributions are preserved.
