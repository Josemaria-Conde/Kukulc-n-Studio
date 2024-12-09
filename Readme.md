<h1 align="center">
Kukulc-n-Studio
</h1>
<div align="center">
Proyect FIS.

</div>

<a name="top"></a>

# Integrantes

- Josemaría Conde Chabarría
- José Luis Basulto Cámara
- Mauricio Antonio De lázaro Lara
- Christopher May Paat
- Juan Angel Canché Góngora
- Joel Humberto Basto Chavarria
- Oswaldo Castillo Machado

# Introducción

**Propósito**

Su propósito es ser un servicio de entretenimiento para sus jugadores. El sistema de transporte Va y Ven en la ciudad de Mérida Yucatán es muy conocido y querido por la ciudadanía, hoy en día existen muchos videojuegos que tienen el concepto del Va y Ven como principal atractivo. Hasta el momento los juegos que se han lanzado son principalmente del género "simulador" donde el usuario simula ser conductor del vehículo y recorre las calles de Mérida. Este proyecto ofrece un estilo diferente de jugabilidad, que busca satisfacer a otro tipo de jugadores los cuales se inclinan por el género de administración y estrategia.

**Convenciones del documento** 
Convención | Descripción 
---------- | :--------- | 
Las palabras grandes en blanco | Son títulos. | 
Las palabras de tamaño normal con sombreado  | Son subtítulos.  | 
RF-000   | Hace referencia a un requerimiento funcional y en qué orden está.   | 
RNF-000    | Hace referencia a un requerimiento no funcional y en qué orden está.    |
NPC| Personaje no jugable. | 
UML | Lenguaje Unificado de Modelado. | 
Interfaz | Representación de la interacción humano-máquina. | 

**Audiencia objetivo y sugerencias de lectura**

Este documento está dirigido a desarrolladores involucrados en la creación del videojuego de administración y estrategia basado en el sistema de transporte metropolitano Va y Ven, así como a desarrolladores externos que deseen conocer más sobre el proyecto. Además, también está destinado al público en general que busque una comprensión más profunda de las características y objetivos del juego. Para los desarrolladores se sugiere leer la parte de requerimientos y diagramas UML y C4, para saber sobre la arquitectura y funcionamiento del videojuego. Para el público en general, leer este apartado de introducción y requerimientos.

**Objetivos**
- Mostrar una interfaz de usario intuitiva.
- Registrarse e iniciar sesión.
- Tener las funciones base de toda aplicación como: Botones de reanudar, pausar, quitar sonido, configuración, perfil, etc.
- Crear, eliminar y actualizar perfiles de usuario.
- Mostrar los mapas.
- Mostrar las rutas.
- Reproducir de ambientación.
- Mostrar y usar los diferentes tipos de transporte (camiones).
- Mostrar los NPCs y que puedan subir y bajar del camión.

**Alcance del proyecto**

**Tareas(elementos dentro del alcance)**

- Gestión de rutas: Los jugadores podrán tomar decisiones sobre la asignación y optimización de las rutas del sistema Va y Ven, asegurando que las unidades de transporte funcionen de manera eficiente y satisfagan las necesidades de los personajes no jugables (NPCs) durante cada nivel.
- Gestión de camiones: El juego incluirá diferentes tipos de camiones los cuales se irán desbloqueando mientras se sube de nivel, cada unidad tendrá una velocidad específica, una capacidad de personas y cierta energía para funcionar.
- Interacción de pasajeros: Los pasajeros que serán NPCs servirán como método de validación para la efectividad de las rutas y las unidades que se estén usando, habrá diferentes tipos de pasajeros y cada uno tendrá una ruta específica. Además, contarán con las acciones de subir y bajar del camión.
- Progresión por niveles: Los jugadores comenzarán en el nivel 1 del juego, mientras vayan avanzando iran subiendo de nivel y desbloquenado diferentes mapas, camiones, rutas y la dificultad irá incrementando, por ejemplo, en la cantidad de rutas que administrar y desafíos relacionados con la satisfacción de los pasajeros. 
- Interfaz de usuario: El juego contará con una interfaz de usario intuitiva para que al jugador le sea fácil de interactuar con la aplicación y pueda realizar las actividades de manera satisfactoria. Los jugadores podrán visualizar y gestionar las rutas, mapas, camiones, los niveles de satisfacción de los NPCs a través de paneles interactivos y gráficos y usar las funciones por defecto de un videojuego tales como pausar, reanudar, configurar la aplicación, quitar el sonido, registrarse, iniciar sesión, crear perfil, entre otras.

