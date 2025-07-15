# Estructura de 02_users_profiles

Esta carpeta está organizada siguiendo el patrón **MVC (Modelo-Vista-Controlador)** y agrupada en tres módulos principales: **users**, **profiles** y **verification**. Cada módulo responde a una necesidad funcional distinta dentro de la gestión de usuarios y perfiles del sistema.

## ¿Por qué tres partes?

- **users/**: Contiene todo lo relacionado con la gestión de usuarios (CRUD, servicios de cambio de contraseña, primer login, etc.). Aquí se centralizan las operaciones principales sobre los usuarios del sistema.
- **profiles/**: Gestiona la información de perfil de los usuarios, como la edición de datos personales y la gestión de imágenes de perfil. Se separa para mantener la lógica de perfil independiente de la gestión general de usuarios.
- **verification/**: Incluye la lógica de verificación de usuarios, recuperación de contraseñas y envío de correos de verificación. Se aísla para facilitar el mantenimiento y la escalabilidad de los procesos de autenticación y seguridad.

## Estructura MVC

Cada módulo sigue el patrón MVC, distribuyendo los archivos en:

- **Controllers/**: Controladores que reciben las solicitudes HTTP, validan datos y coordinan la lógica de negocio.
- **Models/**: Representan las entidades y estructuras de datos del sistema (por ejemplo, User.php).
- **Requests/**: Clases para la validación de datos de entrada en las solicitudes (por ejemplo, StoreUserRequest.php).
- **Resources/**: Transforman los modelos en respuestas JSON estructuradas para la API (por ejemplo, UserResource.php, UserCollection.php).
- **Services/**: Contienen la lógica de negocio reutilizable y operaciones complejas (por ejemplo, UserService.php, ChangePasswordService.php).
- **Mails/** (solo en verification): Plantillas y clases para el envío de correos electrónicos.
- **Views/** (solo en verification): Vistas Blade para correos electrónicos y procesos de verificación.

## Ejemplo de estructura

```
02_users_profiles/
  ├── users/
  │   ├── Controllers/         # Controladores de usuarios
  │   ├── Models/              # Modelos de datos de usuario
  │   ├── Requests/            # Validaciones de usuario
  │   ├── Resources/           # Formateo de respuestas de usuario
  │   ├── Services/            # Lógica de negocio de usuario
  │   └── #HU01-GestionUsuarios-CRUD/ # Documentación de la historia de usuario
  ├── profiles/
  │   ├── Controllers/         # Controladores de perfil
  │   ├── Models/              # Modelos de perfil (si aplica)
  │   ├── Requests/            # Validaciones de perfil
  │   ├── Services/            # Lógica de negocio de perfil
  ├── verification/
  │   ├── Controllers/         # Controladores de verificación (si aplica)
  │   ├── Models/              # Modelos de verificación
  │   ├── Services/            # Lógica de negocio de verificación
  │   ├── Mails/               # Clases de correo
  │   └── Views/               # Vistas Blade para emails
```

## ¿Qué hace cada archivo?

- **UserController.php, ProfileController.php, etc.**: Gestionan las peticiones y respuestas HTTP.
- **User.php, UserVerificationCode.php, etc.**: Definen la estructura y relaciones de los datos.
- **StoreUserRequest.php, UpdateProfileRequest.php, etc.**: Validan los datos recibidos en las solicitudes.
- **UserResource.php, UserCollection.php, etc.**: Transforman los modelos en respuestas API.
- **UserService.php, ChangePasswordService.php, etc.**: Implementan la lógica de negocio y operaciones complejas.
- **VerificationEmail.php**: Define el contenido y destinatarios de los correos de verificación.
- **verification.blade.php, password-restore.blade.php**: Plantillas visuales para los correos electrónicos enviados a los usuarios.

Esta organización facilita el mantenimiento, la escalabilidad y la comprensión del código, permitiendo que cada parte del sistema evolucione de forma independiente y ordenada. 