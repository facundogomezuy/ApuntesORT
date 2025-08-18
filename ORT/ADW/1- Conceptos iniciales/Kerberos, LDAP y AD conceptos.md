
###### **Autenticación:**
Proceso que usa el Sistema Operativo para identificar a un usuario y otorgarle o denegarle el acceso a una sesión en un equipo

• En los dominios de Active Directory este proceso es brindado por el protocolo Kerberos v5. 
• En un grupo de trabajo este proceso ocurre localmente a través de la SAM (Security Account Manager) de cada equipo

###### **Autorización:**
Proceso que usa el Sistema Operativo para otorgarle o denegarle el acceso a un usuario sobre un determinado recurso.

• En entornos de dominio este acceso se obtiene al mismo tiempo que la autenticación, ya que el protocolo Kerberos v5 implementado por Microsoft asigna un “token” en el que se incluye el identificador del usuario y el de los grupos a los que pertenece. 
• Según los permisos o derechos que tenga ese usuario y los grupos de los que es miembro, será el acceso efectivo que obtendrá.

![[Pasted image 20250506171100.png]]


• Utiliza DNS como Sistema de nombres y de búsqueda.
• Permite la delegación de la administración. 
• Brinda un alto nivel de seguridad por medio de protocolos y métodos de cifrado que protegen los datos almacenados y las comunicaciones entre los miembros de un dominio.

• Componentes lógicos más comunes de Active Directory: 
– Dominio: contexto de seguridad y administración
– Unidad Organizativa (OU): contenedor que facilita la administración 
– Árbol de dominios: conjunto de dominios que comparten un espacio de nombres DNS contiguos 
– Bosque: Conjunto de árboles de dominio. Todos los objetos de un bosque tienen la misma definición y los mismos atributos. 
– Objetos: el contenido del Directorio. Ejemplos de objetos son los usuarios, grupos o cuentas de equipo.

![[Pasted image 20250506171301.png]]

Unidades organizativas (OU): Las unidades organizativas son como “carpetas” que permiten entre otras cosas organizar los elementos dentro del dominio

![[Pasted image 20250506171353.png]]

Microsoft Management Console: Permite administrar las distintas funciones de un equipo 
• Algunas consolas predefinidas se encuentran en la carpeta “Herramientas administrativas” 
• Es posible crear consolas personalizadas desde una MMC vacía 
• Muchas funciones de Windows Server agregan complementos para MMC


• Los roles de servidor son paquetes de software que permiten al servidor realizar una función determinada para los demás equipos de la red. 
• Un equipo puede tener uno o varios roles. 
• Ejemplos de roles: Controlador de Dominio (AD DS), Servidor DHCP, Servidor DNS, Servidor Web. • Los roles pueden tener uno o varios servicios. Un ejemplo de rol con varios servicios es NPAS (Network Policy and Access Server)


• Las características de servidor son componentes de software que proveen funcionalidades adicionales. 
• Ejemplos de características: Windows Server Backup, .NET Framework, WINS.


![[Pasted image 20250510124749.png]]



preguntas a hacerse:
• ¿Qué es un sistema operativo? 
• ¿Cuál es la diferencia entre un dominio y un grupo de trabajo? 
• ¿Qué es un Controlador de Dominio? 
• ¿Qué particularidad tiene el token de Kerberos de Active Directory? 
• ¿Qué es un dominio? ¿Qué es una OU? 
• ¿Cuál es la relación entre AD DS y DNS? 
• ¿Cuántas MMC predefinidas hay en un equipo?
• ¿Qué es un rol de servidor? 
• ¿Qué es una característica de servidor?