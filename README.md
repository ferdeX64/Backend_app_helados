Funcionalidades:

1.Registro de usuarios: La aplicación permite a los usuarios registrarse proporcionando su nombre de usuario, contraseña y una foto de perfil.
2.Almacenamiento seguro de contraseñas: Antes de almacenar la contraseña en la base de datos, se aplica un proceso de hashing utilizando la función bcrypt para garantizar la seguridad de las contraseñas de los usuarios.
3.Almacenamiento de la foto de perfil: La foto de perfil del usuario se guarda en el sistema de archivos del servidor. Se almacena la ruta de la imagen en la base de datos para su posterior recuperación.
4.Autenticación: Los usuarios pueden autenticarse proporcionando su nombre de usuario y contraseña. Si las credenciales son válidas, se genera un token JWT que se devuelve al cliente para su uso en futuras solicitudes.
5.Protección de rutas: Se implementa un middleware que verifica la validez del token JWT en las rutas que requieren autenticación. Si el token es válido, se permite el acceso; de lo contrario, se devuelve un error de autorización.
6.Renovación de tokens: Se proporciona un mecanismo para que los usuarios actualicen su token JWT antes de que expire.