**Limitaciones**
- En esta primera versión el juego no contará con modo multijugador en línea.
- El diseño del mapa del juego debe estar inspirado unicamente en la ciudad de Mérida Yucatán.
- En esta fase inicial el juego solo será compatible con el sistema operativo android.
- La interacción del jugador con los NPCs será solo para saber sobre su satisfacción, no tendrán dialogos.
- El juego esta pensado para que sea en una perspectiva 2D.

**Referencias** 
- Lifeparticle. (s. f.). GitHub - lifeparticle/Markdown-Cheatsheet: 🔖  The Ultimate Markdown Cheatsheet. GitHub. Recuperado el 4 de octubre de 2024, de https://github.com/lifeparticle/Markdown-Cheatsheet?tab=readme-ov-file#tables
-  StackEdit. (s/f). Stackedit.io. Recuperado el 4 de octubre de 2024, de https://stackedit.io/app
- Flowchart maker & online diagram software. (s/f). Diagrams.net. Recuperado el 4 de octubre de 2024, de https://app.diagrams.net/
- O365devx. (2023). Convenciones de documento (VBA). Microsoft Learn. https://learn.microsoft.com/es-es/office/vba/language/concepts/getting-started/document-conventions-visual-basic-for-applications
- Atlassian. (s/f). Alcance del proyecto: cómo puede ahorrar tiempo la gestión del alcance del proyecto. Atlassian. Recuperado el 4 de octubre de 2024, de https://www.atlassian.com/es/work-management/project-management/project-
- Blog - Create UML class diagrams. (s. f.). https://www.drawio.com/blog/uml-class-diagrams
- Blog - Create C4 models and diagrams. (s. f.). https://www.drawio.com/blog/c4-modelling
- AJ&Smart. (2020). Figma UI Design Tutorial: Get Started in Just 24 Minutes! [Vídeo]. YouTube. https://www.youtube.com/watch?v=FTFaQWZBqQ8
- Oliver Puente. (2022). Figma tutorial para principiantes | 👋Aprende Diseño Web UI de manera simple a través de Figma [Vídeo]. YouTube. https://www.youtube.com/watch?v=bIK7PIdlLTU

# Descripción del proyecto

**Descripción general** 

El videojuego pertenece al género de administración y estrategia, en el que se gestionan las rutas del sistema de transporte metropolitano "Va y Ven". El jugador toma decisiones sobre el funcionamiento de las rutas y las unidades de transporte con el objetivo de mantener la mayor satisfacción posible de los personajes no jugables (NPCs) durante los niveles o fases del juego. Este sistema se centra en la toma de decisiones estratégicas, permitiendo al jugador utilizar la divisa de satisfacción generada por los NPCs para mejorar su estrategia. Las decisiones del jugador impactarán directamente en el funcionamiento de las rutas, la eficiencia del transporte y la experiencia general de los pasajeros virtuales. El proyecto busca ofrecer una experiencia de juego que combine la complejidad de la gestión de un sistema de transporte con una jugabilidad accesible y entretenida.

**Perspectiva del producto**

El videojuego está diseñado para personas de todas las edades, especialmente para aquellos que buscan una actividad entretenida para ocupar su tiempo libre y disminuir el aburrimiento. Esto incluye tanto a niños como a adultos que se encuentran en situaciones donde necesitan una distracción ligera pero estimulante.

