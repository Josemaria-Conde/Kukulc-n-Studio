# Diagrama de clases UML por José Luis Basulto Cámara

![Diagrama UML](/images/Diagrama_Fis_Basulto.drawio.png)

# Descripción

Este sistema tiene diversas clases que interactúan entre sí para gestionar un entorno donde el usuario puede controlar rutas, camiones, mapas, pasajeros y configuraciones. Cada clase tiene una función específica dentro del sistema y en conjunto permiten la creación de una experiencia compleja y detallada para el jugador.

La clase **Usuario** gestiona toda la información relacionada con los usuarios que interactúan con el sistema. Un Usuario tiene un identificador único (usuarioID), un nombre de usuario, una contraseña y una edad asociada. Además, puede tener una lista de amigos (otros usuarios) con los que puede interactuar dentro del juego o la aplicación. Las funcionalidades principales de esta clase incluyen el inicio y cierre de sesión, la posibilidad de registrarse, actualizar información personal como la contraseña y la gestión de perfiles. A través de esta clase, los usuarios pueden crear, actualizar o eliminar sus perfiles, además de añadir amigos. Se relaciona con la clase Perfil, ya que un mismo usuario puede tener muchos perfiles y en cada uno tener un avance diferente.

Cumple con los requisitos funcionales:
- RF-001: Para poder acceder completamente a las funciones, se debe iniciar sesión con un usuario y contraseña. De esta manera podremos ayudar a la creación y personalización de perfiles y a la seguridad de la cuenta.
- RF-019: En caso de no contar con una cuenta, el usario deberá registrarse para así poder incicar sesión y acceder completamente a las funciones.
- RF-014: El usuario podrá agregar como amigos a otros usuarios que tengan creado un perfil dentro del juego.

La clase **Perfil** representa la experiencia individual del jugador en el sistema. Un perfil tiene un nombre, nivel y una lista de rutas, camiones y mapas asociados que el jugador ha desbloqueado o adquirido. Además, se almacenan las monedas recogidas y el tiempo total jugado. parte de sus atributos sirven como historial o estadísticas del jugador. La clase permite actualizar el perfil, eliminarlo, acumular monedas y registrar el tiempo de juego. Para saber las rutas, camiones y mapas que tiene el perfil, esta clase se relaciona con las clases de esos mismos nombres.

Cumple con los requisitos funcioales: 
- RF-003: El programa debe de permitir a los usuarios crear un perfil local, en donde, se guarde el progreso, tanto como logros y puntuaciones previamente obtenidas al jugar.
- RF-016: El juego contara con un apartado donde se puedan consultar las estadisticas del jugador (horas jugadas, monedas recolectadas, cantidad de rutas, camiones, etc.)

La clase **Rutas** representa los caminos que los camiones seguirán en el sistema. Cada ruta tiene un identificador único, un nombre, distancia, horario y paradas específicas. Además, existe un límite de camiones que pueden circular por cada ruta. Los jugadores pueden crear nuevas rutas, actualizarlas, eliminar paradas o buscar paradas disponibles. Esta clase gestiona la relación entre los camiones y los mapas, ya que los camiones deben recorrer rutas específicas en los mapas disponibles. También en esta clase se obtendrán las monedas que se ganen en la rutas. 

Cumple con los requisitos funcionales: 
- RF-021: Las rutas tendrán una distancia (cuánto recorre esa ruta), un nombre, horario, paradas, camiones y de ellas se obtendran monedas. Cada que ingrese un pasajero obtendrá monedas a través de la tarifa y las rutas tienen un límite de camiones.
- RF-006: El programa debe incluir un sistema de recompensas que permita a los usuarios obtener monedas o puntos por completar rutas. Estos puntos podrán ser usados para desbloquear nuevas zonas o vehículos.

La clase **Camiones** hace referencia a los vehículos que el jugador administra en el juego. Cada camión tiene un identificador, un tipo específico, velocidad, capacidad de pasajeros y un nivel de energía. Los camiones pueden recorrer rutas, recoger y dejar pasajeros y asignarse a rutas específicas. Además, la clase ofrece funciones para calcular la energía consumida por los camiones en función de sus recorridos. Esta clase esta relacionada al perfil, rutas, mapas y la tienda donde los camiones pueden ser adquiridos.

Cumple con los requisitos funcionales:
- RF-020: El juego debe tener diferentes tipos de camiones, por ejemplo, a gasolina, eléctricos, híbridos, etc. Cada tipo de camión consumirá una cantidad de energía, tendrá una velocidad específica y un límite de capacidad.

