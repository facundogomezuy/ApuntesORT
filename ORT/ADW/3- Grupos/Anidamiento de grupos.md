
• MIEMBRO de un grupo: es cada uno de los objetos que ha sido asignado al grupo. 
• MIEMBRO DE: es el grupo al cual está asignado un objeto. 
• ANIDAMIENTO DE GRUPOS – es la posibilidad de que un grupo pueda ser miembro de otro grupo. 
Cuando un usuario es agregado como miembro de un nuevo grupo, el cambio se hace efectivo cuando el usuario vuelva a iniciar la próxima sesión.




![[Pasted image 20250510133903.png]]![[Pasted image 20250510133924.png]]



Estrategia I-G-DL-A:

Microsoft sugiere una estrategia de administración basada en roles de la siguiente forma: 
• Los miembros de un grupo son llamados Identidades para no hacer diferencia entre usuarios, equipo u otros.
• Definir grupos que definen tipo de trabajo o características de los usuarios (roles), con ámbito Global.
• Definir grupos que definen tipo de acceso a los recursos (reglas de negocio), con ámbito Local Dominio• Anidar los grupos de forma que facilite la administración 
• El término Acceso incluye no solo el control sobre los recursos (permisos) sino también sobre las funcionalidades del sistema (derechos). Seguridad: Para asignar derechos y permisos de usuario. También se puede usar como lista de correo electrónico
![[Pasted image 20250510134006.png]]
![[Pasted image 20250510134016.png]]
![[Pasted image 20250510134028.png]]

Ejemplo a representar mediante I-G-DL-A: 
• En mi empresa tengo las carpetas compartidas LEGALES, PROCEDIMIENTOS y DIRECCION. 
• Las tres carpetas tienen dos niveles de acceso, LECTURA (R) y CONTROL TOTAL (FC). 
• La gente de administración debe poder acceder con permisos de FC a la carpeta LEGALES y con permisos de R a PROCEDIMIENTOS y DIRECCION. 
• Los directivos deben poder acceder con los permisos de FC a las tres carpetas. 
• Los gerentes deben poder acceder con permisos de Ra la carpeta LEGALES y con permisos de FC a la carpeta PROCEDIMIENTOS. 
• Los técnicos deben poder acceder con permisos de Ra la carpeta PROCEDIMIENTOS.

![[Pasted image 20250510134118.png]]

Ventajas: 
• ACLs más cortas y manejables 
• Escalabilidad: a mayor cantidad de usuarios, impactan en los grupos globales pero no los DL. Si el número de grupos globales es muy grande, anidarlos. 
• La administración diaria se centra en los miembros de los grupos globales solamente 

Si el escenario es un bosque con varios árboles, pueden incluirse grupos Universales: Estrategia I-G-U-DL-A