## 🛠 Despliegue de la aplicación Pokédex
Este documento describe detalladamente cómo desplegué la aplicación web Pokédex usando GitHub y Vercel, paso a paso, incluyendo todos los comandos y configuraciones especiales utilizadas.

## 1. Subir el proyecto a GitHub 
### Paso 1: Descargar y descomprimir
- Descargué el archivo `.zip` del proyecto Pokédex desde el repositorio original
- Lo descomprimí en una carpeta local en mi computador.

### Paso 2: Subir los archivos a GitHub
#### Inicializar y subir a un nuevo repositorio
- Desde la terminal (dentro de la carpeta del proyecto):

1. Configure mi git bash con mi identidad
     git config --global user.name
     git config --global user.email
3. Inicializar el repositorio:
     git init
4. Añadir todos los archivos:
     git add .
5. Hacer el primer commit:
     git commit -m "Subir carpeta"
6. Crear el repositorio en GitHub desde la web: [https://github.com/new](https://github.com/new)
7. Conectar el repositorio local con GitHub:
     git remote add origin https://github.com/TU_USUARIO/pokedex.git
8. Subir el proyecto a GitHub:
     git push -u origin main

### Paso 3. Desplegar en Vercel
#### Crear cuenta y conectar con GitHub
1. Ingresé a [https://vercel.com/](https://vercel.com/)
2. Me registré con mi cuenta de GitHub
3. Autoricé a Vercel a acceder a mis repositorios
4. Hice clic en **"Add New Project"**
5. Seleccioné el repositorio `pokedex`

## 2. Configuración de despliegue en Vercel
- Vercel detectó automáticamente que el proyecto era Angular. Estas fueron las configuraciones utilizadas:
- **Framework Preset**: Angular
- **Build Command**:
  ```bash
  npm run build -- --configuration=production
  ```
- **Output Directory**:

  ```
  dist/pokedex
  ```
  
> Esta configuración es necesaria porque Angular coloca los archivos generados en la carpeta `dist/`, y dentro de ella en una subcarpeta con el nombre del proyecto.

 ## 3. Ejecutar el despliegue en vercel
- Hice clic en **"Deploy"**, y tras compilar el proyecto, Vercel generó una URL pública para acceder a la aplicación:

🔗 [https://pokedex-delta-ruddy-76.vercel.app/](https://pokedex-delta-ruddy-76.vercel.app/)

## Resultado final
- La aplicación quedó publicada en línea.
- No se usó ningún servidor propio ni configuración avanzada de backend.
- Solo fue necesario GitHub para el control de versiones y Vercel para el hosting automático.

## Notas adicionales
- No fue necesario instalar dependencias localmente ni usar `ng serve`, ya que el despliegue se hizo 100% desde la nube.
- Vercel se encargó de ejecutar automáticamente los comandos de build y hostear los archivos estáticos generados por Angular.

