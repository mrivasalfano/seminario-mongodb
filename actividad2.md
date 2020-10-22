# Actividad 2

[Inicio](README.md)

### Lista de comandos utilizados:

##### 1) Crear una nueva base de datos de un sistema de streaming de video (ej. Netflix, Flow, Amazon Prime) que permita almacenar movies.
> -use netflix  
  -db.createCollection("movies")

##### 3) Agregar películas usando insert(), insertOne() & insertMany().
> -db.movies.insert({  
    "title": "Los hombres de negro",  
    "year": 1997,  
    "rating": 4.5,  
    "genre": "Acción",  
    "description": "Narra la historia de una organización secreta que vigila la actividad alienígena en la Tierra.",  
    "actors": ["Tommy Lee Jones", "Will Smith"],  
    "country": "Estados unidos",  
    "income": 589390500,  
    "duration": 98  
  });
  
  Retorno: WriteResult({ "nInserted" : 1 })
  
> -db.movies.insert([  
  {  
  "title": "Carrera contra la muerte",
  "year": 1987,  
  "rating": 4.0,  
  "genre": "Ciencia Ficción",  
  "description": "La película, ambientada en un distópico año 2017, relata los sucesos ocurridos en un programa de televisión llamado The Running Man (traducido       literalmente como El Corredor) donde criminales convictos deben escapar de asesinos profesionales que los quieren llevar a la muerte.",  
  "actors": ["Arnold Schwarzenegger", "María Conchita Alonso"],  
  "country": "Estados unidos",  
  "income": 38122105,  
  "duration": 101 
  },  
  {  
  "title": "Enamorándose",
  "year": 1984,  
  "rating": 4.1,  
  "genre": "Romance",  
  "description": "Mientras hacen las compras para sus respectivas familias en Navidad el arquitecto Frank Raftis (De Niro) y la bella artista gráfica Molly Gilmore (Streep) se cruzan y confunden sus regalos de Navidad. Lo que comienza como una amistad agradable se convierte en un romance.",  
  "actors": ["Meryl Streep", "Robert De Niro"],  
  "country": "Estados unidos",  
  "income": 11129057,  
  "duration": 106  
  }
  ]);  
  
  Retorno:  
  BulkWriteResult({  
        "writeErrors" : [ ],  
        "writeConcernErrors" : [ ],  
        "nInserted" : 2,  
        "nUpserted" : 0,  
        "nMatched" : 0,  
        "nModified" : 0,  
        "nRemoved" : 0,  
        "upserted" : [ ]  
  })
  
> -db.movies.insertOne({  
    "title": "El clán",  
    "year": 2015,  
    "rating": 4.2,  
    "genre": "Drama",  
    "description": "La historia está basada en el caso policial del Clan Puccio, que conmovió a la sociedad argentina a comienzos de los años 80.",  
    "actors": ["Guillermo Francella", "Peter Lanzani"],  
    "country": "Argentina",  
    "income": 20381995,  
    "duration": 110  
  });  
  
  Retorno: 
  {  
  "acknowledged" : true,  
  "insertedId" : ObjectId("5f918437f2fdb8aecb4be001")  
  }
  
> -db.movies.insertMany([  
  {  
    "title": "El Gato con Botas",  
    "year": 2011,  
    "rating": 4.7,  
    "genre": "Animacion",  
    "description": "Gato es un fugitivo de la justicia que se dedica a cometer robos para subsistir, sin robar a personas de bajos recursos o a iglesias.",  
    "actors": [],  
    "country": "Estados Unidos",  
    "income": 554709226,  
    "duration": 90  
  },  
  {  
    "title": "Alicia en el país de las maravillas",  
    "year": 2010,  
    "rating": 4.6,  
    "genre": "Fantasía",  
    "description": "La pequeña Alicia Kingsleigh, tiene una pesadilla sobre un mundo fantástico de seres extraños, relatando a su padre, Charles Kingsleigh lo que había en ese lugar. Pero él la consuela diciéndole que los sueños no pueden lastimarle.",  
    "actors": ["Mia Wasikowska", "Johnny Depp"],  
    "country": "Estados Unidos",  
    "income": 1025467110,  
    "duration": 108  
  }  
  ]);
  
  Retorno:  
  {  
        "acknowledged" : true,  
        "insertedIds" : [  
                ObjectId("5f918945f2fdb8aecb4be004"),  
                ObjectId("5f918945f2fdb8aecb4be005")  
        ]  
  }
