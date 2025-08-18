
• Los permisos son acciones que se pueden realizar sobre los objetos de un Sistema Operativo. Por ejemplo: ejecutar un archivo, ver el contenido de una carpeta, modificar un documento. 
• Los derechos son acciones que se pueden realizar sobre el Sistema operativo. Por ejemplo: iniciar sesión en el equipo, modificar la hora, apagar el equipo. 
• Los permisos se manejan a través de las llamadas ACL (Access Control List) 
• Los derechos se establecen a través de las directivas de grupo.

• La existencia de una ACL depende de que el Sistema de archivos sea NTFS. 
• En otros Sistemas de archivos, el permiso es de “control total” para “Todos” 
• Una ACL es un conjunto de ACEs (Access Control Entries). Si ninguna ACE coincide con el intento de acceso, este es denegado. 
• No es necesaria la denegación o negación explícita. Esta se usa para excepciones a los accesos otorgados.

que es un grupo?
Un grupo es un objeto que representa a una lista de objetos similares (usuarios, equipos, otro grupo), permitiendo una administración más eficiente.

Existen dos tipos de grupos: 
• Distribución: Para integración con aplicaciones de correo electrónico 
• Seguridad: Para asignar derechos y permisos de usuario. También se puede usar como lista de correo electrónico. Los grupos varían menos que los usuarios, por lo que las ACLs cambian menos que la lista de objetos que están en el grupo.



El ámbito de grupo (group scope) define desde dónde es visible para poder agregarlo a la ACL del recurso.
• Local al Equipo
• Local al Dominio
• Global 
• Universal

![[Pasted image 20250510133618.png]]

Grupo local de equipo 
• Se define en la SAM de cada equipo 
• Los miembros pueden ser:
– Usuarios locales del equipo 
– Usuarios o grupos del dominio (si el equipo está sumado a un dominio) 
• Es visible solamente para los recursos de ese equipo
• Se utiliza en grupos de trabajos. No es recomendable su uso en entornos de dominio.


Grupo local de dominio 
• Los miembros pueden ser: 
– Usuarios, Equipos, Grupos Globales y Grupos Universales de cualquier dominio en el bosque 
– Grupo Local de Dominio del mismo dominio 
• Es visible solo para los recursos solo del dominio donde se crea. 
• Puede ser miembro de otro Grupo Local de Dominio del mismo dominio 
• Los grupos DL se utilizan en las ACLs de los recursos

![[Pasted image 20250510133742.png]]



Grupo global 
• Los miembros pueden ser: 
– Usuarios, Equipos y Grupos Globales del mismo dominio que el grupo 
• Es visible para los recursos de cualquier dominio del bosque. 
• Puede ser miembro de cualquier Grupo Local de Dominio o Grupo Universal del bosque y Global del mismo dominio 
• Facilita el acceso a recursos que se encuentran en otro dominio.



![[Pasted image 20250510133814.png]]


Grupo Universal 
• Los miembros pueden ser: 
– Usuarios, Equipos, Grupos Globales y Grupos Universales de cualquier dominio en el bosque 
• Es visible solo para los recursos de cualquier dominio del bosque. 
• Puede ser miembro de un Grupo Universal o de un Grupo Local de Dominio de cualquier dominio del bosque 
• Su uso es similar al de un grupo global, más eficiente en bosques con múltiples árboles. 
• Su uso genera un mayor tráfico de replicación entre los controladores de dominios que almacenan una copia del Catálogo Global.

![[Pasted image 20250510133853.png]]



Recomendaciones para grupos 
• Usar grupos predeterminados con cautela. 
• Usar grupos locales de equipo, sólo si el equipo no pertenece a ningún dominio. 
• Planificar los grupos usando estrategia I-G-DL-A o I-G-U-DL-A 
• Documentar y usar nombres de grupos adecuados. 
• Agregar las cuentas de usuario a los grupos más restrictivos. 
• Usar el grupo “authenticated users” en vez de “everyone”. 
• Limitar el número de miembros del grupo “Administradores”. 
• Proteger los grupos DL más críticos.