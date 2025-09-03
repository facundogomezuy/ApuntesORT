**Variables en Bash** 
En Bash, las variables son contenedores que almacenan valores, como cadenas de texto o números, que pueden ser utilizados a lo largo de un script o en la línea de comandos. Las variables se definen simplemente asignando un valor a un nombre, por ejemplo:

**Variables de ambiente** 
Por otro lado, las variables de ambiente son un tipo especial de variables que no solo son accesibles en el shell actual, sino que también son heredadas por los procesos hijos creados por el shell. Estas variables de ambiente son utilizadas por el sistema y los programas para configurar su comportamiento. Ejemplos comunes incluyen PATH, HOME, y USER. 
Para convertir una variable en una variable de ambiente, se usa el comando export. 
Por ejemplo: *`export nombre=”Juan”*`

###### **Sustitución de Variables** 
Las variables en Bash se sustituyen por sus valores antes de la ejecución del comando. Esto permite utilizar valores almacenados en variables directamente en los comandos.
![[Pasted image 20250903192018.png]]
###### **Sustitución de comandos** 
La sustitución de comandos permite ejecutar un comando dentro de una línea de comando y usar su salida como parte de otro comando. Esto se logra con la sintaxis $(comando) o `comando`.
![[Pasted image 20250903192107.png]]

###### **Sustitución aritmética** 
Permite realizar cálculos aritméticos dentro de la línea de comando. La sintaxis es $(()).
![[Pasted image 20250903192136.png]]

###### **Sustitución de tilde (~)** 
El tilde (~) se sustituye por el directorio home del usuario actual
![[Pasted image 20250903192204.png]]


###### **Expansión de nombres de archivo (Globbing)** 
La coincidencia de patrones en la línea de comandos de Bash, también conocida como "globbing", es una característica que permite a los usuarios especificar conjuntos de archivos o directorios utilizando caracteres especiales llamados metacaracteres. Bash expande estos patrones para coincidir con nombres de archivos y directorios en el sistema de archivos antes de ejecutar un comando. Los caracteres especiales son *, ?, [ ]

![[Pasted image 20250903192553.png]]
![[Pasted image 20250903192601.png]]







