# 🎮 En Búsqueda de la Era Dorada de los Videojuegos

## 📖 Descripción del Proyecto
Los videojuegos son un negocio masivo; según Mordor Intelligence, se proyecta que el mercado global de los videojuegos tenga un valor de más de $300 mil millones para 2027. Con tanto en juego, los desarrolladores buscan crear el próximo gran éxito. Pero, ¿los juegos están mejorando o la "era dorada" de los videojuegos ya pasó? 

En este proyecto de análisis de datos con SQL, exploramos las ventas globales, así como las calificaciones de usuarios y críticos para los 400 mejores videojuegos lanzados desde 1977. El objetivo es identificar cuáles fueron los mejores años para la industria y explorar el lado comercial del gaming.

## 🗄️ Conjunto de Datos
El análisis se realiza sobre un esquema de base de datos llamado `games`, el cual contiene las siguientes tablas principales:

* **`game_sales`**: Contiene información sobre el nombre del juego, plataforma, editor, desarrollador, copias vendidas (en millones) y el año de lanzamiento.
* **`reviews`**: Almacena las calificaciones de los críticos (`critic_score`) y de los usuarios (`user_score`) según Metacritic.
* **Tablas de apoyo**: `users_avg_year_rating` y `critics_avg_year_rating` con los promedios precalculados por año.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** SQL
* **Técnicas:** JOINs (Inner/Left), Funciones de Agregación (`COUNT`, `AVG`), Filtrado de Grupos (`HAVING`), Operaciones Aritméticas entre columnas y Ordenamiento de Datos.

## 📊 Análisis y Consultas Principales

**1. Los Juegos Más Vendidos de la Historia**
Identificamos los 10 títulos más vendidos. El indiscutible número uno es *Wii Sports* para la consola Wii con 82.90 millones de copias vendidas, seguido por *Super Mario Bros.* para NES.

**2. Los 10 Mejores Años Según la Crítica**
Calculamos el promedio de calificaciones de los críticos agrupado por año, filtrando solo aquellos años con al menos 4 lanzamientos para asegurar una muestra representativa. El año **1998** lidera la lista con un puntaje promedio de 9.32.

**3. Los "Años Dorados" (Consenso entre Críticos y Usuarios)**
Cruzamos las calificaciones promedio de la crítica y de los usuarios para encontrar los años donde **ambos** grupos otorgaron calificaciones excepcionales (mayores a 9.0). Además, calculamos la diferencia (`diff`) entre ambas opiniones para ver el nivel de consenso. Años como 1998 destacaron por una diferencia mínima de apenas -0.08, demostrando un acuerdo casi perfecto entre jugadores y prensa especializada.
