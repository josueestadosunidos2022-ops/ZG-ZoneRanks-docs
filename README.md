# ZG ZoneRanks

## English

Server controlled player ranks, permissions, titles, name tags and chat styling for Minecraft 1.20.1, Forge 47.x and Java 17. The client shows the custom rank/title interfaces and visual assets.

### Install the pair

Install zoneranks-server-3.3.9-protected.jar and ZG ZoneCore 2.1.0+ on the dedicated server. Install zoneranks-client-3.3.3-protected.jar on each client. Both JARs are on this **one CurseForge project**. The rank and title channels remain protocols 4 and 1. ZoneCrates 2.0.0+ is optional on the server, but needed for title purchases with Gochocoins. Keep the server and client versions stated here together.

### Use

Administrators can assign ranks, edit prefixes/colors/icons, grant permission nodes and manage titles through commands or the custom editor. /rangos permisos disponibles [page] lists permission nodes published by loaded Forge and ZoneCore modules; /rangos permisos buscar <text> [page] filters them. Mods that do not publish nodes cannot be enumerated, but their node strings can be entered manually. /zoneranks reload applies edits to rank TOML; /titulo reload applies title catalog edits. The optional marker zoneranks.commands.usuario grants a rank the current USUARIO permission set; it is **not** granted to other ranks automatically.

Read [TOML paths and fields](CONFIGURATION.md) and [release compatibility](RELEASES.md). Back up the world and config/ZONEMODS/zoneranks before updating. Server rank and player data are persistent; do not publish assignments with real player UUIDs.

## Español

Rangos, permisos, títulos, etiquetas de nombre y estilo de chat controlados por el servidor para Minecraft 1.20.1, Forge 47.x y Java 17. El cliente muestra las interfaces personalizadas y recursos visuales.

### Instala la pareja

Instala zoneranks-server-3.3.9-protected.jar y ZG ZoneCore 2.1.0+ en el servidor dedicado. Instala zoneranks-client-3.3.3-protected.jar en cada cliente. Ambos JAR están en **un único proyecto CurseForge**. Los canales de rangos y títulos conservan protocolos 4 y 1. ZoneCrates 2.0.0+ es opcional en servidor, pero necesario para comprar títulos con Gochocoins. Usa junta la pareja indicada.

### Uso

El administrador asigna rangos, edita prefijos, colores e iconos, concede nodos de permisos y gestiona títulos mediante comandos o editor propio. /rangos permisos disponibles [pagina] enumera los nodos publicados por Forge y ZoneCore de mods cargados; /rangos permisos buscar <texto> [pagina] los filtra. Los nodos no publicados no pueden enumerarse, pero pueden escribirse a mano. /zoneranks reload aplica cambios del TOML de rangos; /titulo reload aplica el catálogo de títulos. El marcador opcional zoneranks.commands.usuario concede a un rango los permisos actuales de USUARIO; **no** se asigna automáticamente a otros rangos.

Consulta [rutas y claves TOML](CONFIGURATION.md) y [compatibilidad](RELEASES.md). Respalda el mundo y config/ZONEMODS/zoneranks antes de actualizar. Los datos de rangos y jugadores persisten; no publiques asignaciones con UUID reales.

## Ownership / Titularidad

Copyright © 2026 Elgochogms. New server 3.3.9 and client 3.3.3 binaries are All Rights Reserved. Earlier releases retain their original license rights. This repository contains documentation and the original ZG avatar only; no source, private maps or player data. Obfuscation cannot make Java bytecode impossible to decompile.

