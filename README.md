# Pokédex Angular

[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![codecov](https://codecov.io/gh/keilermora/pokedex-angular/branch/master/graph/badge.svg?token=9E0D28IOFT)](https://codecov.io/gh/keilermora/pokedex-angular)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

[https://keilermora.github.io/pokedex-angular/](https://keilermora.github.io/pokedex-angular/)

La aplicación muestra el listado y el detalle de los Pokémon de las primeras 3 generaciones.

La imagen que representa un Pokémon en el listado muestra las variaciones que estos tuvieron durante las primeras versiones, desde la versión Green (1996) hasta la version Emerald (2005).

Los detalles de un Pokémon individual muestra sus estadísticas base y los registros de la Pokédex de las diferentes versiones.

El proyecto fue desarrollado usando la librería de JavaScript [Angular](https://angular.io/) para crear la interfaz de usuario, en comunicación con la Api RESTful [PokéAPI](https://pokeapi.co/).

## Requisitos mínimos

- [Nodejs](https://nodejs.org) con soporte de largo plazo (LTS).
- Un navegador web

## Ambiente de pruebas

Ejecutar en la raíz del proyecto:

```
npm start
```
## Demo
👉 [Ver aplicación en línea](https://pokedex-delta-ruddy-76.vercel.app/)

## Requisitos
Para desplegar este proyecto necesitas:

- Una cuenta en GitHub → [https://github.com/](https://github.com/)
- Una cuenta en Vercel → [https://vercel.com/](https://vercel.com/)
- Node.js instalado si deseas probarlo localmente → [https://nodejs.org/](https://nodejs.org/)

## Crear una cuenta en GitHub
- Ve a GitHub → [https://github.com/](https://github.com/)
- Haz clic en "Sign up" (Registrarse) en la esquina superior derecha
- Completa el formulario con:
  - Tu correo electrónico
  - Una contraseña segura
  - Un nombre de usuario único

- Resuelve el rompecabezas de verificación cuando aparezca
- Haz clic en "Create account" (Crear cuenta)
- Verifica tu dirección de correo electrónico haciendo clic en el enlace recibido

## Crear una cuenta en Vercel
- Ve a Vercel → [https://vercel.com/](https://vercel.com/)
- Haz clic en "Sign Up" (Registrarse) en la esquina superior derecha
- Recomendamos seleccionar "Continue with GitHub" para vincular ambas cuentas directamente
- Autoriza a Vercel para acceder a tu cuenta de GitHub cuando se solicite
- Completa la información solicitada:
   - Nombre completo
   - Para "I'm creating an account for" selecciona la opción adecuada (Hobby, Work, etc.)
   - Haz clic en "Continue" (Continuar)

## Conectar GitHub con Vercel (si no utilizaste "Continue with GitHub")
- Inicia sesión en tu cuenta de Vercel
- Ve a Settings > Git
- Haz clic en "Connect with GitHub"
- Autoriza a Vercel para acceder a tus repositorios
- Selecciona los repositorios que deseas que estén disponibles en Vercel o permite acceso a todos

## Desplegar la aplicación Pokédex en Vercel
- En el dashboard de Vercel, haz clic en "Add New..." > "Project"
- Selecciona el repositorio de GitHub donde se encuentra tu proyecto Pokédex
- Configuración del proyecto:
   - Framework Preset: Angular
   - Root Directory: Deja en blanco si tu proyecto está en la raíz del repositorio
   - Build Command: ng build --prod (o el comando especificado en tu package.json)
   - Output Directory: dist/pokedex (o la carpeta donde se genera tu build)
   - Environment Variables: No se requieren para este proyecto específico
- Haz clic en "Deploy" y espera a que se complete el proceso
- Una vez finalizado, Vercel te proporcionará una URL para acceder a tu aplicación desplegada

## Cómo se desplegó esta aplicación

1. Se descargó el proyecto original como archivo `.zip`
2. Se descomprimió y subió a un nuevo repositorio en GitHub usando la terminal
3. Se vinculó el repositorio desde Vercel y se desplegó la aplicación

Puedes ver todos los pasos detallados en el archivo [`Despliegue.md`](./Despliegue.md)

## Referencias

- [Angular](https://angular.io/): One framework.
- [Angular Folder Structure](https://angular-folder-structure.readthedocs.io/en/latest/): Create a skeleton structure which is flexible for projects big or small.
- [Font Awesome](https://fontawesome.com/): The web's most popular icon set and toolkit.
- [Normalize.css](https://necolas.github.io/normalize.css/): A modern, HTML5-ready alternative to CSS resets.
- [PokéAPI](https://pokeapi.co/): The RESTful Pokémon API.
