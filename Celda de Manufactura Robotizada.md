# Celda de Manufactura Robotizada

Para agilizar la producción de la planta, se plantea una celda robótica, en la cual un brazo robótico alimentará tornos CNC, fresadoras CNC y talladoras para complementar el trabajo de los operarios y lograr la fabricación de las piezas necesarias para cumplir con la producción. 

## Tipo de celda robótica

Será una celda con robot, ya que la operación principal será realizada por las diferentes máquinas que se encuentren en la celda. El robot alimentará las máquinas y en caso de que cuando termine la operación, la maquina de la operación siguiente ya esté disponible, la alimente, y en caso de que no, que se transporten para que operarios sigan con el maquinado de la pieza. El robot tendrá la posibilidad de colocar las piezas en una banda transportadora, que permitirá que la pieza llegué cerca de las estaciones de trabajo, o al almacén, para disminuir el tiempo que toma el transporte de las piezas. Se posicionarán almacenes en la celda para que disponga de suficientes piezas para iniciar su maquinado. Se llenarán los almacenes al inicio de cada turno, antes de que se ponga en funcionamiento la celda. 

(imagen celda con robot)

## Elementos de la celda robótica

La celda contará con el robot y su respectivo controlador, el cual conectará con el PLC por medio de ethernet, para recibir las señales necesarias para realizar la alimentación de los tornos CNC, las fresadoras CNC y la talladoras. Tendrá almacenes para las piezas a maquinar y contará con bandas transportadoras. La celda no necesitará la intervención de operarios para la producción, pero sí para mantenimiento y el llenado de almacenes. Se plantea un layout en U, con el robot en el centro para que pueda alcanzar a realizar la recogida de las piezas y colocarlas en la máquina que realizará el proceso. 

## Evaluación de riesgo y medidas de seguridad

Peligros que se pueden presentar en la celda son de atrapamiento y corte por parte de las bandas transportadoras y las máquinas presentes en la celda, aplastamiento por parte del movimiento del brazo robótico, . Al tener elementos que funcionan con electricidad, implica también un peligro eléctrico. Finalmente, ya que los operarios deben mover piezas dentro de la celda, hay presente un peligro ergonómico. 
Para la evaluación de los riesgos, se utiliza el método Hazard Rating Number (HRN)

**Frecuencia de exposición**

Debido a que se deben realizar labores de alistamiento todos los días, pero no habrán operarios en la celda cuando está esté funcionando,  la frecuencia de exposición se determina como diaria, lo que da un valor FE=2.5

**Posibilidad de ocurrencia**

Corte y atrapamiento: ya que se plantea que las maquinas no sean capaces de funcionar en los momentos en los que se encuentren operarios en la celda, y debido al uniforme de los operarios, es improbable que los atrapen las bandas transportadoras, se determina la posibilidad de ocurrencia como muy improbable, y se le asigna un valor LO=1.

Aplastamiento: debido a que el brazo robótico no debería poder operar mientras haya operarios en la celda, se asigna una posibilidad de ocurrencia improbable y se asigna un valor LO=1.5.

Electricidad: no se tendrán conexiones descubiertas en la celda, pero es posible que daños imprevistos en cables puedan generar un accidente. Debido a que se trabajará con electricidad unicamente en las operaciones de mantenimiento, la posibilidad de ocurrencia se determina como improbable y se le asigna un valor LO=1.5.

**Número de personas**

Para labores de alistamiento y mantenimiento, se plantea la intervención de 2 operarios, po lo que se le asigna un valor NP=2.

**Severidad de posbible lesión**

- Corte y atrapamiento: debido al tipo de maquinas utilizadas, la severidad de la lesión podría llegar a ser "pérdidad de una extremidad" o comparable, por lo que se le asigna un valor DPH=6.

- Aplastamiento: debido a la naturaleza de los robots, el robot podría causar facilmente la muerte de un operario, por lo que se le asigna un valor DPH=15.

- Electricidad:  adfasdfas

Ahora, utilizando la formula HRN = NP x FE x LO x DPH, podemos asignar un valor númerico a cada uno de los riesgos.

- Corte y atrapamiento: HRN = 1 x 2.5 x 1 x 6 = 15

- Aplastamiento: HRN = 1 x 2.5 x 1.5 x 15 = 93.75

- Electricidad: HRN = 1 x 2.5 x 1.5 x DPH = ???

De esta manera, se clasifican los riesgos de corte y atrapamiento como "bajo, pero posible", el riesgo de aplastamiento como "alto", y el riesgo electrico como "por definir".

Como respuesta a lo anterior, se implementarán medidas de seguridad. La celda estará encerrada por una cerca para evitar el paso de operarios por el área de trabajo del robot. En respuesta al riesgo alto de aplastamiento, se plantea que el robot de la celda no pueda iniciar su funcionamiento mientras que la celda esté abierta, y para evitar accidentes, que solo pueda operar cuando esté cerrada la celda, y posteriormente, se pulsen dos botones, separados lo suficiente para que se requiera de 2 personas para pulsarlos simultaneamente. Se requerirá que los operarios entren con los equipos de protección personal y se instalará la señalización necesaria para indicar los peligros de corte y atrapamiento. 