El producto no solo ofrece entretenimiento, sino que también brinda la oportunidad de desarrollar habilidades clave de manera intuitiva. Al tomar decisiones estratégicas relacionadas con la gestión de rutas y el funcionamiento del sistema de transporte, los jugadores mejoran sus capacidades de organización, planificación y resolución de problemas.

El enfoque principal es proporcionar una experiencia accesible y relajante, que permita a los jugadores disfrutar sin necesidad de una curva de aprendizaje pronunciada, al mismo tiempo que se sienten recompensados por sus elecciones inteligentes. De este modo, el juego equilibra la diversión y el desarrollo de habilidades, contribuyendo al fortalecimiento cognitivo del usuario mientras combate el aburrimiento.

**Características del producto**

**Clases y características del usuario**

**Ambiente de operación**

**Restricciones de diseño e implementación**

**Documentación del usario**

**Suposiciones y dependencias**


# Requerimientos

# Funcionales

- RF-001: El usurio puede iniciar sesión con un usuario y contraseña. De esta manera podremos ayudar a la creación y personalización de perfiles y a la seguridad de la cuenta.

- RF-002: El juego no contendrá sonidos o imágenes capaces de asustar a los más pequeños. Tampoco contendrá lenguaje inapropiado, es decir, lo que se mostrará dentro de la aplicación deberá contener un lenguaje sano para todas las edades, esto involucra: texto en la interfaz, texto de los personajes no jugables (NPCs), etc.

- RF-003: El programa debe de permitir a los usuarios crear un perfil local, en donde, se guarde el progreso, tanto como logros y puntuaciones previamente obtenidas al jugar.

- RF-004: Contará con un algoritmo que modifique la complejidad y diseño del nivel, para que este sea más inmersivo y menos repetitivo.  Funcionando en base a como se desempeñe el usuario en el transcurso del programa.

- RF-005: El juego debe permitir al usuario pausar y reanudar la partida en cualquier momento con solo presionar un botón en la pantalla.

- RF-006: El programa debe incluir un sistema de recompensas que permita a los usuarios obtener monedas o puntos por completar rutas. Estos puntos podrán ser usados para desbloquear nuevas zonas o vehículos.

- RF-007: El usuario podrá seleccionar entre distintas zonas del mapa para completar rutas, obteniendo recompensas o puntos de experiencia al finalizar con éxito.  

- RF-008: El juego debe permitir a los jugadores comparar sus puntuaciones y tiempos con los de otros usuarios, mostrando un ranking global, por región o amigos.

- RF-009: El programa contara con un sistema de horario interno de 24 horas para los niveles, siendo 1 hora en el juego equivalente a 30 segundos en la vida real, es decir que un dia en el juego consta de 12 minutos en la vida real

- RF-010: El programa mostrara un apartado llamado Tienda en el cual se podra comprar los diferentes vehiculos, usando las monedas recolectadas en los niveles. Se le mostrará al usuario los camiones, pero solo podrá comprar los camiones a los que tenga acceso por su nivel.

- RF-011: El juego tendrá una interfaz gráfica que se encargará de todo lo visual, mostrar el perfil, los mapas, rutas en los mapas, los camiones que estan en las rutas, los pasajeros, la tienda, una barra de busqueda, etc. 

- RF-012: El juego contará con un apartado de configuraciones donde podrá modificar el volumen de la música, el nivel del sonido, el idioma, etc.

- RF-013: El juego contará con música y efectos de sonido que se reproduciran durante su partida.  
 
- RF-014: El usuario podrá agregar como amigos a otros usuarios que tengan creado un perfil dentro del juego.

- RF-015: El programa permitira cambiar el color del fondo entre blanco y negro.

- RF-016: El juego contara con un apartado donde se puedan consultar las estadisticas del jugador (horas jugadas, monedas recolectadas, cantidad de rutas, camiones, etc.)

