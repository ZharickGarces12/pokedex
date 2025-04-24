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
  ```bash
   git config --global user.name
  ```
 ```bash
     git config --global user.email
 ```
3. Inicializar el repositorio:
    ```bash
     git init
     ```
5. Añadir todos los archivos:
    ```bash
     git add .
     ```
7. Hacer el primer commit:
    ```bash
     git commit -m "Subir carpeta"
     ```
9. Crear el repositorio en GitHub desde la web: [https://github.com/new](https://github.com/new)
10. Conectar el repositorio local con GitHub:
     ```bash
     git remote add origin https://github.com/ZharickGarces12/pokedex.git
      ```
12. Subir el proyecto a GitHub:
     ```bash
     git push -u origin main
      ```

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

## Cabeceras HTTP de Seguridad
1. X-Frame-Options: SAMEORIGIN
   - Previene que la página sea cargada dentro de un iframe (un marco dentro de una página web), lo que ayuda a prevenir ataques de clickjacking.
2. X-Content-Type-Options: nosniff
   - Impide que el navegador intente adivinar el tipo de contenido de una respuesta. Esto previene vulnerabilidades como la ejecución de archivos maliciosos si el servidor no define un tipo MIME correctamente.
3. Referrer-Policy: strict-origin-when-cross-origin
   - Controla la información que se envía en el encabezado Referer cuando se navega desde una página a otra. Con strict-origin-when-cross-origin, solo se envía el origen del referidor en solicitudes a 
   dominios distintos.
4. Strict-Transport-Security: max-age=63072000; includeSubDomains; preload
   - Fuerza el uso de HTTPS (conexión segura) en el sitio web, lo que ayuda a prevenir ataques de man-in-the-middle. El valor max-age=63072000 asegura que esta política se aplique durante dos años.
5. Permissions-Policy
   - Controla qué permisos puede solicitar la página web, como acceso a la cámara, ubicación o micrófono. Los permisos aquí están deshabilitados para todas las funciones listadas.
6. Cross-Origin-Opener-Policy: same-origin
   - Aísla el contexto de navegación de la página actual de otras páginas de diferentes orígenes para evitar ciertos ataques, como la ejecución de scripts maliciosos.
7. Cross-Origin-Resource-Policy: same-origin
   - Evita que recursos de diferentes orígenes puedan ser accesados por otras páginas, mejorando la seguridad frente a ataques de recursos compartidos entre dominios.
8. Cross-Origin-Embedder-Policy: require-corp
   - Requiere que los recursos externos, como scripts o imágenes, vengan de orígenes que permitan ser cargados, ayudando a proteger contra ciertos tipos de ataques.
9. Cache-Control: no-store, max-age=0
   - Controla cómo se almacenan en caché las respuestas. no-store significa que no se debe almacenar en caché, y max-age=0 indica que la respuesta debe ser considerada como caducada inmediatamente.
10. Content-Security-Policy
   - Te da control total sobre de dónde y qué tipo de contenido se puede cargar en tu web. Es una capa esencial de defensa para proteger a los usuarios y evitar que scripts externos maliciosos se ejecuten.
 

