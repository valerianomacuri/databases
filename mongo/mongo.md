# MongoDB

## Comandos

- Verificar la version:

```console
mongod --version
```

- Habilitar MongoDB para que se inicie al iniciar el sistema.

```console
sudo systemctl enable mongod
```

- Iniciar MongoDB server:

```console
sudo service mongod start
```

- Ver el estatus:

```console
sudo service mongod status
```

- Editar MongoDB config file:

```console
sudo nano /etc/mongod.conf
```

- Restaurar MongoDB:

```console
sudo systemctl restart mongod
```

- Conectarse a MongoDB shell:

```console
mongosh
```

- Si ejecuta `mongo` como alternativa a `mongosh`, le mostrara la siguiente
  advertencia:

```console
Advertencia: el "mongo" shell ha sido reemplazado por "mongosh", que ofrece una mejor usabilidad y compatibilidad. El "mongo" shell ha quedado obsoleto y se eliminará en un próximo lanzamiento.
```

- Crear o cambiar de base de datos:

```console
use database
```

- Ingresar como usuario administrador:

```console
mongo -u myUserAdmin -p root --authenticationDatabase admin
```

> Nota: `mongosh` usa un interprete de javascript, es decir que puede ejecutar
> código de javascript.

## Mongo URI

![connection uri parts](connection_uri_parts.png)

## Mongo SHELL Comands

- [Documentación](https://www.mongodb.com/docs/manual/reference/mongo-shell/)

Mostrar bases de datos:

```console
show dbs
```

Usar una base de datos:

```console
use taskdb
```

Mostrar las colecciones de una base de datos:

```console
show collections
```

Mostrar todos los documentos de una colección:

```console
db.<collection>.find()
```

Borrar un documento de una colección:

```console
db.<collection>.deleteOne( { "_id" : ObjectId("[id]") } )
```

## bson

- M: M es una representación desordenada de un documento BSON. Este tipo debe
  usarse cuando el orden de los elementos no importa. Este tipo se maneja como
  una interfaz normal de map[string]{} al codificar y decodificar. Los elementos
  se serializarán en un orden aleatorio e indefinido. Si el orden de los
  elementos importa, se debe usar una D en su lugar.

* D: el tipo bson.D representa un documento bson que contiene elementos
  ordenados.

### keywords

- `$set`: permite realizar una actualización parcial del documento.

## Cargar los datos a MongoDB:

Vale la pena mencionar que puede usar la utilidad mongoimport para cargar la
receta. json directamente en la colección de recetas sin escribir una sola línea
de código en Golang. El comando para esto es el siguiente:

```console
mongoimport --username [admin] --password [password] --authenticationDatabase admin --db demo --collection recipes --file recipes.json --jsonArray
```

## MongoDB Service Commands

You can start, stop, enable, disable, restart using the following commands.

- Start MongoDB

```console
sudo systemctl start mongodb
```

- Stop MongoDB

```console
sudo systemctl stop mongodb
```

- Enable MongoDB

```console
sudo systemctl enable mongodb
```

- Disable MongoDB

```console
sudo systemctl disable mongodb
```

- Restart MongoDB

```console
sudo systemctl restart mongodb
```
