# AppQuizMaster

## Contexto del Problema
Actualmente, muchas personas disfrutan de las aplicaciones de trivia y quizzes como una forma de entretenimiento, aprendizaje o incluso como desafío entre amigos. Sin embargo,
a menudo las aplicaciones disponibles no ofrecen la flexibilidad de crear quizzes personalizados ni facilitan una adecuada gestión del contenido por parte de los usuarios. 
Además, algunas no permiten medir adecuadamente el desempeño de los usuarios en los quizzes o carecen de una interfaz sencilla y accesible.

## Propuesta: AppQuizMaster
AppQuizMaster es una aplicación que permite a los usuarios crear, compartir y resolver quizzes de manera sencilla y divertida.
Con esta herramienta, los usuarios pueden seleccionar temas de interés, crear sus propias preguntas y respuestas, y realizar un seguimiento de su progreso. 
Esta aplicación está dirigida a personas de todas las edades que deseen mejorar sus conocimientos, jugar con amigos o simplemente divertirse.

## Características
**Creación de Quizzes Personalizados:** Los usuarios podrán crear quizzes con sus propias preguntas y respuestas. Esto fomenta la creatividad y el aprendizaje, permitiendo a los usuarios compartir sus propios cuestionarios con otros.
**Temáticas Variadas:** Los quizzes podrán clasificarse por temas (ciencia, historia, deportes, etc.), lo que permite a los usuarios elegir según sus intereses.
**Niveles de Dificultad:** Los usuarios podrán filtrar preguntas o quizzes basados en tres niveles de dificultad: Fácil, Medio y Difícil.
**Progreso del Usuario:** Se podrá seguir el progreso del usuario, midiendo su desempeño en los quizzes resueltos, con estadísticas de respuestas correctas e incorrectas.
**Modo Desafío:** Opción para competir con otros usuarios en tiempo real, completando quizzes en modo desafío.

# Modelo Relacional
Basado en la estructura SQL previamente detallada, aquí está el modelo relacional adaptado para AppQuizMaster:

**Usuario:**
- IdUsuario (clave primaria)
- NombreUsuario
- CorreoElectronico

**Pregunta**
- IdPregunta (clave primaria)
- TextoPregunta
  
**Respuesta**
- IdRespuesta (clave primaria)
- TextoRespuesta
- EsCorrecta (booleano)
- IdPregunta (relación con tabla Pregunta)

**Quiz**
- IdQuiz (clave primaria)
- NombreQuiz
- DescripcionQuiz

**QuizPregunta (relación muchos a muchos entre Quiz y Pregunta)**
- IdQuiz (relación con tabla Quiz)
- IdPregunta (relación con tabla Pregunta)

**QuizUsuario (relación muchos a muchos entre Quiz y Usuario)**
- IdQuiz (relación con tabla Quiz)
- IdUsuario (relación con tabla Usuario)

**SQL**
![image](https://github.com/user-attachments/assets/528b1ad5-d1ec-4a09-a68c-c61bcba03116)
![image](https://github.com/user-attachments/assets/1559878a-ed90-4cfe-aa4d-a91b1676a731)

# Desarrollo de la Propuesta
Nuestra solución será implementada a través de una aplicación web y móvil donde los usuarios pueden interactuar de manera sencilla con la plataforma. Se crearán las siguientes funcionalidades específicas:

**Panel de Usuario:** Los usuarios podrán registrarse e iniciar sesión utilizando su correo electrónico.

**Creación de Quizzes:** Los usuarios pueden crear un quiz desde cero, añadiendo preguntas y respuestas.

**Resolución de Quizzes:** Los usuarios podrán resolver quizzes de otros usuarios o quizes predeterminados por la aplicación.

**Interacción Social:** Se permitirá compartir quizzes con amigos mediante enlaces.

**Ranking y Progreso:** Los usuarios podrán ver sus estadísticas: cantidad de preguntas respondidas, porcentaje de aciertos, y rankings semanales de los mejores jugadores.

