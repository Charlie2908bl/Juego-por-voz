# Juego-por-voz
EcoMind Voice Challenge

Descripción: Juego de consola en Python donde el jugador elige un tema (de una lista de 15) y un nivel de dificultad. El juego muestra una palabra o frase en español relacionada con ese tema, el jugador debe pronunciarla en inglés, la app graba su voz, la reconoce, la traduce/compara contra la respuesta esperada y le da puntos. Mantiene vidas, racha de aciertos y un dato curioso relacionado al tema después de cada ronda (para reforzar aprendizaje, no solo vocabulario)

Funciones: Al iniciar, el programa recibe al jugador con un mensaje de bienvenida y le presenta la lista de los quince temas disponibles para que elija uno. Después le pide seleccionar un nivel de dificultad, que determina qué tan complejas serán las palabras o frases que deberá pronunciar y cuántos puntos valen.

Una vez elegidos el tema y la dificultad, el juego selecciona de manera aleatoria una palabra o frase en español relacionada con ese tema, cuidando de no repetir las que ya se usaron en la misma partida. Esa palabra se muestra en pantalla junto con la cantidad de vidas restantes, representadas con corazones.

El jugador debe decir en voz alta la traducción al inglés de esa palabra. El sistema graba el audio durante unos segundos, transforma esa grabación en texto mediante reconocimiento de voz configurado en inglés, y obtiene la traducción esperada de la palabra original para poder compararlas.

Antes de comparar, el texto reconocido y la traducción esperada se limpian: se convierten a minúsculas, se eliminan tildes y signos de puntuación, para evitar que pequeñas diferencias de formato arruinen una respuesta correcta. La comparación en sí no exige una coincidencia exacta, sino que permite cierto margen de similitud, ya que el reconocimiento de voz no siempre transcribe perfecto.

Si la respuesta es correcta, el jugador gana puntos según la dificultad elegida, y si lleva varias respuestas correctas seguidas, recibe puntos adicionales por la racha. Si la respuesta es incorrecta, pierde una vida y se le muestra cuál era la traducción correcta. Después de cada ronda, ya sea acierto o error, se presenta un dato curioso relacionado con el tema elegido, de forma que el juego no solo evalúa pronunciación sino que también enseña algo nuevo en cada ronda.

El juego continúa presentando rondas hasta que el jugador pierde sus tres vidas, momento en el que termina la partida. Al finalizar, se muestra un resumen con el puntaje total obtenido, ese puntaje se guarda junto con el nombre del jugador, el tema y el nivel jugado en un archivo que funciona como historial permanente, y se presenta una tabla con los mejores puntajes registrados hasta el momento, ya sea en general o filtrados por tema. Por último, se le pregunta al jugador si desea jugar de nuevo, pudiendo elegir otro tema o nivel, o si prefiere salir del juego.
