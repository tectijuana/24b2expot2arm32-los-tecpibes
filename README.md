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
<p align=center>

<p align=left>
Depuración: GDB es una herramienta utilizada para depurar programas. La depuración es el proceso de 
identificar y corregir errores en un programa de computadora.

Puntos de interrupción: GDB permite establecer puntos de interrupción en el código fuente del programa.
Cuando el programa alcanza un punto de interrupción, se detiene y el usuario puede examinar su estado.

Ejecución paso a paso: GDB permite ejecutar el programa paso a paso, 
línea por línea. Esto es útil para observar el comportamiento 
del programa y detectar posibles errores.

Inspección de variables: Con GDB, 
puedes inspeccionar el valor de las variables en 
cualquier punto del programa durante la depuración.

Backtrace (traza de llamadas): GDB proporciona una traza de llamadas, 
también conocida como backtrace, que muestra la pila de llamadas de funciones 
activas en un momento dado. Esto es útil para comprender cómo se llegó a un
determinado punto en el programa.

Modificación de variables: Además de inspeccionar variables, 
GDB también te permite modificar su valor durante la ejecución del programa.
Esto puede ser útil para probar diferentes escenarios o corregir errores en tiempo real.

Ayuda y documentación: GDB cuenta con una amplia documentación y una interfaz de ayuda integrada 
que te permite acceder a información detallada sobre sus comandos y funcionalidades.

Uso avanzado: Además de estas funciones básicas, GDB ofrece muchas características avanzadas, 
como el seguimiento de la memoria, el control de subprocesos y la depuración remota, que
pueden ser útiles para tareas de depuración más complejas.

Watchpoints (puntos de observación): GDB permite establecer watchpoints en variables específicas.
Cuando el valor de una variable cambia, GDB detiene la ejecución del programa, 
lo que puede ser útil para detectar cuándo y dónde se modifican ciertos datos.

Excepciones y señales: GDB puede manejar excepciones y señales, 
como las generadas por errores de segmentación o violaciones de acceso. 
te permite investigar la causa de estas excepciones y, en algunos casos, continuar la ejecución del programa después de su manejo.

Ejecución remota: GDB puede depurar programas que se ejecutan en sistemas
remotos a través de una conexión de red. Esto es útil cuando necesitas depurar un 
programa que se ejecuta en un entorno diferente al tuyo.

Archivo de comandos: GDB te permite crear un archivo de comandos con una secuencia de 
instrucciones para ejecutar automáticamente durante la depuración. 
Esto puede ahorrarte tiempo al automatizar tareas repetitivas o configurar el entorno de 
depuración de forma específica.

Extensibilidad: GDB es altamente extensible y puede ser personalizado
mediante el desarrollo de extensiones y scripts en lenguajes como Python.
Esto te permite adaptar GDB a tus necesidades específicas o ampliar su funcionalidad según tus requerimientos.

Depuración de programas multi-hilo: GDB es capaz de depurar
programas que hacen uso de múltiples hilos de ejecución de manera concurrente. 
Puedes inspeccionar y controlar cada hilo individualmente para entender mejor el c
omportamiento del programa.

Interfaz gráfica: Aunque GDB suele utilizarse a través de una interfaz de línea de comandos,
existen también interfaces gráficas como GDB GUI y DDD (Data Display Debugger) que 
proporcionan una experiencia de depuración visual más amigable.

</pre>
<pre>


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
en diferentes puntos, los desarrolladores pueden ver qué partes del código se ejecutan en diferentes situaciones 
y cómo interactúan entre sí.

<p align=center>
Ventajas
<p align=left>
Facilita la depuración: 
Los breakpoints permiten detener la ejecución del programa en puntos específicos, lo que facilita la
identificación y corrección de errores al proporcionar a los desarrolladores la capacidad de examinar 
el estado del programa en ese momento.

Ahorra tiempo:
Al detener la ejecución en puntos críticos del código, los desarrolladores pueden ahorrar tiempo al 
no tener que revisar todo el programa en busca de errores. Esto acelera el proceso de depuración y 
ayuda a resolver problemas de manera más eficiente.
	
Permite el análisis detallado:
Los breakpoints ofrecen a los desarrolladores la capacidad de inspeccionar variables, ejecutar instrucciones 
paso a paso y analizar el flujo de ejecución del programa. 
Esto les permite comprender mejor cómo funciona el código y cómo interactúan diferentes partes del programa.
	

