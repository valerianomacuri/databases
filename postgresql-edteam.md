# Clientes de postgres

> AUTHOR: Alexys Lozada

1. Para conectarse al cliente utilizaremos `psql`. Ejemplo:

```console
psql -U postgres -d postgres -h 127.0.0.1 -p 5432
```

Se lee:

```console
psql -U user -d database -h host -p port
```

2. `\?` permite listar todos los metacomandos del cliente psql.
3. `\l` las bases de datos que están en ese servidor.
4. `\c` permite conectarse a una base de datos.
5. `\c` lista las relaciones (tablas, secuencias, indices, etc) de la base de
   datos en la que estamos ubicados actualmente.

6. `\dg` muestra los roles y sus atributos.

7. `\dt` lista solo las tablas de la base de datos en la que estamos ubicados
   actualmente. Si quieres más información puedes usar un `+` así:
   `\d+ [NOMBRE-TABLA]`.

8. `\d [NOMBRE-TABLA]` muestra el detalle de la tabla específica.

9. `\h` Nos da ayuda acerca de comandos SQL. Es como una documentación del
   lenguaje SQL. Ejemplo: `\h INSERT` <- Muestra la ayuda del comando INSERT.

10. `\i` Permite ejecutar comandos de un archivo SQL. Ejemplo restaurar un
    backup: `\i /ruta/del/backup/archivo.sql` <- Si el archivo `archivo.sql` es
    un backup, lo restaurará.

11. `\! [COMANDO DEL SHELL]` Ejecuta un comando del shell con el que está
    trabajando. Ejemplo: `\! ls` <- Lista el directorio donde se está ubicado
    actualmente.
