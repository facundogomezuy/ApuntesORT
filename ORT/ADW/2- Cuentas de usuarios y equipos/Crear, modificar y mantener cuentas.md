
Tipos de cuentas de usuario
• Cuentas de usuario almacenadas en la SAM de cada equipo. 
• Cuentas de usuario almacenadas en el directorio de red
• Cada cuenta de usuario está identificada por un SID (Security ID) único para cada contexto de seguridad

Cmd comando crear cuenta: 
– DSADD USER “nombre LDAP completo” parámetros

dsadd user "cn=ChewDavid,ou=Empleados,dc=empresa,dc=com" ^
-pwd MiContraseña123 (ESPECIFICA CONTRASENIA)
-mustchpwd yes (deba cambiar la contrasenia en el proximo loguio)
-canchpwd no  (no pueda cambiar la contrasenia)
-disabled no  (deshabilitadao)
-display "David Chew"(nombre)
-desc "Director de Tecnología" (descripcion)

PowerShell comando crear cuenta:
New-ADUser -Name "ChewDavid" -OtherAttributes @{'title'="director";'mail'="chewdavid@fabrikam.com"}


New-ADUser -Name "ChewDavid" `
-SamAccountName "chewdavid" `
-GivenName "David" (NOMBRE)
-Surname "Chew" (APELLIDO)
-UserPrincipalName "chewdavid@empresa.com" `
-Title "Director" `
-EmailAddress "chewdavid@empresa.com" `
-AccountPassword (ConvertTo-SecureString "MiContraseña123" -AsPlainText -Force) `
-Enabled $true `
-ChangePasswordAtLogon $true `
-PasswordNeverExpires $false `
-Path "OU=Empleados,DC=empresa,DC=com" `
-Description "Director de Tecnología"



dsmod user <DN_del_usuario> [opciones]

| `-samid <nombre>` | Cambia el `sAMAccountName` (nombre de inicio de sesión). |
| ----------------- | -------------------------------------------------------- |

| `-upn <usuario@dominio>` | Cambia el UPN (nombre principal de usuario). |
| ------------------------ | -------------------------------------------- |

| `-fn <nombre>` | Cambia el primer nombre (givenName). |
| -------------- | ------------------------------------ |


| `-ln <apellido>` | Cambia el apellido (surname). |
| ---------------- | ----------------------------- |

| `-display <nombre>` | Cambia el nombre mostrado (displayName). |
| ------------------- | ---------------------------------------- |

| `-pwd <contraseña>` | Cambia la contraseña. |
| ------------------- | --------------------- |

| `-mustchpwd {yes | no}` |
| ---------------- | ---- |

| `-canchpwd {yes | no}` |
| --------------- | ---- |

| `-pwdneverexpires {yes | no}` |
| ---------------------- | ---- |

| `-disabled {yes | no}` |
| --------------- | ---- |

| `-desc <texto>` | Cambia la descripción. |
| --------------- | ---------------------- |

| `-office <texto>` | Asigna una oficina. |
| ----------------- | ------------------- |

| `-email <correo>` | Asigna un correo electrónico. |
| ----------------- | ----------------------------- |

| `-tel <número>` | Teléfono del usuario. |
| --------------- | --------------------- |


Set-ADUser -Identity <usuario> [parámetros]
|Parámetro|Descripción|
|---|---|
|`-Identity`|Identifica al usuario (puede ser SamAccountName, DistinguishedName, etc.).|
|`-GivenName`|Primer nombre.|
|`-Surname`|Apellido.|
|`-DisplayName`|Nombre para mostrar.|
|`-UserPrincipalName`|UPN (correo/identificador de inicio de sesión).|
|`-Title`|Título del cargo.|
|`-Department`|Departamento.|
|`-Description`|Descripción.|
|`-EmailAddress`|Correo electrónico.|
|`-OfficePhone`, `-MobilePhone`|Teléfonos.|
|`-CannotChangePassword $true`|El usuario **no puede cambiar la contraseña**.|
|`-PasswordNeverExpires $true`|La contraseña **nunca expira**.|
|`-AccountExpirationDate`|Fecha de expiración de la cuenta.|
|`-Enabled $false/$true`|Habilita o deshabilita la cuenta.|
|`-Replace @{atributo=valor}`|Cambia directamente cualquier atributo LDAP.|