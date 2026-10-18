# ZoneRanks — TOML configuration reference

This guide describes **server 3.3.9 / client 3.3.3**. The Forge keys below show source defaults. The dynamic TOML files are server owned under config/ZONEMODS/zoneranks. / Esta guía corresponde a **servidor 3.3.9 / cliente 3.3.3**. Las claves Forge siguientes muestran valores iniciales; los archivos TOML dinámicos pertenecen al servidor en config/ZONEMODS/zoneranks.

## Configuration files

- `config/zoneranks-common.toml`: display.defaultColor, display.nameTagEnabled and display.chatEnabled / apariencia, etiquetas y chat.
- `config/ZONEMODS/zoneranks/rangos/creados.toml`: rank IDs and title, prefix, color, gradient, bold and icon fields / rangos y aspecto.
- `config/ZONEMODS/zoneranks/permisos/rangos.toml`: [permisos.ID].nodos lists granted permission strings / nodos concedidos.
- `config/ZONEMODS/zoneranks/jugadores/asignaciones.toml`: player UUID to rank mappings; private data / asignaciones privadas.
- `config/ZONEMODS/zoneranks/rangos/predeterminado.toml`: activo=true/false and existing rango ID for automatic first rank / rango inicial.
- `config/ZONEMODS/zoneranks/rangos/orden.toml`: ordered list for display only; does not grant permissions / orden solo visual.
- `config/ZONEMODS/zoneranks/titulos/catalogo.toml`: [titulos.ID] with nombre, icono, descripcion, comprable, precio and persistent registro / catálogo de títulos.
- `world/data/zoneranks.dat`: persistent world data; back up before migration / datos persistentes del mundo.

## Detected keys / Claves detectadas

| Key / Clave | Declared default | Source class |
|---|---|---|
| `chatEnabled` | `true` | `ZoneRanksConfig.java` |
| `defaultColor` | `"white"` | `ZoneRanksConfig.java` |
| `nameTagEnabled` | `true` | `ZoneRanksConfig.java` |

## Editing / Edición

In creados.toml the [rangos.ID] table defines whether a rank exists. A [permisos.ID] table cannot create a rank. Player assignment uses UUIDs; never publish a production copy. Edit the rank files while the server is stopped or use /zoneranks reload after valid edits. The title catalog uses /titulo reload. Invalid TOML is rejected without replacing the active set. / En creados.toml, [rangos.ID] determina si existe un rango; [permisos.ID] no puede crearlo. Las asignaciones contienen UUID; no publiques el archivo real. Edita con el servidor detenido o ejecuta /zoneranks reload tras cambios válidos. El catálogo de títulos usa /titulo reload. Un TOML inválido no reemplaza la configuración activa.

Permission discovery lists published Forge and ZoneCore nodes from installed mods in pages of 12. Use /rangos permisos disponibles [pagina] or /rangos permisos buscar <texto> [pagina]. Manually enter undocumented nodes only after verifying the owning mod. The marker zoneranks.commands.usuario is optional and inherits the current USUARIO node set, without copying it to other ranks. / La búsqueda enumera nodos publicados por los mods instalados de Forge y ZoneCore en páginas de 12. Los nodos no publicados se escriben a mano tras comprobarlos. El marcador opcional zoneranks.commands.usuario hereda el conjunto actual de USUARIO sin copiarlo a otros rangos.