- RF-017: El juego debe permitir al usuario reiniciar un nivel en cualquier momento desde el menú de pausa, para que pueda intentarlo de nuevo sin necesidad de salir al menú principal.

- RF-018: El juego debe incluir una opción para restablecer la configuración predeterminada en el menú de ajustes, permitiendo al usuario volver a los valores originales de sonido y brillo fácilmente.

- RF-019: En caso de no contar con una cuenta, el usario deberá registrarse para así poder incicar sesión y acceder completamente a las funciones.

- RF-020: El juego debe tener diferentes tipos de camiones, por ejemplo, a gasolina, eléctricos, híbridos, etc.
Cada tipo de camión consumirá una cantidad de energía, tendrá una velocidad específica y un límite de capacidad.

- RF-021: Las rutas tendrán una distancia (cuánto recorre esa ruta), un nombre, horario, paradas, camiones, color y de ellas se obtendran monedas. Cada que ingrese un pasajero obtendrá monedas a través de la tarifa y las rutas tienen un límite de camiones.

- RF-022: Los pasajeros serán NPCs y harán uso de los camiones, estos pueden ser de diferentes tipos, por ejemplo, discapacitado, estudiante o general. Dependiendo del tipo, tendrá una tarifa diferente en el camióm. Cada pasajero tendrá una ruta, destino y parada en concreto.

- RF-023: Los mapas deben tener un nombre para su identifación, cada mapa debe tener rutas y un límite para ello, así como música de ambientación. Los mapas dependerán del nivel del perfil, mientras se suba de nivel, se desbloquearán los mapas.

- RF-024: El color base de la interfaz del juego debe ser azul "1E90FF" para el modo normal y para el modo oscuro debe ser azul "1A5276".

- RF-025: El programa debe incluir una pantalla de carga al iniciar.

- RF-026: El programa debe incluir un botón de "Salir" en el menú principal. 

- RF-027: El programa debe incluir soporte para dos idiomas principales, español e inglés.

# No funcionales

- RNF-001: La clasificación del juego debe ser para todas las edades "E".

- RNF-002: El programa debe de ser capaz de soportar elementos del juego mostrados simultáneamente, en este caso, 26 objetos (camiones) sin que el rendimiento sea por debajo de 60 FPS.

- RNF-004: El programa debe ejecutarse correctamente en dispositivos móviles con procesador Qualcomm Snapdragon 765, al menos 2 GB de RAM y un mínimo de 350 MB de almacenamiento disponible.

- RNF-005: El tiempo de carga inicial del juego no debe exceder los 5 segundos en dispositivos que cumplan con los requisitos mínimos

- RNF-006: La información del usuario, como credenciales y progreso en el juego, debe estar protegida mediante encriptación, garantizando la seguridad y privacidad.

- RNF-007: El programa debe adaptarse a diferentes tamaños de pantalla y resoluciones, garantizando una experiencia optima tanto en smarphones de gama baja como en tablets de mayor capacidad.

- RNF-008: El programa contara con actualizaciones en un plazo de tiempo medio, siendo aproximadamente de 1 a 3 meses, variando en la cantidad cambios que se hagan, como la solucion a futuros errores que se puedan presentar como nuevo contenido para el juego.

- RNF-09: La interfaz gráfica de usuario deberá estar adaptada para uso táctil. 

- RNF-010: El juego será compatible con versiones de Sistema Operativo Android 6.0 y posteriores.

- RNF-011: El juego sera capa de escalar copn la pantalla del sipositivo para evitar franjas negras en los bordes.

- Rnf-012: El juego no debera de necesitar internet para inicalizar.

- RNF-013: El juego debe poder activar o desactivar la música y efectos de sonido desde el menú de configuración.

- RNF-014: El juego debe permitir al usuario ajustar el brillo de la pantalla dentro de la aplicación para mejorar la visibilidad en diferentes condiciones de luz. 
</div>
