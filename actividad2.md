# Actividad 2

[Inicio](README.md)

### Lista de comandos utilizados:

##### 1) Crear una nueva base de datos de un sistema de streaming de video (ej. Netflix, Flow, Amazon Prime) que permita almacenar movies.
> -use netflix  
  -db.createCollection("movies")

##### 3) Agregar películas usando insert(), insertOne() & insertMany().
> -db.movies.insert({
    titulo: "Los hombres de negro"
  });  
        Retorno: 
  -db.movies.insert([]);  
  -db.movies.insertOne();  
  -db.movies.insertMany([]);

##### 4) Crear una nueva collection llamada players.
> -db.createCollection("players")

##### 5) Insertar 5 documentos en la collection players con datos básicos (nombre, apellido, posición, fecha de nacimiento, etc).
> -db.players.insertMany([  
	{  
	"nombre": "Juan",  
	"apellido": "Pérez",  
	"posicion":  "Delantero",  
	"fecha_nacimiento": new Date("1995-08-07")  
	},  
	{  
		"nombre": "Gabriel",  
		"apellido": "Rolando",  
		"posicion":  "Central",  
		"fecha_nacimiento": new Date("1997-04-22")  
	},  
	{  
		"nombre": "Omar",  
		"apellido": "Lapenta",  
		"posicion":  "Arquero",  
		"fecha_nacimiento": new Date("1965-01-02")  
	},  
	{  
		"nombre": "Luciano",  
		"apellido": "Martin",  
		"posicion":  "Delantero",  
		"fecha_nacimiento": new Date("1990-10-05")  
	},  
	{  
		"nombre": "Martin",  
		"apellido": "Rodríguez",  
		"posicion":  "Defensor",  
		"fecha_nacimiento": new Date("1985-12-29")  
	}  
])

##### 6) Listar todos los documentos de la collection players.
> -db.players.find()

##### 7) Crear otras collections con documentos (ej. teams, games, etc).

> Creo equipos:  
> -db.createCollection("teams")  
> -db.teams.insertMany([  
	{  
		"nombre": "Juventus",  
		"directorTecnico": "Diego Maradona"  
	},  
	{  
		"nombre": "Lanús",  
		"directorTecnico": "Ricardo Miller"  
	},  
	{  
		"nombre": "Boca",  
		"directorTecnico": "El más grande"  
	}  
])  

> Creo un partido:  
> -db.createCollection("games")  
> -db.games.insert({  
	"equipo_1": "Juventus",   
	"equipo_2": "Milan",  
	"fecha": new Date("2020-10-25")  
})
