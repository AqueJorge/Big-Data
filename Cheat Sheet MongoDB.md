# Mongo DB Cheat sheet

### Mostrar todas las bases de datos 
- show dbs

### Mostrar Base de datos en la que estamos
- db 

### Moverse a otra Base de datos o crearla
- use database

### Crear una colección
- db.createCollection('name')
 
### Mostrar colecciones 
- show collections
 
### Insertar fila/documetos
- db.dbname.insert({name:'name', ...})

### Buscar fila/documento
- db.dbname.find()

### Obtener todo el formato de las filas/documentos
- db.dbname.find().pretty()

### Ordenar las filas/documetos
- db.dbname.find().sort({name:1/-1})

### Buscar dentro fila/documento(especifico)
- db.dbname.find({"name.name":10}) 

### Remover fila/documento
- db.dbname.remove({"name":"thename"})

### Actualizar fila/documento
- db.dbname.update({"name":"thename"},{"$set" {"old": new}})

### Actualizar multiples fila/documento
- db.dbname.update({"name":"thename"},{"$set" {"old": new}}, {"multi": true})

### Actualizar incrementando valores contador
- db.dbname.update({"name":"thename"},{"$inc":{"counter":1}})

### Contar las filas/documentos 
- db.dbname.find().count()
