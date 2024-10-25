# Diagrama de clases UML por Josemaría Conde Chabarría

images/Conde UML Entidades.png

# Descripción

Las distintas entidades presentes en el juego siguen un orden casi jerárquico para el desempeño de sus roles, con el propósito de que el jugador pueda, dentro de los parámetros establecidos en los siguientes requisitos funcionales, modificar los componentes para diseñar las rutas así como los camiones que las recorrerán :
RF-007: El usuario podrá seleccionar entre distintas zonas del mapa para completar rutas, obteniendo recompensas o puntos de experiencia al finalizar con éxito.
RF-021: Las rutas tendrán una distancia (cuánto recorre esa ruta), un nombre, horario, paradas, camiones y de ellas se obtendrán monedas. Cada que ingrese un pasajero obtendrá monedas a través de la tarifa y las rutas tienen un límite de camiones.
RF-023: Los mapas deben tener un nombre para su identifación, cada mapa debe tener rutas y un límite para ello, así como música de ambientación. Los mapas dependerán del nivel del perfil, mientras se suba de nivel, se desbloquearán los mapas.

Además, los pasajeros y camiones heredaran las propiedades de la clase characther que contiene los datos de nombre, descripción e imagen representativa o “portrait” para poder ser consultados en la sección de estadística como lo indica el requisito funcional
RF-016: El juego contara con un apartado donde se puedan consultar las estadísticas del jugador (horas jugadas, monedas recolectadas, cantidad de rutas, camiones, etc.)
En adición a ello las clases pasajeros y camiones podrán ser categorizados mediante la lista de tarifas (para pasajeros) y la lista de tipos de camión (para camiones), que impactaran en los costos y las ganancias de acuerdo a los siguientes requisitos funcionales
RF-022: Los pasajeros serán NPCs y harán uso de los camiones, estos pueden ser de diferentes tipos, por ejemplo, discapacitado, estudiante o general. Dependiendo del tipo, tendrá una tarifa diferente en el camión. Cada pasajero tendrá una ruta, destino y parada en concreto.
RF-020: El juego debe tener diferentes tipos de camiones, por ejemplo, a gasolina, eléctricos, híbridos, etc. Cada tipo de camión consumirá una cantidad de energía, tendrá una velocidad específica y un límite de capacidad.
RF-006: El programa debe incluir un sistema de recompensas que permita a los usuarios obtener monedas o puntos por completar rutas. Estos puntos podrán ser usados para desbloquear nuevas zonas o vehículos.

