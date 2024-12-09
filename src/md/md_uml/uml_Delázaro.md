# Diagrama UML

![Diagrama UML](/src/assets/images/diagramas_uml/uml_mauricio.png)

# Descripción de clases

## Interfaz 

La clase ***Interfaz*** está encargada de dar visualización al usuario de los distintos apartados del juego, por ejemplo, el perfil de usuario, la tienda o la selección de mapas. También permite al usuario interactuar con los distintos sistemas del juego, ya sea abriendo y cambiando la configuración o la opción de agregar amigos en el perfil.

La relación con todas las demás clases recae en que la interfaz es parte esencial para que el usuario pueda visualizar e interacturar con cada una. 

Esta clase abarca los siguientes requerimientos: 

- RF-005: El juego debe permitir al usuario pausar y reanudar la partida en cualquier momento con solo presionar un botón en la pantalla.
- RF-011: El juego tendrá una interfaz gráfica que se encargará de todo lo visual, mostrar el perfil, los mapas, rutas en los mapas, los camiones que estan en las rutas, los pasajeros, la tienda, etc.
- RF-012: El juego contará con un apartado de configuraciones donde podrá modificar el volumen de la música, el nivel del sonido, el idioma, etc.

## Usuario 

La clase ***Usuario*** maneja toda información relevante para el usuario en cuanto al registro e ingreso de su cuenta. Se incluye la opción de registrase con un correo electrónico, solicituando la creación de un nombre de usuario, contraseña y un registro de edad. 

Se relaciona con las siguientes clases: ***Configuración*** y ***Perfil***. El usuario tendrá acceso al menu de configuraciones así como se le permitirá la creación de distintos perfiles. 

Esta clase abarca los siguientes requerimientos:

- RF-001: Para poder acceder completamente a las funciones, se debe iniciar sesión con un usuario y contraseña. De esta manera podremos ayudar a la creación y personalización de perfiles y a la seguridad de la cuenta.
- RF-003: El programa debe de permitir a los usuarios crear un perfil local, en donde, se guarde el progreso, tanto como logros y puntuaciones previamente obtenidas al jugar.

## Perfil 

La clase ***Perfil*** almacena el progreso del usuario referente a los logros, mapas desbloqueados, camiones comprados o el tiempo de juego. Se le permite al usuario crear y manejar distintos perfiles así pudiendo tener distintos porcentajes de avance en cada perfil. Otra funcionalidad del perfil es la posibilidad de personalizar el nombre o la opción de agregar amigos. 

