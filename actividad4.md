# Actividad 4

[Inicio](README.md)

### Lista de comandos utilizados:

#### 1) Utilizar la misma base de datos de películas e insertar varias películas (al menos 30) con distinto contenido
>  -use netflix
   -db.movies.insert([  
  {  
  "title": "Bitchip",  
  "description": "Duobam",  
  "rating": 4.3  
  },   
  {  
  "title": "Flowdesk",  
  "description": "Duobam",  
  "rating": 4.8  
  },   
   ...,  
   ...,
   hasta 10000 documentos aproximadamente
   ])  
   
#### 2) Crear índice en field rating y luego hacer búsquedas usando este campo

>  Tiempo en milisegundos sin índice:  
   -db.movies.find({ rating: 3.7 }).explain("executionStats").executionStats.executionTimeMillis  
   10  
   
>  Creo índice:  
   -db.movies.createIndex({ rating: 1 })  
   
>  Tiempo en milisegundos con índice creado:  
   -db.movies.find({ rating: 3.7 }).explain("executionStats").executionStats.executionTimeMillis  
   2  
   
#### 3) Crear índice en title y description, y después hacer búsquedas de texto en estos campos
>  -db.movies.createIndex({ title: "text", description: "text" })  
   -db.movies.find({ $text: { $search: "Zoolab" } })
