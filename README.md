# Back-end con Firebase

_Este proyecto tiene como finalidad la comprensión del uso del servicio de back-end de Firebase para crear webs dinámicas._

## Comenzando 🚀

_Estas instrucciones le permitirán obtener una copia del proyecto en funcionamiento en su máquina local para propósitos de desarrollo, pruebas y aprendizaje._


### Pre-requisitos 📋

_Firebase es un servicio de back-end en la nube que no requiere tener nada pre-instalado de forma local para su funcionamiento, sino que lo todo será consumido con JavaScript desde el front-end._

_También se puede trabajar mediante sus herramientas de desarrollo desde la terminal, pero no es la finalidad de éste proyecto. Si quiere instalar las herramientas de desarrollo de Firebase debe tener instalado [Node.js](https://nodejs.org/es/)._

```
https://nodejs.org/es/
```

### Instalación 🔧

_Desarrollar un proyecto igual que éste solo requiere poseer una cuenta en Google y darse de alta en los servicios de Firebase. Luego se debe [ingresar a la consola](https://console.firebase.google.com) y crear un nuevo proyecto._

_Agregue Firebase a su aplicación web copiando y pegando el fragmento indicado en su código HTML. Debe generar este código desde su propia consola de Firebase para poder desarrollar su proyecto con la configuración propia del mismo (su propia apiKey, su propia URL de DB, etc.)._

```
<script src="https://www.gstatic.com/firebasejs/5.8.4/firebase.js"></script>
<script>
  // Initialize Firebase
  var config = {
            apiKey: "AIzaSyCmR0YLhO-s1tdVlW48TvczbqkKmN5hKGc",
            authDomain: "practica-firebase-1a43c.firebaseapp.com",
            databaseURL: "https://practica-firebase-1a43c.firebaseio.com",
            projectId: "practica-firebase-1a43c",
            storageBucket: "practica-firebase-1a43c.appspot.com",
            messagingSenderId: "55386506176"
        }
  firebase.initializeApp(config);
</script>
```

_Este proyecto trabaja con el servicio de Realtime Database de Firebase para el uso de una base de datos en tiempo real. Para crear la base de datos debe ir al apartado Database y luego crear una nueva base de datos desde Realtime Database._

_En este paso es necesario configurar las reglas de seguridad para la DB. Para los fines de este proyecto educativo es necesario habilitar la lectura y escritura para cualquiera que tenga la referencia de la DB._

```
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

_Para acceder a la base de datos de Firebase y trabajar sobre ella debe instanciarla dentro de su script:_

```
db = firebase.database()
```

_Es conveniente generar desde las [herramientas de desarrollo](https://www.npmjs.com/package/firebase-tools?activeTab=versions) los archivos necesarios para trabajar adecuadamente._

_Si quiere instalar las [herramientas de desarrollo](https://www.npmjs.com/package/firebase-tools?activeTab=versions) de Firebase debe abrir una terminal y ejecutar el siguiente comando:_

```
npm i -g firebase-tools
```

_Luego debe autenticarse ejecutando el siguiente comando:_

```
firebase login
```

_Una vez ingresadas sus credenciales, muévase al directorio del proyecto y ejecute el siguiente comando para iniciar un proyecto Firebase y siga los pasos de configuración:_

```
firebase init
```

_Se instalarán todas las dependencias necesarias y se crearán los archivos de configuración. A partir de aquí ya puede comenzar el desarrollo de la aplicación usando Firebase como back-end._

_En algunos casos como puede ser la prueba de autenticaciones será necesario levantar un servidor de desarrollo. Puede instalar [http-server](https://www.npmjs.com/package/http-server) desde una terminal ejecutando el siguiente comando:_

```
npm install http-server -g
```

_Para levantar su servidor http ejecute:_

```
http-server
```

## Ejemplos de uso⚙️

_Este proyecto contiene 5 simples aplicativos que sirven para comprender el uso de Firebase:_

- [Hola Mundo desde Firebase](https://hugo-ff.github.io/Backend-con-Firebase/0_hola-mundo.html)
- [CRUD](https://hugo-ff.github.io/Backend-con-Firebase/1_crud.html) - El ejemplo consiste en una lista de contactos donde se pueden leer los contactos existentes, ingresar nuevos contactos, eliminar contactos, y editar los contactos que ya están en la DB. Todos los cambios se ven reflejados en tiempo real.
- [Autenticación desde redes sociales - GitHub](https://hugo-ff.github.io/Backend-con-Firebase/2_autenticacion_social.html) - La red social habilitada desde la configuración de este proyecto para experimentar en este punto es GitHub.
- [Alta de usuarios y autenticación con correo electrónico](https://hugo-ff.github.io/Backend-con-Firebase/3_autenticacion_email.html)
- [Almacenamiento de archivos en Firebase](https://hugo-ff.github.io/Backend-con-Firebase/4_almacenamiento.html) - Es necesario estar previamente autenticado con correo electrónico o GitHub.

## Construido con 🛠️

* [Firebase](https://firebase.google.com/docs/web/setup?hl=es-419) - El servicio de back-end utilizado.

## Licencia 📄

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE.md](LICENSE.md) para detalles

---

