# Actividad 3

[Inicio](README.md)

### Lista de comandos utilizados:

#### 1) Utilizar la misma base de datos de películas e insertar varias películas con distinto contenido
>  -use netflix
   -db.movies.insert([  
   {  
   "title": "Batman ninja",
   "year": 2018,  
   "rating": 3.7,  
   "genre": "Anime",  
   "description": "Mientras luchaba contra Gorilla Grodd en el Manicomio Arkham, Batman se queda atrapado en la máquina de desplazamiento temporal del motor Quake de Gorilla Grodd y es enviado al Japón feudal.",  
   "actors": [],  
   "country": "Japón",  
   "income": 1548785,  
   "duration": 85 
   }, 
   {  
   "title": "A la deriva",  
   "year": 2018,  
   "rating": 3.7,  
   "genre": "Anime",  
   "description": "Mientras luchaba contra Gorilla Grodd en el Manicomio Arkham, Batman se queda atrapado en la máquina de desplazamiento temporal del motor Quake de Gorilla Grodd y es enviado al Japón feudal.",  
   "actors": ["Shailene Woodley", "Sam Claflin"],  
   "country": "Estados Unidos",  
   "income": 59945012,  
   "duration": 96  
   },  
   {  
   "title": "Batman ninja",
   "year": 2018,  
   "rating": 3.7,  
   "genre": "Anime",  
   "description": "Mientras luchaba contra Gorilla Grodd en el Manicomio Arkham, Batman se queda atrapado en la máquina de desplazamiento temporal del motor Quake de Gorilla Grodd y es enviado al Japón feudal.",  
   "actors": [],  
   "country": "Hollywood",  
   "income": 784878945,  
   "duration": 85 
   }, 
   {  
   "title": "A la deriva",  
   "year": 2018,  
   "rating": 3.7,  
   "genre": "Anime",  
   "description": "Mientras luchaba contra Gorilla Grodd en el Manicomio Arkham, Batman se queda atrapado en la máquina de desplazamiento temporal del motor Quake de Gorilla Grodd y es enviado al Japón feudal.",  
   "actors": ["Shailene Woodley", "Sam Claflin"],  
   "country": "Estados Unidos",  
   "income": 59945012,  
   "duration": 96  
   },  
   ])
   
#### 2) Listar todas las películas del año 2018
>  -db.movies.find({ year: 2018 })

#### 3) Listar las 10 primeras películas de Hollywood
>  -db.movies.find({ country: "Hollywood" }).limit(10)

#### 4) Listar las 5 películas más taquilleras
>  -db.movies.find().sort({ income: -1 }).limit(5)


#### 5) Listar el 2do conjunto de 5 películas más taquilleras
>  -db.movies.find().sort({ income: -1 }).skip(5).limit(5)

#### 6) Repetir query 3 y 4 pero retornando sólo el título y genre
>  -db.movies.find({ country: "Hollywood" }, { title: 1, genre: 1, _id: 0 }).limit(10)  
   -db.movies.find({}, { title: 1, genre: 1, _id: 0 }).sort({ income: -1 }).limit(5)
   
#### 7) Mostrar los distintos países que existen en la base de datos
>  -db.movies.distinct("country")
