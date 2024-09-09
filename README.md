# Juego de Memorama de Secuencias
### Introducción Detallada del Proyecto

Este proyecto consiste en la creación de un juego de memorama en Python, diseñado para desafiar la capacidad de memoria del usuario a través de secuencias progresivamente más complejas. El juego incluye una serie de características clave, como la generación aleatoria de combinaciones de letras y números, un sistema de 10 niveles, un límite de 3 vidas, un contador regresivo visible en la terminal, y la posibilidad de volver a jugar si el usuario pierde todas sus vidas.

#### Proceso seguido para resolver el reto:

1. **Definición del objetivo del juego:**
   El primer paso fue definir claramente el propósito del juego. En este caso, el jugador debe memorizar una secuencia de combinaciones aleatorias de letras (A-F) y números (1-6), las cuales se incrementan en longitud a medida que el jugador avanza de nivel. El jugador tiene 3 vidas y debe superar un total de 10 niveles. Si pierde todas las vidas, el juego termina y se le ofrece la opción de volver a jugar o salir.

2. **Generación de las secuencias aleatorias:**
   Para hacer el juego más interesante, cada nivel genera una secuencia aleatoria diferente de combinaciones de letras y números. Esto se logró mediante el uso de la función `random.choice()` para seleccionar letras de un conjunto predefinido (A-F) y números (1-6). La secuencia crece a medida que se avanza de nivel, comenzando con una secuencia de 2 combinaciones en el nivel 1, y aumentando con cada nivel subsiguiente.

3. **Visualización de la secuencia y cuenta regresiva:**
   Para permitir que el jugador memorice la secuencia, se implementó una cuenta regresiva de 10 segundos que se muestra en la terminal. Esto se logró con un bucle `for` que muestra el tiempo restante en la terminal, actualizándose cada segundo. Después de mostrar la secuencia, la pantalla se limpia para evitar que el jugador vea la secuencia mientras ingresa su respuesta.

4. **Entrada y verificación de la secuencia:**
   El jugador debe ingresar la secuencia memorizada. Se capturó la entrada del jugador utilizando la función `input()`, y luego se comparó con la secuencia generada utilizando una simple comparación de listas. Si el jugador ingresa la secuencia correctamente, avanza al siguiente nivel; de lo contrario, pierde una vida.

5. **Manejo de las vidas y niveles:**
   El jugador empieza con 3 vidas. Cada vez que falla una secuencia, pierde una vida y se mantiene en el mismo nivel. Este enfoque asegura que el juego no avance si el jugador no ha memorizado correctamente la secuencia. Si pierde todas sus vidas, el juego termina y se le ofrece la opción de volver a intentarlo o salir del juego.

6. **Opción de volver a jugar:**
   Una vez que el jugador pierde todas sus vidas, se le pregunta si desea volver a jugar o salir. Si elige jugar nuevamente, el juego se reinicia desde el nivel 1 con 3 vidas. Si elige salir, el juego termina.

7. **Interfaz de usuario:**
   Se añadió una interfaz simple que incluye un mensaje de bienvenida y una explicación básica de las reglas antes de que el juego comience. El juego solo empieza cuando el jugador presiona la tecla Enter, lo que le da al usuario tiempo para prepararse.

### Resumen de características del código:
- **Generación de combinaciones aleatorias:** Letras de A a F y números del 1 al 6.
- **Niveles progresivos:** Cada nivel incrementa la longitud de la secuencia.
- **Tiempo para memorizar:** El jugador tiene 10 segundos para memorizar la secuencia, visualizando un contador regresivo en la terminal.
- **Sistema de vidas:** El jugador tiene 3 vidas. Si falla, no avanza de nivel y pierde una vida.
- **Opción de volver a jugar:** Si el jugador pierde todas sus vidas, puede optar por jugar de nuevo o salir del juego.
- **Pantalla de bienvenida:** Se muestra un mensaje inicial que explica las reglas y requiere que el usuario presione Enter para empezar.

Este código implementa un juego interactivo que ejercita la memoria, con una estructura modular que permite añadir nuevas funcionalidades o ajustes de dificultad en futuras versiones. Es ideal para ser ejecutado en la terminal y puede ser adaptado a otros entornos o lenguajes fácilmente.
