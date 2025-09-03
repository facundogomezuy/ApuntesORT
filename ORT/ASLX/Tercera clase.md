

###### **Gestión de la CPU en Linux** 
Linux emplea un planificador avanzado: 
● Completely Fair Scheduler (CFS): Usa árboles de búsqueda balanceados para asignar CPU de manera justa. 
● Grupos de control (cgroups): Permiten restringir el uso de CPU por procesos específicos. 
● Modo kernel y modo usuario: Los procesos ejecutan instrucciones en dos niveles de privilegios.

###### **Gestión de Memoria en Linux** 
Linux gestiona la memoria con técnicas avanzadas como: 
● Paginación demandada: Carga en memoria sólo las páginas requeridas. 
● Swapping: Intercambio de páginas entre RAM y disco. 
● Transparent Huge Pages (THP): Reduce la fragmentación de memoria.



###### **Gestión de Dispositivos y Recursos en Linux: procfs y sysfs** 
El kernel de Linux expone información del sistema a través de interfaces virtuales ubicadas en /proc y /sys. Estas interfaces permiten a los administradores y aplicaciones consultar el estado del sistema y modificar parámetros en tiempo real.


**procfs (/proc) - Sistema de Archivos de Procesos** 
El sistema de archivos /proc (procfs) es una interfaz virtual en Linux que proporciona información detallada sobre los procesos en ejecución y el estado del sistema. Se monta en /proc y contiene una serie de archivos y directorios que reflejan datos del kernel.


**sysfs (/sys) - Interfaz para la Información del Hardware** 
El sistema de archivos /sys (sysfs) proporciona una forma estructurada de acceder a información del hardware y modificar ciertos parámetros de los dispositivos. Fue introducido en el kernel 2.6 para mejorar la organización del sistema de archivos virtual /proc.

**¿Qué es un Shell?** 
Un shell es un programa que ofrece una interfaz entre el usuario y el sistema operativo, permitiendo el acceso y gestión de sus servicios. 
Tipos de Shell: 
● Gráficos: GNOME, KDE Plasma, Xfce, LXDE. 
● Texto: Bash, Zsh, csh, ksh, dash.

**¿Qué es la Consola?** 
La consola es un conjunto de dispositivos (pantalla, teclado y mouse) que se conectan al computador. En equipamientos más antiguos la consola podía ser una terminal denominada terminal tonta que consiste de una pantalla y un teclado. O podría ser un teleimpresor. La consola era utilizada por administradores u operadores.


**¿Qué es una terminal?** 
Una terminal es un dispositivo electrónico compuesto por una pantalla y un teclado. Es utilizado para comunicarse con una computadora.

¿Qué es un emulador de terminal? 
Un emulador de terminal es una aplicación que simula la funcionalidad de una terminal física en entornos gráficos o redes modernas. 
● Ejemplos en Windows: Windows Terminal, PuTTY, MobaXterm. 
● Ejemplos en Linux: gnome-terminal, xterm, konsole.

###### **Bash**
Bash es un intérprete de comandos y un lenguaje de programación compatible con sh (Bourne shell). También incorpora características útiles de los shells Korn y C (ksh y csh)

Tipos de comandos. 
1. Alias 
2. Función 
3. Comando integrado a la shell (shell builtin) 
4. Palabra clave 
5. Archivo

