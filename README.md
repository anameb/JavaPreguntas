# JavaPreguntas-- Proyecto sofka.
 
Para realizar este proyecto me base en un proyecto ya implementado en el diplomado realizado este año en MISIONTIC, de el cual se tomo la conexion con la  base de datos. 

La informacion de este proyecto se almaceno en la base de datos MySQL, por medio del modulo XAMPP, el nombre de la base datos que se le asigno a este proyecto es : app_preguntas y el puerto de conexión usado es localhost:3306.

![image](https://user-images.githubusercontent.com/88283220/147309529-af54251b-14c4-4b2e-bc5f-799a7b426068.png)

# Clases BD

<img width="736" alt="BD app_preguntas" src="https://user-images.githubusercontent.com/88283220/147307953-670e497e-8928-4da6-931d-45870a1aebdd.png">

# Creacion de tablas para almacenar información de premios, categorias, preguntas , opciones de respuesta y jugadores. 

CREATE TABLE appPremio (
id INTEGER (10) AUTO_INCREMENT PRIMARY KEY, 
valor INTEGER (10), idRonda INTEGER (10) );

CREATE TABLE appCategoria ( 
id INTEGER (10) AUTO_INCREMENT PRIMARY KEY, name varchar (10) );

CREATE TABLE appPregunta ( 
id INTEGER (10) AUTO_INCREMENT PRIMARY KEY, 
categoria varchar (10),
enunciado varchar (10),
opciones varchar (250),
idRonda INTEGER (10) );

CREATE TABLE appOpciones ( 
id INTEGER (10) AUTO_INCREMENT PRIMARY KEY, 
enunciado varchar (250), 
opcionCorrecta boolean );

CREATE TABLE appJugador ( 
id INTEGER (10) AUTO_INCREMENT PRIMARY KEY, 
name varchar (10), 
premioTotal INTEGER (10));


# Queries usados para la creacion de rondas, categorias, premios y preguntas para pruebas 

INSERT INTO appronda (name) VALUES ("Ronda 1");
INSERT INTO appronda (name) VALUES ("Ronda 2");
INSERT INTO appronda (name) VALUES ("Ronda 3");
INSERT INTO appronda (name) VALUES ("Ronda 4");
INSERT INTO appronda (name) VALUES ("Ronda 5");

INSERT INTO appcategoria (name) VALUES ("Matematicas");
INSERT INTO appcategoria (name) VALUES ("Cultura General");
INSERT INTO appcategoria (name) VALUES ("Deporte");
INSERT INTO appcategoria (name) VALUES ("Ciencias");
INSERT INTO appcategoria (name) VALUES ("Programación");

INSERT INTO apppremio (valor, idRonda) VALUES (50, 1);
INSERT INTO apppremio (valor, idRonda) VALUES (100, 2);
INSERT INTO apppremio (valor, idRonda) VALUES (200, 3);
INSERT INTO apppremio (valor, idRonda) VALUES (400, 4);
INSERT INTO apppremio (valor, idRonda) VALUES (800, 5);

INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (1, "Si 10 + x es 5 más que 10, ¿cuál es el valor de 2x?", 1);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (2, "¿Cuál es el nombre del río más largo del mundo?", 1);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (3, "¿Cuándo se celebró el primer mundial de fútbol?", 1);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (4, "En qué parte del cuerpo está el hígado", 1);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (5, "Son los tipos de datos que se manejan en Programación.", 1);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (1, "Aproxima el número 58 a la decena.", 2);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (2, "¿Cuál es el país más grande del mundo?", 2);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (3, "¿Qué revista concede el Balón de Oro?", 2);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (4, "¿Cuántos elementos tiene la tabla periódica?", 2);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (5, "¿Que es un algoritmo?", 2);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (1, "Pregunta de prueba Ronda 3 Categoria 1 respuesta 1", 3);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (2, "Pregunta de prueba Ronda 3 Categoria 2 respuesta 1", 3);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (3, "Pregunta de prueba Ronda 3 Categoria 3 respuesta 1", 3);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (4, "Pregunta de prueba Ronda 3 Categoria 4 respuesta 1", 3);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (5, "Pregunta de prueba Ronda 3 Categoria 5 respuesta 1", 3);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (1, "Pregunta de prueba Ronda 4 Categoria 1 respuesta 1", 4);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (2, "Pregunta de prueba Ronda 4 Categoria 2 respuesta 1", 4);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (3, "Pregunta de prueba Ronda 4 Categoria 3 respuesta 1", 4);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (4, "Pregunta de prueba Ronda 4 Categoria 4 respuesta 1", 4);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (5, "Pregunta de prueba Ronda 4 Categoria 5 respuesta 1", 4);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (1, "Pregunta de prueba Ronda 5 Categoria 1 respuesta 1", 5);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (2, "Pregunta de prueba Ronda 5 Categoria 2 respuesta 1", 5);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (3, "Pregunta de prueba Ronda 5 Categoria 3 respuesta 1", 5);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (4, "Pregunta de prueba Ronda 5 Categoria 4 respuesta 1", 5);
INSERT INTO apppregunta (idCategoria, enunciado, idRonda) VALUES (5, "Pregunta de prueba Ronda 5 Categoria 5 respuesta 1", 5);

INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (1, "1. -5", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (1, "2. 5", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (1, "3. 10", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (1, "4. 25", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (2, "1. Río Nilo", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (2, "2. Río Amazonas", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (2, "3. Río Danubio", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (2, "4. Río Magdalena", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (3, "1. 1930", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (3, "2. 1956", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (3, "3. 1878", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (3, "4. 1912", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (4, "1. arriba", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (4, "2. izquierda", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (4, "3. abajo", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (4, "4. derecha", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (5, "1. Tipo Java, C++, Smalltalk, Python, Object Pascal, Visual .net, Visual Basic, Delphi, Perl, entre otros.", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (5, "2. Cadena, Boleano, Carácter, Numeros, alfanuemrico, Entero.", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (5, "3. String, Boolean, Char, Integer, int, etc.", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (5, "4. Simbólicos, de estructura, de cadena, de complemento, generales, particulares, entre otros.", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (6, "1. 50", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (6, "2. 60", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (6, "3. 66", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (6, "4. 55", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (7, "1. China", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (7, "2. Rusia", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (7, "3. India", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (7, "4. Colombia", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (8, "1. La revista France Footbal", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (8, "2. La revista Semana", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (8, "3. La revista Vanidades", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (8, "4. La revista European League", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (9, "1. 120", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (9, "2. 112", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (9, "3. 100", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (9, "4. 118", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (10, "1. Es una serie de pasos para dar solución a un problema.", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (10, "2. Es el orden de los pasos para un sistema de informacion.", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (10, "3. Es el estudio de las ordenes creadas por un programador.", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (10, "4. Es la forma de realizar un programa", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (11, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (11, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (11, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (11, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (12, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (12, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (12, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (12, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (13, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (13, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (13, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (13, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (14, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (14, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (14, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (14, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (15, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (15, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (15, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (15, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (16, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (16, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (16, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (16, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (17, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (17, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (17, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (17, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (18, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (18, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (18, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (18, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (19, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (19, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (19, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (19, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (20, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (20, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (20, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (20, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (21, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (21, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (21, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (21, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (22, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (22, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (22, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (22, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (23, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (23, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (23, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (23, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (24, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (24, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (24, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (24, "4. opcion 4", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (25, "1. opcion 1", true);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (25, "2. opcion 2", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (25, "3. opcion 3", false);
INSERT INTO appopciones (idPregunta, enunciado, opcionCorrecta) VALUES (25, "4. opcion 4", false);


# Codigo 
Se crearon cada una de la clases, los controladores y una clase principal la cual llame JavaPreguntas, en esta se encuentra almacenada la logica del proyecto, esta es la clase que se debe ejecutar  a la hora de provar el proyecto. 

![image](https://user-images.githubusercontent.com/88283220/147309898-6ff83735-0e43-4bc4-9818-905ee8f450c0.png)