El ***Perfil*** tiene relación con varias clases, entre ellas los ***Mapas***, ***Camiones*** y ***Usuario***. Las clases **Mapas** y **Camiones** sirven para rastrear el progreso del usuario en perfil, y la clase usuario permite la creación de los mismos, como antes mencionado en el apartado [Usuario](#usuario).

Esta clase abarca los siguientes requerimientos:

- RF-003: El programa debe de permitir a los usuarios crear un perfil local, en donde, se guarde el progreso, tanto como logros y puntuaciones previamente obtenidas al jugar.
- RF-014: El usuario podrá agregar como amigos a otros usuarios que tengan creado un perfil dentro del juego.
- RF-016: El juego contara con un apartado donde se puedan consultar las estadisticas del jugador (horas jugadas, monedas recolectadas, cantidad de rutas, camiones, etc.)

## Configuración 

La clase de ***Configuración*** es el apartado donde el usuario podrá modificar distintos parametros del juego como el brillo, el volumen o el idioma del juego. 
A su vez, permitirá al usuario guardar la configuración o regresarla a su estado por defecto. 

Está relacionada con la clase ***Usuario*** pues es esta la que tiene el método para configurar el juego. 

Esta clase abarca los siguientes requerimientos: 
- RF-012: El juego contará con un apartado de configuraciones donde podrá modificar el volumen de la música, el nivel del sonido, el idioma, etc.
- RF-018: El juego debe incluir una opción para restablecer la configuración predeterminada en el menú de ajustes, permitiendo al usuario volver a los valores originales de sonido y brillo fácilmente.

## Mapas 

La clase ***Mapas*** es la que ofrece los distintos "niveles" disponibles en el juego, en los que se encuentran las rutas en las que se desarrollará la jugabilidad. 
Esta clase incluye el nombre de los mapas, el conjunto de rutas y la música que se reproducirá a la hora de jugar. Se le permite al usuario desbloquear nuevos mapas para avanzar en el juego, seleccionarlos y cambiar la música. 

La clase ***Mapas*** está relacionada con las clases ***Perfil*** y ***Rutas***. La clase **Perfil** almacenará el progreso de desbloqueo de mapas. La clase **Rutas** se relaciona pues las rutas que navegarán los camiones están dentro de cada mapa, también pudiendo modificar el número. 

Esta clase abarca los siguientes requerimientos:
- RF-007: El usuario podrá seleccionar entre distintas zonas del mapa para completar rutas, obteniendo recompensas o puntos de experiencia al finalizar con éxito.
- RF-013: El juego contará con música y efectos de sonido que se reproduciran durante su partida.
- RF-023: Los mapas deben tener un nombre para su identifación, cada mapa debe tener rutas y un límite para ello, así como música de ambientación. Los mapas dependerán del nivel del perfil, mientras se suba de nivel, se desbloquearán los mapas.

## Rutas 

La clase ***Rutas*** es aquella que incluye información relevante sobre las rutas en las que se desarrolla el juego. Esto incluye su nombre, distancia, límite de camiones, estado (abierta o cerrada) y horario. También se incluye un sistema de recompensas por ruta. 

La clase ***Rutas*** está relacionada con las tres clases ***Mapas***, ***Pasajero*** y ***Camiones***. La forma en la que la relación funciona es la siguiente: las rutas están dentro de los mapas, los pasajeros estarán esperando en cada ruta y los camiones navegaran estas mismas para transportar a los pasajeros. 

Esta clase abarca los siguientes requerimientos:
- RF-007: El usuario podrá seleccionar entre distintas zonas del mapa para completar rutas, obteniendo recompensas o puntos de experiencia al finalizar con éxito.
- RF-009: El programa contara con un sistema de horario interno de 24 horas para los niveles, siendo 1 hora en el juego equivalente a 30 segundos en la vida real, es decir que un dia en el juego consta de 12 minutos en la vida real
- RF-010: El programa mostrara un apartado llamado Tienda en el cual se podra comprar los diferentes vehiculos, usando las monedas recolectadas en los niveles. Se le mostrará al usuario los camiones, pero solo podrá comprar los camiones a los que tenga acceso por su nivel.
- RF-021: Las rutas tendrán una distancia (cuánto recorre esa ruta), un nombre, horario, paradas, camiones y de ellas se obtendran monedas. Cada que ingrese un pasajero obtendrá monedas a través de la tarifa y las rutas tienen un límite de camiones.

## Pasajero

La clase ***Pasajero*** incluye a los personajes no jugables que esperarán en las ruyas y sobre los que se revuelve la mécanica de juego principal. Cuentan con distintas acciones como subir o bajar de los camiones y esperar en rutas especificas. 

La clase ***Pasajero*** se encuentra relacionada con las clases ***Rutas*** y ***Camiones***. La relación se encuentra principalmente en los métodos disponibles para el **Pasajero**, como subirse al camión o esperar en una ruta diferente. Esta clase también cuenta con subclases nombradas **PasajeroDiscapacitado**, **PasajeroNiño** y **PasajeroAdulto**, las cuales heredan la información de la clase **Pasajero** e incluyen una tarifa individual para cada una. 

Esta clase abarca los siguientes requerimientos: 
- RF-022: Los pasajeros serán NPCs y harán uso de los camiones, estos pueden ser de diferentes tipos, por ejemplo, discapacitado, estudiante o general. Dependiendo del tipo, tendrá una tarifa diferente en el camióm. Cada pasajero tendrá una ruta, destino y parada en concreto.

## Camiones

La clase ***Camiones*** es una de las principales clases dentro del juego. Estos recorren las rutas en busca de pasajeros y así completar cada mapa con un índice de satisfacción suficiente. El usuario interactuará con esta clase mediante la asignación de rutas para su recorrido, y dichos camiones podrán interactuar con la clase ***Pasajero*** deteniendose en las paradas de cada ruta. 

La clase ***Camiones*** está relacionada con las clases ***Rutas***, ***Pasajeros*** y ***Tienda*** y ***Perfil*** . Los camiones recorreran las rutas en busca de pasajeros, y con los métodos definidos para la clase completarán los niveles según la designación del usuario. La clase también cuenta con otras tres subclases nombradas **CamiónEléctrico**, **CamiónBásico** y **CamiónHíbrido**, heredando los atributos de la clase **Camiones** además de tener un atributo de tipo de Energía cada uno.

Esta clase abarca los siguientes requerimientos: 
- RF-020: El juego debe tener diferentes tipos de camiones, por ejemplo, a gasolina, eléctricos, híbridos, etc. Cada tipo de camión consumirá una cantidad de energía, tendrá una velocidad específica y un límite de capacidad.

## Tienda 

La clase ***Tienda*** se refiere a uno de los apartados tocados en la clase [Interfaz](#interfaz). Esta clase permitirá al usuario comprar distintos camiones con las monedas obtenidas por completar las distintas rutas en los mapas seleccionados. 

La clase ***Tienda*** está relacionada con la clase ***Camiones***. Este apartado del juego ofrecerá camiones con distintos precios, usando la moneda obtenida de manera gratuita, al jugador para ir desbloqueandolos, los cuales luego se registrarán en el perfil para indicar el progreso.

Esta clase abarca los siguientes requerimientos: 
- RF-006: El programa debe incluir un sistema de recompensas que permita a los usuarios obtener monedas o puntos por completar rutas. Estos puntos podrán ser usados para desbloquear nuevas zonas o vehículos.
- RF-010: El programa mostrara un apartado llamado Tienda en el cual se podra comprar los diferentes vehiculos, usando las monedas recolectadas en los niveles. Se le mostrará al usuario los camiones, pero solo podrá comprar los camiones a los que tenga acceso por su nivel.


