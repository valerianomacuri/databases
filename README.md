# PostgreSQL

Cumple con el estandar ACID:

- Atomicidad: Puedes separar las funciones en pequeñas tareas, ejecutarlas com
  un todo, si alguna de ellas falla se deshace los cambios.
- Consistencia: Las bases de datos se relacionan con LLAVES PRIMARIAS, LLAVES
  FORANEAS, los datos tiene una congruencia entre sí.
- Aislamiento: Pueden haber varias tareas ejecutandose a la vez.
- Durabilidad: La información no se va a perder.

## Resumenes

- [MySQL](/mysql.md)
- [Postgres](/postgresql-edteam.md)
- [Mongo](/mongo/mongo.md)

## Comandos

ENTRAR A LA CONSOLA DE POSTGRES

```console
psql -U postgres -W
```

VER LOS COMANDOS \ DE POSTGRES

```console
\?
```

LISTAR TODAS LAS BASES DE DATOS

```console
\l
```

VER LAS TABLAS DE UNA BASE DE DATOS

```console
\dt
```

CAMBIAR A OTRA BD

```console
\c nombre_BD
```

DESCRIBIR UNA TABLA

```console
\d nombre_tabla
```

VER TODOS LOS COMANDOS SQL

```console
\h
```

VER COMO SE EJECTUA UN COMANDO SQL

```console
\h nombre_de_la_funcion
```

CANCELAR TODO LO QUE HAY EN PANTALLA

```console
Ctrl + C
```

VER LA VERSION DE POSTGRES INSTALADA, IMPORTANTE PONER EL ';'

```console
SELECT version();
```

VOLVER A EJECUTAR LA FUNCION REALIZADA ANTERIORMENTE

```console
\g
```

INICIALIZAR EL CONTADOR DE TIEMPO PARA QUE LA CONSOLA TE DIGA EN CADA EJECUCION
¿CUANTO DEMORO EN EJECUTAR ESA FUNCION?

```console
\timing
```

LIMPIAR PANTALLA DE LA CONSOLA PSQL

```console
Ctrl + L
```

## Archivos Configuración

- postgresql.conf
- pg_hba.conf
- pg_ident.conf

Muestra la ruta de nuestros archivos de configuración

```console
SHOW config_file;
```

- postgresql.conf: Configuración general de postgres, múltiples opciones
  referentes a direcciones de conexión de entrada, memoria, cantidad de hilos de
  pocesamiento, replica, etc.

- pg_hba.conf: Muestra los roles así como los tipos de acceso a la base de
  datos.

- pg_ident.conf: Permite realizar el mapeo de usuarios. Permite definir roles a
  usuarios del sistema operativo donde se ejecuta postgres.

## Comandos más usados

```console
SELECT VERSION();
    PostgreSQL 11.6 (Ubuntu 11.6-1.pgdg18.04+1) on x86_64-pc-linux-gnu, compiled by gcc (Ubuntu 7.4.0-1ubuntu1~18.04.1) 7.4.0, 64-bit
\h -- ayuda
\h comnado -- ayuda del comando especifico
\l -- Listar las bases
\c base de datos --moverse a una base de datos especifica
\dt -- listar las tablas de la base actual
\dn -- listar los esquemas de la base actual
\dv -- listar las vistas
\df -- listar las funciones
\du -- listar los usuarios
\g -- ejecutar ultimo comando 
\s -- historial de comandos
\l nombrearchivo --guardar lista de comandos
\i nombre archivo -- ejecuta comandos guardados
\e -- abrir editor 
\ef -- editor de funciones
\timming -- activar o desactivar el tiempo de respusta de las consultas
\q cerra consola
CREATE DATABASE base; -- crea base
CREATE TABLE tabla (columnas); crea tabla
INSERT INTO tabla(columna) VALUES('dato');
SELECT * FROM tabla;
UPDATE tabla SET cammpo = dato WHERE condicion;
DELETE FROM tabla WHERE condicion;
```
