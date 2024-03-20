<pre>

	<p align=center>

Tecnológico Nacional de México
Instituto Tecnológico de Tijuana

Departamento de Sistemas y Computación
Ingeniería en Sistemas Computacionales

Semestre:
Febrero - Junio 2024

Materia:
Lenguajes de interfaz

Docente:
M.C. Rene Solis Reyes 

Unidad:
1

Título del trabajo:
Depuración de programas en Assembly con GDB
......

Estudiantes:
Sanchez Tolentino Gerardo Julian 	21212048
Morales Lopez Billi Joel 		21212002
Hernandez Vazquez Cristian		21211954
Escalante Hernandez Kevin Ulises	21211937
Fragoso Arellano Jorge Yahir		21211943
.......

	</p>

</pre>

<pre>

	<p align=left>


Conceptos básicos de GDB

	</p>

</pre>

<pre>

	<p align=left>


Breakpoints

<p align=center>
¿Que es un  breakpoint?
<p align=left>
Se refiere a un punto específico en el código de un programa donde la ejecución se pausa temporalmente 
para permitir a los programadores examinar el estado del programa en ese momento. 
Los breakpoints son herramientas muy útiles para depurar código y encontrar errores.

Cuando se establece un breakpoint en un entorno de desarrollo integrado (IDE) o en un depurador, 
el programa se detiene cuando alcanza esa línea de código específica. Esto permite a los desarrolladores 
inspeccionar las variables, ejecutar instrucciones paso a paso y examinar el flujo de ejecución del programa 
para identificar problemas y corregir errores. Una vez que se han resuelto los problemas, los breakpoints 
se pueden eliminar para permitir que el programa se ejecute normalmente.

<p align=center>
¿Cuando se utiliza un breakpoint?
<p align=left>

Identificar errores: 
Cuando un programa no funciona como se espera, los desarrolladores pueden usar breakpoints para detener la 
ejecución del programa en puntos específicos y examinar el estado del programa para identificar errores.
	
Analizar el flujo de ejecución:
Los breakpoints permiten a los desarrolladores observar el flujo de ejecución del programa. Pueden ver en 
qué punto se ejecuta una determinada sección de código y cómo afecta al estado del programa.

Inspeccionar variables:
Cuando se alcanza un breakpoint, los desarrolladores pueden examinar el valor de las variables en ese momento. 
Esto es útil para detectar valores inesperados o incorrectos que pueden estar causando problemas en el programa.

Entender el comportamiento del código:
Los breakpoints también se pueden utilizar para comprender cómo funciona un programa. Al detener la ejecución 
en diferentes puntos, los desarrolladores pueden ver qué partes del código se ejecutan en diferentes situaciones y cómo interactúan entre sí.

<p align=center>
Ventajas
<p align=left>
Facilita la depuración: 
Los breakpoints permiten detener la ejecución del programa en puntos específicos, lo que facilita la identificación 
y corrección de errores al proporcionar a los desarrolladores la capacidad de examinar el estado del programa en ese momento.

Ahorra tiempo:
Al detener la ejecución en puntos críticos del código, los desarrolladores pueden ahorrar tiempo al no tener que 
revisar todo el programa en busca de errores. Esto acelera el proceso de depuración y ayuda a resolver problemas de manera más eficiente.
	
Permite el análisis detallado:
Los breakpoints ofrecen a los desarrolladores la capacidad de inspeccionar variables, ejecutar instrucciones paso a paso y analizar 
el flujo de ejecución del programa. Esto les permite comprender mejor cómo funciona el código y cómo interactúan diferentes partes del programa.
	

<p align=center>
Desventajas
<p align=left>
Puede ralentizar la ejecución:
El uso excesivo de breakpoints puede ralentizar la ejecución del programa, especialmente en aplicaciones grandes o complejas. 
Esto puede afectar negativamente la productividad del desarrollador y el rendimiento del programa.

Posible dependencia excesiva:
Algunos desarrolladores pueden volverse dependientes de los breakpoints para depurar su código, lo que puede dificultar el 
desarrollo de habilidades de depuración más avanzadas y comprensión del código.

Riesgo de introducir nuevos errores:
Al agregar o modificar breakpoints durante el proceso de depuración, existe el riesgo de introducir nuevos errores en el código. 
Por ejemplo, olvidar eliminar un breakpoint después de su uso puede causar problemas en la ejecución del programa en producción.


	</p>

