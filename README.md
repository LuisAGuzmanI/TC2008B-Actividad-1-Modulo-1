# TC2008B Actividad 1 Modulo 1: Barredoras
## Integrandes del equipo

* Luis Ángel Guzmán Iribe - A01741757
* Cesar Galvez - A01252177
* Antonio López Chávez - A01741741
* Sebastián Gálvez Trujillo - A01251884

Este programa tiene la función de simular un cuarto donde se coloquen "roombas" o barredoras que se muevan a través del espacio y limpien toda suciedad que se encuentren. Se importan librerías que permiten el uso de "Multiagentes" (clases con un comportamiento específico para cumplir diferentes objetivos), uso de matrices y arreglos específicos, así como "Pandas" que permiten organizar la información del programa. 

## Reglas

Las reglas de la simulación varían según el tipo de agente, siendo la clase "TileAgent" correspondiente a las celdas que rellenarán el "Grid" creado y la clase "RoombaAgent", las barredoras que limpiarán el espacio.

Características de celdas:
1. Existen valores predefinidos en el código (sección de "Ejecución del modelo") que dictan el tamaño del grid y por ende la cantidad de agentes de celdas que se crearán (Ancho * Altura = número de agentes).
2. Otros valores predefinidos permiten el cálculo de la cantidad de celdas sucias, se eligen aleatoriamente las coordenadas de estas celdas.

Reglas de celdas:
1. Solo habrá un agente de celda por cada coordenada del grid.
2. Solo puede tener un estado, sucia o limpia, cada uno con un color diferente.
3. La primer fila de celdas tiene la característica de cargar la batería de las barredoras.

Reglas de "roombas" o barredoras:
1. Tienen dos acciones, limpiar la celda donde se encuentran o moverse en una de sus posibles direcciones (todas sus celdas adyacentes).
2. Cada acción le toma un "step" o generación, es decir, no puede moverse y limpiar al mismo tiempo.
3. Cada generación reduce en "1" la batería del "roomba", ya sea que limpie o se mueva.
4. Su batería se recarga si pasan por una celda de la primera fila del "grid".
5. Al acabarse su batería, su estado pasa a "descargada", por lo que ya no puede moverse y gráficamente cambia de color.
6. Pueden convivir en la misma celda con otros "roombas", sin interferir en sus acciones.
