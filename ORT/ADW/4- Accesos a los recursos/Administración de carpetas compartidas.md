

**Que son las carpetas compartidas:** Las Carpetas Compartidas (Shared folders) proporcionan un mecanismo de acceso a archivos que se encuentran en otro equipo. 
Para el manejo de carpetas compartidas es requerido contar con permisos administrativos: 
• Administrators 
• Server Operators 
• Power users (en versiones viejas)



**Para compartir una carpeta necesito:** 
• Una Computadora que necesite compartir una carpeta a través de la red. Por ejemplo: PC01. 
• Una Carpeta Real (Folder Path) en el File System donde está la información que quiero compartir. Por ejemplo C:\DATOS\2023. 
• Un Alias (Share Name) que es el nombre con el que va a ver esa carpeta compartida desde la red (punto de acceso remoto). Por ejemplo: INFORMES. 

El acceso remoto se controla a través de una ACL que se asocia al recurso compartido. 

La ACL contiene, como cualquier ACL, una lista de entradas (ACEs) compuestas cada una de: 
• Un SID (usuario, equipo o grupo) 
• Un nivel de acceso (Control Total, Cambio, Lectura) 
• Un tipo (Permitir o Denegar)

##### **Permisos de las carpetas compartidas:**

**Lectura (Read)** 
• Ver datos de archivos y atributos. 
• Ver nombre de los archivos y subcarpetas. 
• Ejecutar archivos de programa. 

**Cambio (Change)** 
• Agregar archivos y subcarpetas. 
• Cambiar contenido en los archivos. 
• Eliminar archivos y subcarpetas. 

**Control Total (Full Control)** 
• Cambiar los permisos de archivos y carpetas. 
• Cambiar atributos (nombre, dueño)

**De forma predeterminada se aplica el permiso READ(LECTURA) al grupo EVERYONE (TODOS)**

**ACL (ACCESS CONTROL LIST)** 
• Es una lista de permisos 
• Tiene un conjunto de entradas 
• Cada entrada se denomina ACE 

**ACE (ACCESS CONTROL ENTRY)** 
• Determinar la membrecía a Grupos. 
• Quién --- Permiso --- Otorgado o Denegado(Allow or Denied) 
• Quién (Equipo, Usuario, Grupo) 
• Permiso (Read, Change, FC)


###### **PERMISOS EFECTIVOS** 
• Son los permisos resultantes cuando un usuario accede a una carpeta compartida. 
• Como los permisos son acumulativos, hay que establecer un método para determinarlos. 
• Los permisos denegados tienen “mayor peso”, es decir que prevalecen. 
• Es el resultado del acceso (proceso de autorización) de un usuario a una carpeta compartida. 
• Hay 4 posibilidades de resultado (Full Control, Change, Read o no tiene permisos) 

###### **MÉTODO PARA EVALUAR PERMISOS (Cuando accede un usuario)**
1. Determinar la membrecía a Grupos. 
2. Separar permisos otorgados (allow) de denegados (deny) en la ACL. 
3. “Sumar” los permisos otorgados. 
4. “Restar” los permisos denegados.

![[Pasted image 20250510135146.png]]

![[Pasted image 20250510135157.png]]

![[Pasted image 20250510135203.png]]

![[Pasted image 20250510135208.png]]

![[Pasted image 20250510135215.png]]



Es posible compartir carpetas utilizando el 
Explorador de Archivos: 
• Con asistente. 
• Sin asistente (avanzado) 
Desde Computer Management – Shared FoldersDesde CMD: 
• Listar recursos: Net Share 
• Crear: Net Share (nombre)=(ruta de carpeta) 
• Eliminar: Net share (nombre) /delete 
Otras opciones incluyen PowerShell (New-SMBShare)
![[Pasted image 20250510135313.png]]

![[Pasted image 20250510135332.png]]
![[Pasted image 20250510135341.png]]


Recomendaciones 
• Usar los permisos más restrictivos posibles. – Evitar asignar Full Control a menos que sea necesario. 
• Asignar permisos a grupos en vez de a usuarios. 
• Sustituir el grupo Everyone por el grupo Authenticated Users. 
• Crear carpetas compartidas ocultas asignando una unidad para uso de los usuarios que corresponda.