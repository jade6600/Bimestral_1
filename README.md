# Bimestral_1
# Bimestral_1

## Para poder empezar
el import pygame es un linea que nos habilita la biblioteca Pygame.
from random import randint: Esta linea importa la función random esta función se usa para generar números enteros aleatorios dentro de el rango establecido.
Aqui se inicia pygame y se empiezan a crear las especificaciones.

- ```pygame.init():```inicializa todos los módulos importados de Pygame.

- ALTURA_VENTANA = 600: Define una constante para la altura de la ventana.
- COLOR_FONDO = (255, 255, 250): Define los colores del fondo de la ventana usando valores RGB (rojo, verde, azul).
- PANTALLA = ```pygame.display.set_mode((ALTURA_VENTANA))```
- ANCHURA_VENTANA)): Crea la ventana del juego con unas dimensiones especificas que se extraen de ALTURA_VENTANA y ANCHURA_VENTANA.
## Las variables son:

- PARAR_JUEGO = False:Controla el bucle principal del juego y cuando es True el juego termina.
XX_COHETE = 210, YY_COHETE = 300: Posición inicial del cohete en la ventana.
- ALTURA_COHETE = 88, ANCHURA_COHETE = 175: Son las dimensiones de el cohete.
- MOVIMIENTO_XX_COHETE = 0: Es la velocidad del movimiento del cohete en el eje X.
- XX_PLANETA = randint(30, 130), YY_PLANETA = 20: Seria cmo la posición inicial del primer planeta.
- ALTURA_PLANETA = 111, ANCHURA_PLANETA = 80: Son las dimensiones de toos los planetas.
- XX_ENTRE_PLANETAS = 350, YY_ENTRE_PLANETA = 125: Es la distancia entre los dos planetas.
- VELOCIDAD_PLANETAS = 2: Es la velocidad de descenso de los planetas.
- PUNTOS = 0: Inicializa la puntuación del jugador.
- FUENTE = pygame.font.Font(None, 24): Crea como un objeto fuente para mostrar el texto de la puntuación.
- MARCADOR = FUENTE.render("0 puntos", 1, (255, 0, 0)): Renderiza el texto inicial de la puntuación.

## Para cargar las imagnes

- ```IMG_COHETE = pygame.image.load("img/COHETE.png"):``` la imagen del cohete.
- ```IMG_PLANETA_IZQUIERDO = pygame.image.load("img/PLANETA.png"):``` Carga la imagen del planeta.
- ```IMG_PLANETA_DERECHO = pygame.image.load("img/PLANETA.png"):``` Carga la imagen del planeta.
- Se pone un titulo a la ventana

```pygame.display.set_caption("PRIMER JUEGO"):``` Establece el título de la ventana del juego.
# Bucle principal del juego:

- ```while not PARAR_JUEGO:``` Este bucle se ejecuta hasta que PARAR_JUEGO sea True.
- ```for event in pygame.event.get():``` Itera sobre todos los eventos que han ocurrido.
- ```if event.type == pygame.KEYDOWN:``` Comprueba si si se ha presionado una tecla.
- ```if event.key == pygame.K_ESCAPE:``` Si es la tecla escape pues termina el juego.
- ```if event.key == pygame.K_RIGHT:``` Si es la flecha derecha entonces mueve el cohete a la derecha.
```elif event.type == pygame.KEYUP:```Comprueba si se ha soltado una tecla.
-MOVIMIENTO_XX_COHETE = -4: Mueve el cohete a la izquierda.
- ALTURA_VENTANA:: Termina el juego si el cohete se sale de la visibilidad de la pantalla.
- PANTALLA.fill(COLOR_FONDO): Rellena la pantalla con el color de fondo previamente seleccionado.
- PANTALLA.blit(...): Dibuja las imágenes de los planetas y el cohete en la pantalla.

- VELOCIDAD_PLANETAS: Mueve los planetas en direccion hacia abajo.
```if YY_PLANETA > ANCHURA_VENTANA:``` Si los planetas llegan al final, reinicia su posición y aumenta la puntuación.
Sección de colisiones: Calcula las áreas de colisión de los planetas y el cohete, y termina el juego si hay una colisión.
XX_COHETE = XX_COHETE + MOVIMIENTO_XX_COHETE: Actualiza la posición del cohete.
- PANTALLA.blit(MARCADOR, (20, 580)): Hace la ilustracion de la puntuación en la pantalla.
pygame.display.update(): Actualiza la pantalla para mostrar los cambios a medida que corre el juego.