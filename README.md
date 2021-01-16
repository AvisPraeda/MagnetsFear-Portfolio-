# MagnetsFear-Portfolio-
ESP: Este es un videojuego que realicé con un amigo para probar una mecánica que nos había resultado interesante. Puedes revisar el proyecto original en su cuenta (https://github.com/Pistoncito/Magnets-Fear).

ENG: This is a videogame I made with a friend to try interesting mechanics. You may revise the original project in his account (https://github.com/Pistoncito/Magnets-Fear).


## Documento de Diseño
Versión 1.2
### Creative Condors

Álvaro Ramirez Míguez

Víctor González Rivera

## Descripción del Juego
*Magnets Fear* es un juego arcade 2D en red para dos jugadores, de partidas 1vs1 de dos minutos.

Cada jugador controla a una esfera magnética con dos polaridades intercambiables, con las que pueden atraer o repeler proyectiles dependiendo de la polaridad de los últimos, y así proteger sus bases de los mismos.

### Plataforma
Inicialmente se desarrollará para PC, teniendo en cuenta que los controles puedan adaptarse más adelante a otras plataformas como consola o smartphone.

### Propósito y Público Objetivo
El objetivo del juego es crear una alternativa sencilla dentro de los juegos competitivos buscando un público amplio en edad y gustos. Para ello ideamos mecánicas intuitivas y fáciles de aprender que puedan generar dinámicas más complejas a medida que aumenta la habilidad del jugador.

## Mecánicas
### Jugabilidad
El jugador puede cambiar su polaridad cada 0.5 segundos, creando un campo magnético con un rango determinado, y mover su esfera en ocho direcciones. 

### Reglas Básicas
* Hay 2 proyectiles en el escenario que son atraídos por las esferas de polaridad opuesta y repelidos en caso contrario, teniendo en cuenta su posición respecto a la esfera.
* Los proyectiles que toquen una esfera cambian de polaridad.
* Tanto las esferas como los proyectiles rebotan contra los limites del escenario.
* Hay 3 bases por cada jugador, que son invulnerables durante 3 segundos al aparecer. Si no han sido destruídas, desaparecen 30 segundos después generando otras 3 en distintas posiciones, indiferentemente de cuántas quedasen anteriormente.
* Si un proyectil choca contra una base, la destruye. Una vez se destruyen todas las bases de un jugador, desaparecen todas las bases restantes en el escenario generando otras 3 para ambos jugadores en posiciones distintas.

![Error al cargar la imagen](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/magnets%20fear%20classic%20design.png)
![Error al cargar la imagen](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/magnets%20fear%20efecto%20de%20colision.png)
 
### Puntuación
Cada vez que una base sea destruída el jugador propietario gana 10 puntos.

### Fin de Partida y Objetivo
La partida acaba a los 2 minutos y gana el jugador con mayor puntuación.

### Cámara
El juego se desarrolla en todo momento en vista cenital.

### Controles
Controles por defecto:
Jugador 1
* Movimiento: W,A,S,D -> Arriba, Izquierda, Abajo y Derecha, respectivamente. Se permite la combinación de dos movimientos a la vez generando desplazamiento en diagonal (Ej: W + A -> Arriba + Izquierda). 
* Cambio de polaridad: Barra espaciadora.
Jugador 2: 
* Movimiento: Teclas de dirección. 
* Cambio de polaridad: Enter.

## Modos de Juego
Actualmente, sólo existe un modo en el que 2 jugadores compiten entre ellos con las normas explicadas en *Reglas Básicas*, *Puntuación* y *Objetivo*.

## Interfaces
### Diagrama de Flujo
![Error al cargar la imagen](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Diagramas/DiagramaFlujo1.3.PNG)

### Pantalla de Inicio
Se reflejarán las opciones:
1. Jugar: Comenzará una partida 1v1.
2. Opciones: Se abre una nueva interfaz donde se podrá configurar:
   * Audio: Se puede modificar el volumen del sonido y la música.
   * Controles: Se muestran los controles del personaje.
   * Volver: vuelve al menú de inicio.
3. Salir: Aparecerá un mensaje de confirmación y, en caso de que se acepte se saldrá del juego. 

![Error](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Interfaces/Men%C3%BAInicio.PNG)
![Error](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Interfaces/Opciones.PNG)
![Error](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Interfaces/Audio.PNG)
![Error](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Interfaces/Classic.PNG)
![Error](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Interfaces/FinPartida.PNG)


## Arte
### Lore
Un grupo de civilizaciones bautizado con el nombre de X decidieron crear un sistema de recolección de energía para solventar sus problemas y avanzar más rápido tecnológicamente. A este proyecto lo llamaron RIPPED (Recursive Intergalactic and Procedural Project of Energy Development).

RIPPED fue diseñada con la capacidad  generar copias de sí misma y viajar por el espacio en busca de energía.
En poco tiempo RIPPED encontró una fuente de energía lo suficientemente grande como para repartir entre sus civilizaciones padre y además usarla para mejorar su capacidad de aprendizaje.
De esta forma, se convirtió en un ente autosuficiente con conciencia propia, decidiendo abandonar la tarea asignada por este grupo de civilizaciones.

Decide generar pequeñas copias de sí misma que viajen aleatoriamente por el espacio para buscar fuentes de energía de forma más eficiente.

Estas pequeñas copias aumentaron de forma exponencial en número y saturaron el espacio, provocando colisiones con los planetas de civilizaciones cercanas.

Ante este problema, X tuvo que gastar la energía proporcionada por la propia RIPPED para defenderse de ella, creando así un sistema de protección basada en viajes espacio-temporales. Con este sistema podían viajar de forma segura a la vez que avisaban a otras civilizaciones de la inminente amenaza.

Este método tenía un inconveniente: las bases quedaban desprotegidas 30 segundos mientras enviaban el mensaje de aviso, ponían en marcha el sistema y recogían energías de fuentes cercanas. Para solventar este problema, trataron de replicar a RIPPED con una menor inteligencia y capacidad de aprendizaje con la misión de proteger a las bases mientras se encontraban indefensas.
Pero hubo otro inconveniente que no pudieron prever: cada vez que realizaban un viaje creaban una línea temporal adyacente que la esfera también debía proteger.

Cada jugador que crea una cuenta hace el papel de la IA que controla la esfera de una nueva civilización, que le transmite el mensaje para que sepa cual es su misión.

### Estética
Estilo futurista simplificado desarrollado en el espacio. 
Utilizamos colores vivos y saturados para diferenciar los distintos elementos en pantalla. La polaridad positiva se representa con rojo y la negativa con azul. Cada jugador podrá diferenciar la esfera que controla por una tonalidad más clara, mientras que la de su enemigo es más oscura. Lo mismo pasa con las bases de tu propia civilización y las enemigas. 

A los jugadores se les indicará el rango de acción de su magnetismo mediante un aura con el color de su polaridad. Antes de que las bases se intercambien, se mostrarán animaciones indicando dónde aparecerán las nuevas bases.

A continuación adjuntamos una imagen con el concepto.

![Error al cargar la imagen](https://github.com/AvisPraeda/MagnetsFear-Portfolio-/blob/master/Images/Estetica%20in-game.png)

### Música y Sonido (Incompleto)
* Música
  1. Menú de inicio, opciones.
  2. Durante la partida: Hay una base de fondo que se complementa dependiendo de la polaridad de los jugadores:
     * Jugador 1 y 2 con polaridad positiva.
     * Jugador 1 y 2 con polaridad negativa.
     * Jugador 1 con polaridad positiva y Jugador 2 con polaridad negativa.
     * Jugador 1 con polaridad negativa y Jugador 2 con polaridad positiva.
   La música se acelera al acercarse a los 30 segundos finales de la partida.

* Sonido
  1. Colisión proyectil-pared
  2. Colisión  proyectil-jugador
  3. Colisión proyectil-base
  4. Al ganar una partida
  5. Al perder una partida
  6. Animación momentos antes de que aparezcan las bases
  7. Aparición de las bases 
 

## Como usar la aplicacion
Para poder ejecutar la aplicación será necesario crear un servidor web. Recomendaría utilizar la extensión de chrome 200 ok web server
por su simplicidad. Simplemente, en la opción "CHOOSE FOLDER" seleccionar la carpeta del proyecto y pulsar en la dirección Web Server Url que aparece justo debajo.

Otra opción es la siguiente:
1. Instalar Spring o Eclipse STS.
2. Introducir el proyecto en la carpeta de direccionamiento del programa.
3. Abrir el proyecto y ejecutar como aplicación java el documento situado en la carpeta:  src/main/java/CreativeCondors.MagnetsFear/Application.java
4. Para terminar, la url que hay que escribir en el navegador es: localhost:8080.


