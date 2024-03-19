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

	</p>

</pre>
