

![[Pasted image 20250510135422.png]]


Permisos NTFS
• Cada carpeta o archivo en una partición/volumeNTFSposee su propia Lista de Control de Acceso (ACL) que lo protege.
• La ACL es una lista con 0 o más entradas. 
• Cada entrada se llama ACE y asocia un permisoconcreto a un objeto con SID (usuario, equipo o grupo) sobre la carpeta/archivo. 
• Cada entrada puede ser de dos tipos: 
- Heredadas de la carpeta padre.  ![[Pasted image 20250510135505.png]]
- Explícita de la propia carpeta o archivo. ![[Pasted image 20250510135516.png]]


###### **Los permisos NTFS están organizados en permisos BÁSICOS/ESTÁNDAR y permisos AVANZADOS.**

• La interface de permisos NTFS por defecto muestra 5 permisos básicos (o estándar) para archivos y 6 permisos básicos para carpetas. 
• Concede niveles de acceso clásicos o habituales sobre archivos y carpetas (autorizan) 
• Se definen de manera incremental.
![[Pasted image 20250510135613.png]]


PERMISOS EFECTIVOS 
• Son los permisos resultantes cuando un usuario accede a una archivo o carpeta en NTFS. 
• Como los permisos son acumulativos, hay que establecer un método para determinarlos. 
• Los permisos explícitos tienen “mayor peso”, es decir que prevalecen. 
• Es el resultado del acceso (proceso de autorización) de un usuario a una carpeta o archivo en NTFS. 
• Hay 8 posibilidades de resultado cuando se evalúan permisos estándar de propagación estándar – Full Control 
– Modify 
– Read & Execute 
– Read 
– Write 
– Read & Execute + Write
– Read + Write 
– Sin permisos


MÉTODO PARA EVALUAR PERMISOS (Cuando accede un usuario a una carpeta o archivo de forma local en NTFS) 
1. Determinar la membrecía a Grupos. 
2. Separar permisos otorgados (allow) de denegados (deny) en la ACL. 
3. “Sumar” los permisos otorgados heredados. 
4. “Restar” los permisos denegados heredados. 
5. “Sumar” los permisos otorgados explícitos. 
6. “Restar” los permisos denegados explícitos

![[Pasted image 20250510135953.png]]

###### **Permisos NTFS “Permisos AVANZADOS”** 

**Todo permiso es en realidad:** 
	• Una combinación de 13 + 1 permisos avanzados o individuales. 
	• Cada permiso básico es una combinación predeterminada de algunos de los 13 +1 permisos avanzados. 
**Los permisos avanzados o individuales permiten:** 
	• Ajustar más sutilmente la asignación de permisos. 
	• Es posible activar o desactivar algunos de estos permisos avanzados de manera individual. 
	• Cuidado, porque no todas las combinaciones son coherentes o útiles.

**Permisos Avanzados** 
• Son 12 + 1 permisos para archivos. 
• Son 13 + 1 permisos para carpetas. 
• Los permisos “dobles” representan carpetas / archivos


FOLDER:
![[Pasted image 20250510140231.png]]


File:
![[Pasted image 20250510140242.png]]

