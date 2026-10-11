# ZG ZoneRanks — release and compatibility

## English

- Pair on this one CurseForge project: server 3.3.9 + client 3.3.3. Rank network protocol 4 and title protocol 1 unchanged. Minecraft 1.20.1, Forge 47.x, Java 17.
- Server requires ZG ZoneCore 2.1.0+; ZoneCrates 2.0.0+ is optional but required for Gochocoin title purchases. Client carries visual interface, not rank authority.
- Changes from server 3.3.8/client 3.3.2: new release metadata/licensing and protected matching binaries. Rank rules, commands and network protocols unchanged. Older MIT licenses remain effective for older versions.
- Both Gradle builds passed. An isolated unprotected server fixture with final Core 2.1.3, Crates 2.0.6 and ScoreBoard 3.4.1 passed 246 assertions, then 9 persistence assertions after restart. The protected server started with those final mods and protected Protes 2.9.1, answered /zoneranks reload, /rangos permisos disponibles and /titulo reload, then shut down cleanly.
- The client GUI, two player handshake, actual title purchase, complete modpack and production hosting were not tested with these exact protected JARs.
- Obfuscation preserves the public ZoneRanks.has method used by optional mod integration. Public API and bytecode can still be inspected.

## Español

- Pareja de este único proyecto CurseForge: servidor 3.3.9 + cliente 3.3.3. Protocolos de rangos 4 y títulos 1 sin cambios. Minecraft 1.20.1, Forge 47.x, Java 17.
- Servidor requiere ZG ZoneCore 2.1.0+; ZoneCrates 2.0.0+ es opcional pero necesario para comprar títulos con Gochocoins. El cliente muestra la interfaz, no decide permisos.
- Frente a servidor 3.3.8/cliente 3.3.2: metadatos/licencia de nueva entrega y JAR protegidos compatibles. Reglas, comandos y protocolos sin cambios. Los permisos MIT anteriores siguen vigentes para aquellas versiones.
- Compilaron ambos módulos. El fixture aislado del servidor sin proteger con Core 2.1.3, Crates 2.0.6 y ScoreBoard 3.4.1 finales pasó 246 comprobaciones y otras 9 de persistencia tras reiniciar. El servidor protegido arrancó con esos mods y Protes 2.9.1 protegido, respondió /zoneranks reload, /rangos permisos disponibles y /titulo reload, y cerró limpio.
- Faltan interfaz gráfica del cliente, conexión real de dos jugadores, compra real de títulos, modpack completo y hosting con estos JAR exactos.
- La ofuscación conserva el método público ZoneRanks.has usado por integraciones opcionales. La API pública y el bytecode siguen siendo inspeccionables.