</pre>
<pre>

	<p align=left>


Inspección de registros y memoria

	</p>

</pre>
<pre>

	<p align=left>


Seguimiento de ejecución

<p align=center>
¿Que es seguimiento de ejecución?
<p align=left>
El "seguimiento de ejecución" es una técnica de depuración que permite observar y registrar los pasos que sigue un programa
mientras se ejecuta, mostrando el flujo exacto de instrucciones en el procesador.

<p align=center>
¿Como se utiliza?
<p align=left>
Step y Next:
Estos comandos son fundamentales en el seguimiento de ejecución. step ejecuta el programa línea por línea, 
entrando en las funciones. next también ejecuta línea por línea, pero trata las funciones como una sola unidad de ejecución, no entrando en ellas.

Watchpoints:
Son puntos de interrupción basados en el cambio de valor de una expresión o variable. Si la variable o expresión cambia, el programa se detiene, 
lo que permite ver en qué punto del código ocurre el cambio.

Conditionals:
Puedes establecer condiciones en los puntos de interrupción para que la ejecución se detenga solo cuando se cumpla una condición específica, 
lo que ayuda a focalizar la depuración en situaciones de interés particular.

Inspecting state:
Durante el seguimiento de ejecución, puedes inspeccionar y modificar el estado del programa. Esto incluye ver y cambiar el valor de las variables, 
examinar el contenido de la memoria, y ver el estado de los registros del procesador.

Control de flujo:
GDB permite controlar el flujo de ejecución del programa, lo que significa que puedes avanzar o retroceder en la ejecución,
moverte a diferentes puntos del código, y ejecutar código condicionalmente.
<p align=center>
¿Que importancia tiene?
<p align=left>
El seguimiento de ejecución en GDB para ensamblador ARM es de vital importancia debido a varias razones.
Aquí se detallan algunos de los aspectos más significativos:
	
	1. Comprensión detallada del flujo de ejecución
	Permite a los desarrolladores entender exactamente cómo el procesador ARM ejecuta el programa, instrucción por instrucción.
	Esto es crucial en la depuración de ensamblador, donde cada instrucción puede 
	tener un impacto significativo en el comportamiento del sistema.
	
	2. Identificación precisa de errores
	El seguimiento de ejecución facilita la localización de errores y comportamientos inesperados en el código. 
	Por ejemplo, si un programa se comporta incorrectamente o se bloquea, el seguimiento puede 
	ayudar a identificar la instrucción exacta o el conjunto de instrucciones que causan el problema.
	
	3. Optimización del rendimiento
	Al depurar a nivel de ensamblador, los desarrolladores pueden identificar cuellos de botella y optimizar secciones críticas del código para mejorar el rendimiento.
	Esto es especialmente importante en sistemas embebidos o en aplicaciones donde la eficiencia del procesador es crítica.
	
	4. Análisis de bajo nivel
	El seguimiento de ejecución en GDB permite a los desarrolladores observar el comportamiento de los registros, 
	la gestión de la memoria y la ejecución de las instrucciones a nivel de hardware. Esto es fundamental para el desarrollo de firmware,
	drivers, y sistemas operativos donde la interacción directa con el hardware es necesaria.
	
	5. Educación y aprendizaje
	Para quienes aprenden programación en ensamblador ARM o quieren entender cómo funciona el hardware a nivel de instrucciones, 
	el seguimiento de ejecución es una herramienta educativa poderosa. Facilita la 	visualización de conceptos abstractos como el flujo de control,
	manipulación de registros, y la ejecución de instrucciones.
	
	6. Resolución de problemas específicos de hardware
	En el desarrollo de software para plataformas específicas de ARM, el seguimiento de ejecución ayuda a entender cómo el programa interactúa con el hardware específico.
	Esto es esencial para diagnosticar problemas que pueden no ser evidentes a través de la depuración a nivel de código fuente.
	
	7. Automatización de pruebas
	GDB puede ser utilizado en conjunto con scripts de automatización para ejecutar pruebas repetitivas,
	permitiendo un seguimiento sistemático de la ejecución en diferentes escenarios de prueba.
	</p>

</pre>
