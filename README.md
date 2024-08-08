# Tercer Práctica Integradora

El presente repositorio contiene la tercer practica integradora sobre lo visto hasta el momento en el curso de Backend.

# Estructura del Repo

```bash
└───src
│   app.js
│   
├───config
│       config.js
│       database.js
│       passport.config.js
│       socketConfig.js
│       
├───controllers
│       cartController.js
│       mockingController.js
│       productController.js
│       ticketController.js
│       userController.js
│       
├───dao
│   ├───DTOs
│   │       usersDTO.js
│   │       
│   └───models
│           cart.model.js
│           message.model.js
│           product.model.js
│           ticket.model.js
│           user.js
│
├───middleware
│   │   auth.js
│   │
│   └───errors
│           index.js
│
├───public
│   ├───css
│   │       styles.css
│   │
│   └───js
│           carts.js
│           chat.js
│           products.js
│           resetPassword.js
│           tickets.js
│           users.js
│
├───routes
│   │   cart.router.js
│   │   messages.router.js
│   │   mocking.router.js
│   │   product.router.js
│   │   ticket.router.js
│   │   user.router.js
│   │   views.router.js
│   │
│   └───api
│           sessions.js
│
├───services
│       cartService.js
│       customError.js
│       emailService.js
│       enums.js
│       info.js
│       messageService.js
│       productService.js
│       ticketService.js
│       userService.js
│
├───utils
│       utils.js
│
└───views
    │   carts.handlebars
    │   chat.handlebars
    │   editProduct.handlebars
    │   login.handlebars
    │   newProduct.handlebars
    │   products.handlebars
    │   profile.handlebars
    │   register.handlebars
    │   requestReset.handlebars
    │   resetPassword.handlebars
    │   userRole.handlebars
    │
    └───layouts
            main.handlebars
```

## Instalación

1. Clona este repositorio.

   ```bash
   git clone https://github.com/nicob201/practica_integradora_3.git
   ```

## Configuración

1. Crea el archivo `.env.development` para configurar la base de datos segun el entorno que se desee utilizar, ten en cuenta las siguientes variables de entorno:

      MONGO_URL=

      PORT=

      CLIENT_ID=

      CLIENT_SECRET=

      GOOGLE_CLIENT_ID=

      GOOGLE_CLIENT_SECRET=

      MAILING_EMAIL=

      MAILING_PASSWORD=



2. Configura el servidor en `app.js`.

## Inicio

`npm start`: Inicia el servidor

## Rutas relevantes de esta entrega

```bash
   http://localhost:8080/premium/:uid
```
# Pruebas

Si se ingresa como usuario el email: "premium@gmail.com", clave: "123" se inicia la API en el modo premium que permite editar los roles de los usuarios, crear, editar o eliminar productos.

Si se crea un nuevo usuario, este tendra el rol "user", y no podrá hacer CRUD de los productos ni editar los roles de los usuarios.

## Reset Password

Si se crea un usuario con una contraseña, y luego en la pantalla Login se da click en el boton "Reset Password", se pide completar un email donde se envia el link para crear una nueva contraseña para el usuario.