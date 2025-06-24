#  API de Reseñas de Videojuegos

Este proyecto es una API RESTful desarrollada para gestionar usuarios y sus reseñas de videojuegos. Está construida utilizando una base de datos **no estructurada** , ideal para almacenar documentos flexibles con distintos atributos relacionados a juegos.

  Endpoints 

 # USUARIOS

 Registro de Usuario
**POST** `http://localhost:3000/usuarios/registro`  
**Content-Type:** `application/json`

  "nombre": "Alexi Sanchez",
  "email": "alexisanchez@gmail.com",
  "password": "miClaveSegura123"

 Login de Usuario
**POST http://localhost:3000/usuarios/login**
**Content-Type:** application/json


  "email": "alexisanchez@gmail.com",
  "password": "miClaveSegura123"

# CREAR RESEÑAS
  Crear una nueva reseña
**POST http://localhost:3000/juegos**
**Content-Type: application/json**

  **"titulo":** "God of War: Ragnarok",
  
  **"desarrollador":** "Santa Monica Studio",
  
  **"genero":** "Acción",
  
  **"plataforma":** ["PlayStation", "PC"],
  
  **"fechaLanzamiento":** "2023-09-20",
  
  **"calificacion":** 9,
  
  **"comentario":** "Narrativa profunda y combate fluido.",
  
  **"puntosFuertes":** ["Gráficos", "Historia"],
  
  **"puntosDebiles":** ["Puzzles repetitivos"],
  
  **"recomendado":** true,
  
  **"horasJugadas":** 45,
  
  **"autorId":** "AQUI_ID_USUARIO"

# CONSULTAS
 Obtener todas las reseñas
**GET http://localhost:3000/juegos**

 Filtrar por género
**GET http://localhost:3000/juegos?genero=RPG**

 Filtrar por calificación
**GET http://localhost:3000/juegos?calificacion=9**

 Obtener reseña por ID
**GET http://localhost:3000/juegos/AQUI_ID_RESEÑA**

 Obtener reseñas por usuario
**GET http://localhost:3000/usuarios/AQUI_ID_USUARIO/juegos**

# ACTUALIZAR / ACTIVAR / ELIMINAR
 Editar una reseña
**PUT http://localhost:3000/juegos/AQUI_ID_RESEÑA**
**Content-Type:** application/json


  "comentario": "Actualización de reseña con nuevo contenido",
  "horasJugadas": 60

 Desactivar una reseña (soft delete)
**PATCH http://localhost:3000/juegos/AQUI_ID_RESEÑA/deactivate**

 Reactivar una reseña
**PATCH http://localhost:3000/juegos/AQUI_ID_RESEÑA/activate**

 Eliminar reseña permanentemente
**DELETE http://localhost:3000/juegos/AQUI_ID_RESEÑA**

# Tecnologías Utilizadas
**Node.js**

**Express.js**

**MongoDB (base de datos no estructurada)**

**JWT (para autenticación)**

**Postman (para pruebas)**