<p align=center>
Desventajas
<p align=left>
Puede ralentizar la ejecución:
El uso excesivo de breakpoints puede ralentizar la ejecución del programa, especialmente en aplicaciones 
grandes o complejas. 
Esto también puede afectar negativamente la productividad del desarrollador y el rendimiento del programa.

Posible dependencia excesiva:
Algunos desarrolladores pueden volverse dependientes de los breakpoints para depurar su código, lo que 
puede dificultar el desarrollo de habilidades de depuración más avanzadas y comprensión del código.

Riesgo de introducir nuevos errores:
Al agregar o modificar breakpoints durante el proceso de depuración, existe el riesgo de introducir 
nuevos errores en el código; como el olvidar eliminar un breakpoint después de su uso puede causar 
problemas en la ejecución del programa en producción.


	</p>

</pre>
<pre>

	

<p align=center>
Inspección de registros y memoria
	
<p align=left>
La inspección de registros y memoria en ensamblador con GDB es una habilidad fundamental para depurar programas a nivel de bajo nivel. 

<p align=center>
Registros:
	<p align=left>
Los registros son ubicaciones de almacenamiento de datos dentro de la CPU. Cada registro tiene un propósito específico y se utiliza
para realizar operaciones aritméticas, almacenar valores temporales y controlar el flujo del programa.
Algunos registros comunes en arquitecturas x86 incluyen EAX, EBX, ECX, EDX, ESP, EBP, ESI y EDI.
Puedes inspeccionar los valores de estos registros utilizando comandos como info registers o simplemente escribiendo el nombre del 
registro en GDB.
<p align=center>
Memoria:
		<p align=left>
La memoria es donde se almacenan los datos y las instrucciones del programa. En ensamblador, a menudo trabajamos con la memoria
utilizando direcciones de memoria. Puedes inspeccionar la memoria utilizando el comando x seguido de un formato y una dirección.
Por ejemplo, x/10x $esp muestra los primeros 10 valores en la pila (stack) a partir del puntero de pila actual ($esp).
<p align=center>
Inspeccion de registos y memoria
<p align=left>
La inspección de registros y memoria en este contexto implica observar los valores almacenados en los registros del procesador en
un momento dado durante la ejecución del programa, así como examinar los contenidos de las direcciones de memoria donde se almacenan
datos o instrucciones.

Por ejemplo, al depurar un programa escrito en ensamblador con GDB, podrías querer examinar los registros para ver cómo cambian
durante la ejecución del programa, o podrías querer inspeccionar la memoria para ver los valores almacenados en ciertas ubicaciones de memoria.

En resumen, al trabajar con ensamblador y GDB, la inspección de registros y memoria te permite comprender cómo se comporta tu programa
a nivel de procesador y cómo interactúa con la memoria del sistema durante la ejecución. Esto es esencial para depurar y entender el
comportamiento de programas de bajo nivel.
<p align=center>
Como realizar la inspección
<p align=left>
Para realizar la inspección de registros y memoria en ensamblador con GDB, se siguen los siguientes estos pasos:

1.- Abrir el programa en GDB:
Abre una terminal y ejecuta gdb seguido del nombre del programa que deseas depurar. Por ejemplo: gdb mi_programa.
2.- Cargar el programa:
En GDB, carga el programa ejecutando file mi_programa.
3.- Iniciar la depuración:
Ejecuta run o start para comenzar la ejecución del programa.
4.- Examinar registros:
Utiliza el comando info registers para mostrar los valores dentro de los registros. Esto te proporcionará información sobre los registros
actuales y sus contenidos.
5.- Inspeccionar memoria:
Para examinar la memoria, utiliza el comando x seguido de un formato y una dirección. Por ejemplo:
x/10x $esp: Muestra los primeros 10 valores en la pila (stack) a partir del puntero de pila actual ($esp).
x/20i $rip: Muestra las primeras 20 instrucciones a partir del puntero de instrucción ($rip).
6.- Interpretar los valores en memoria:
Los valores hexadecimales que obtienes al inspeccionar la memoria representan los datos almacenados en esas direcciones.
La interpretación depende del contexto del programa y la arquitectura. Por ejemplo:
Si encuentras una dirección que parece ser una función, puedes seguir esa dirección para ver qué instrucciones contiene.
Si ves valores que parecen punteros, puedes seguirlos para ver qué datos apuntan.
7.- Depurar y ajustar:
Utiliza esta información para depurar problemas en tu programa. Puedes establecer puntos de interrupción, modificar valores de registros o 
inspeccionar la memoria en momentos clave.

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
