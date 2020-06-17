Manual de uso para el programa de Aprendizaje por Refuerzo, realizado por Pedro Biedma Fresno y Miguel Yanes Ariza.

-------------------------------------------------------------------------------------------------------------------
1. MODULOS USADOS Y NECESARIOS PARA LA EJECUCIÓN DEL PROGRAMA

La interfaz de usuario ha sido programada mediante los modulos:
	1. Tkinter para la creación de las ventanas.
	2. Matplotlib para las gráficas de rendimientos.
	3. Networkx para los grafos donde se muestran los recorridos tanto de entrenamiento como resultados finales.

Todos los módulos deberán ser instalados previamente a la ejecución del programa.
-------------------------------------------------------------------------------------------------------------------
2. CONFIGURACIÓN Y OPCIONES

Cuando iniciamos el programa nos encontramos una ventana llamada Aprendizaje por Refuerzo, en esta ventana se presentan las principales opciones de 
configuración.

	1. Número de Filas y Numero de Columnas: Asignará el tamaño de la matriz que generaremos. Deben de ser números enteros positivos y encontrarse en el rango de la matriz (entre 0 y MxN-1), de lo contrario aparecerá un mensaje de error.
	Se recomienda elegir matrices menores de 5x5 ya que una superior hace que la matriz Q y R no se vean completamentes mediantes la interfaz de usuario. En ese caso se 
	podrán observar los cambios por la salida del notebook.
	2. Posición de inicio: Donde comienza el agente su recorrido hacia el objetivo cuando se finalizan los entrenamientos y se quiere probar el recorrido. Debe de ser un numero entero que aparezca dentro de la matriz.
	3. Objetivo: Donde tiene que llegar el agente al final de su recorrido. Debe de ser un numero entero que aparezca dentro de la matriz, y no debe cambiarse después de generar la matriz R.
	4. Valor Gamma: Valor entre 0 y 1 usado en el algoritmo de entrenamiento.
	5. Número de Iteraciones: Iteraciones dentro del entranamiento.
	6. Valores de Epsilon y Alpha: Valor entre 0 y 1 usado en el algoritmo de entrenamiento alternativo

Al iniciar el programa todos estos valores serán previamente inicializados aunque el usuario pueda configurarlos a su antojo.
--------------------------------------------------------------------------------------------------------------------
3. INSTRUCCIONES DE USO DEL PROGRAMA

	1. Iniciaremos el programa y configuraremos las opciones comentadas en la entrada 2 de esta guía.
	2. Una vez configurados, pulsamos el botón "Generar Matriz", esto hará que aparezca en pantalla una matriz de entradas de números de las dimensiones previamente seleccionadas.
	En esta matriz podemos cambiar las posiciones de los números, siempre y cuando sean números enteros positivos. Los valores de números no se podrán repetir y el rango posible
	de números es de 0 a z, siendo z: (M x N)-1 (dimensión de la matriz).
	Existe la opción de indicar que una determinada casilla de la matriz esté inhabilitada para que el agente pase por ella, si queremos esto tendremos que añadir "T," sin las comillas
	antes del número de la casilla. Es decir si queremos marcar la casilla 2 como trampa, en la casilla donde está el 2 tendrá que aparecer escrito T,2.
	De la misma manera podemos marcar una casilla como bonificación. Si quisiéramos que el agente tenga interés en pasar por una determinada casilla, por ejemplo la 3,
	escribiremos B,3 en la casilla donde aparece el 3.
	3. Cuando hayamos configurado nuestra matriz, pulsamos el botón "Generar Q y R", el cual hará que aparezca en pantalla la matriz Q y R.
	4. Empezamos ahora nuestra fase de entrenamiento de la matriz. Comenzaremos pulsando "Entrenar Matriz".
	5. Cada vez que pulsemos "Entrenar Matriz" o "Entrenamiento alternativo" nos aparecerán dos nuevas ventanas. Una con los rendimientos de cada episodio del entrenamiento y otra
	con el grafo que detalla el camino recorrido en el entrenamiento. Se recomienda ir cerrando estas ventanas antes de volver a pulsar Entrenar Matriz de lo contrario iremos almacenando
	distintas ventanas que dificultará el seguimiento de los resultados del programa.
	6. Pulsaremos cuantas veces queramos en Entrenar Matriz, se recomienda hacerlo repetidas veces hasta que aparezcan las primeras modificaciones en la matriz Q antes de pulsar el botón
	de "Recorrer tablero".
	7. Durante los pasos 4, 5 y 6 podemos modificar el número de iteraciones, los valores gamma, epsilon y alpha. El valor epsilon disminiuye automáticamente en cada entrenamiento porque se multiplica por alpha, de modo que si el usuario ve que ha alcanzado valores demasiado bajos que están dificultando el entrenamiento, puede volver a subirlo.
	8. Cuando consideremos que la matriz está lo suficientemente entrenada pulsaremos "Recorrer tablero". Si la matriz no ha sido entrenada lo suficiente nos aparecerá un mensaje de error.
	Si la matriz ha sido entrenada lo suficiente aparecerá un grafo que muestra el recorrido que debe de hacer el agente desde la posición inicio hasta la posición objetivo. 

Indistintamente de los datos proporcionados por la interfaz de usuario se recomienda al usuario observar las salidas del notebook para obtener más datos en cada proceso del programa.

En el caso que tras la instrucción 8 no obtengamos el camino más corto posible, tenemos la posibilidad volver entrenar la matriz para que finalmente al pulsar "Recorrer tablero"
nos aparezca el camino más corto.
--------------------------------------------------------------------------------------------------------------------