La clase **Tienda** permite a los jugadores comprar y desbloquear camiones. Aquí se gestionan los camiones disponibles para compra, los requisitos de nivel que el jugador debe alcanzar para desbloquearlos y el precio de cada camión. A través de esta clase, los jugadores pueden comprar camiones nuevos y mejorar su flota para operar en las rutas del juego. Esta relacionada claramente con la clase camiones.

Cumple con los requisitos funcionales: 
- RF-010: El programa mostrara un apartado llamado Tienda en el cual se podra comprar los diferentes vehiculos, usando las monedas recolectadas en los niveles. Se le mostrará al usuario los camiones, pero solo podrá comprar los camiones a los que tenga acceso por su nivel.

La clase **Mapas** tiene que ver con los escenarios donde se crean las rutas y circulan los camiones. Cada mapa tiene un nombre, una cantidad de rutas, un límite en la cantidad de rutas que puede contener y puede tener características adicionales como un archivo de sonido asociado, lo cual sirve para ambientación del mapa. La clase permite bloquear o desbloquear mapas, agregar rutas a los mapas y asignar rutas a las áreas desbloqueadas, así como también permite gestionar la música de ambientación. Los mapas son esenciales para el funcionamiento del sistema de transporte, ya que en ellos se desarrollan todas las actividades. Para su funcionamiento esta clase se relaciona con el perfil y las rutas.

Cumple con los requisitos funcionales:
- RF-013: El juego contará con música y efectos de sonido que se reproduciran durante su partida.
- RF-023: Los mapas deben tener un nombre para su identifación, cada mapa debe tener rutas y un límite para ello, así como música de ambientación. Los mapas dependerán del nivel del perfil, mientras se suba de nivel, se desbloquearán los mapas.
- RF-007: El usuario podrá seleccionar entre distintas zonas del mapa para completar rutas, obteniendo recompensas o puntos de experiencia al finalizar con éxito.

La clase **Pasajeros** tiene que ver con personajes no jugables que utilizan las rutas y camiones gestionados por el jugador. Cada pasajero tiene un identificador, un tipo, una ruta asignada, un destino y una tarifa que paga por el viaje. Los pasajeros pueden subir y bajar de los camiones en las paradas designadas. Estos personajes añaden una capa de complejidad al juego, ya que el jugador debe gestionar las rutas y camiones de manera eficiente para transportarlos. Con ellos se obtienen las monedas y así poder usarlas para comprar camiones en la tienda.

Cumple con los requisitos funcionales: 
- RF-022: Los pasajeros serán NPCs y harán uso de los camiones, estos pueden ser de diferentes tipos, por ejemplo, discapacitado, estudiante o general. Dependiendo del tipo, tendrá una tarifa diferente en el camióm. Cada pasajero tendrá una ruta, destino y parada en concreto.

La clase **Configuración** permite personalizar la experiencia del juego para cada usuario. Aquí se gestionan las opciones de brillo de la pantalla, sonido, idioma del juego y el color de fondo. Los usuarios pueden ajustar estas configuraciones a su gusto. Además, la clase permite guardar las preferencias o cambiarlas cuando sea necesario, ofreciendo al usuario la opción de elegir entre configuraciones predeterminadas.

Cumple con los requisitos funcionales: 
- RF-012: El juego contará con un apartado de configuraciones donde podrá modificar el volumen de la música, el nivel del sonido, el idioma, etc.
- RF-015: El programa permitirá cambiar el color del fondo entre blanco, gris y negro.

La clase **Interfaz** Es la encargada de mostrar el sistema, engloba la visualización de las clases. Muestra la información al jugador, como sus perfiles, mapas, rutas, camiones, el horario y pasajeros. También permite acceder a opciones de juego como pausar, mostrar la tienda y configurar el sistema. A través de la interfaz, el jugador puede ver en pantalla toda la información relevante y realizar acciones en el sistema de manera accesible y ordenada. Por ende todas las clases estan relacionadas a esta.

Cumple con los requisitos funcionales: 
- RF-011: El juego tendrá una interfaz gráfica que se encargará de todo lo visual, mostrar el perfil, los mapas, rutas en los mapas, los camiones que estan en las rutas, los pasajeros, la tienda, etc.
- RF-005: El juego debe permitir al usuario pausar y reanudar la partida en cualquier momento con solo presionar un botón en la pantalla.
- RF-009: El programa contará con un sistema de horario interno de 24 horas para los niveles, siendo 1 hora en el juego equivalente a 30 segundos en la vida real, es decir que un dia en el juego consta de 12 minutos en la vida real