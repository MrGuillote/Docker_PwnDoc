# Docker_PwnDoc
instalacion de la tool

## Instalación de Docker

### Windows:

1. Ve al sitio web oficial de Docker para Windows: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
2. Haz clic en "Download Docker Desktop for Windows" para descargar el instalador.
3. Ejecuta el instalador descargado y sigue las instrucciones del asistente de instalación.
4. Una vez instalado, Docker se iniciará automáticamente.

### macOS:

1. Ve al sitio web oficial de Docker para Mac: [https://www.docker.com/products/docker-desktop](https://www.docker.com/products/docker-desktop)
2. Haz clic en "Download Docker Desktop for Mac" para descargar el instalador.
3. Ejecuta el instalador descargado y sigue las instrucciones del asistente de instalación.
4. Una vez instalado, Docker se iniciará automáticamente.

### Linux:

La instalación de Docker en Linux puede variar según la distribución específica que estés utilizando. A continuación, se muestra un resumen general de los pasos:

- Para distribuciones basadas en Debian (como Ubuntu):
  - Abre una terminal y ejecuta los siguientes comandos:
    ```
    sudo apt update
    sudo apt install docker.io
    sudo systemctl start docker
    sudo systemctl enable docker
    ```

- Para distribuciones basadas en Red Hat (como CentOS, Fedora):
  - Abre una terminal y ejecuta los siguientes comandos:
    ```
    sudo dnf update
    sudo dnf install docker
    sudo systemctl start docker
    sudo systemctl enable docker
    ```

- Para otras distribuciones de Linux, consulta la documentación oficial de Docker para obtener instrucciones específicas.

Después de instalar Docker, verifica que esté funcionando correctamente ejecutando el siguiente comando en una terminal:



# PWNDOC: GENERADOR DE INFORMES PENTEST

PwnDoc es una aplicación de informe de pentest que simplifica y facilita la escritura de tus hallazgos y la generación de informes personalizables en formato Docx.

El objetivo principal es tener más tiempo para Pwn y menos tiempo para Doc al compartir datos como vulnerabilidades entre los usuarios.

## Documentación

- [Instalación](#instalación)
- [Datos](#datos)
- [Vulnerabilidades](#vulnerabilidades)
- [Auditorías](#auditorías)
- [Plantillas](#plantillas)

## Características

- Soporte para múltiples idiomas.
- Soporte para múltiples fuentes de datos.
- Gran capacidad de personalización.
- Gestión de datos de auditoría y vulnerabilidades reutilizables.
- Creación de secciones personalizadas.
- Adición de campos personalizados a las vulnerabilidades.
- Gestión de vulnerabilidades.
- Generación de informes para múltiples usuarios.
- Generación de informes en formato Docx.
- Personalización de la plantilla de informe Docx.

## Instalación

PwnDoc utiliza 3 contenedores: el backend, el frontend y la base de datos.

### Producción

Para utilizar PwnDoc en producción, asegúrate de seguir estos pasos:

1. Cambia el secreto JWT en el archivo `src/lib/auth.js`.
2. Actualiza los certificados en la carpeta `ssl`.

A continuación, puedes construir y ejecutar los contenedores Docker:

```bash
docker-compose up -d --build
    ```

Mostrar los registros del contenedor backend:
    ```
docker-compose logs -f pwndoc-backend
    ```
Detener los contenedores:
    ```
docker-compose stop
    ```
Arrancar los contenedores:
    ```
docker-compose start
    ```
Eliminar los contenedores:
    ```
docker-compose down
    ```
Actualizar la aplicación:
    ```
docker-compose down
    ```
git pull
docker-compose up -d --build
    ```
La aplicación estará disponible en https://localhost:8443 y la API en https://localhost:4242/api. Si utilizas Firefox, deberás añadir una excepción de certificado para el backend. Para ello, ve a https://localhost:4242/api/users/init.

Desarrollo
Para propósitos de desarrollo, puedes utilizar un archivo docker-compose específico en cada carpeta (backend/frontend).

El código fuente puede ser modificado en vivo y la aplicación se recargará automáticamente con los cambios.

A continuación, puedes construir y ejecutar los contenedores de backend y base de datos:
    ```
docker-compose -f backend/docker-compose.dev.yml up -d --build
    ```
Mostrar los registros del contenedor backend:
    ```
mpose -f backend/docker-compose.dev.yml logs -f pwndoc-backend
    ```
Detener el contenedor:
    ```
docker-compose -f backend/docker-compose.dev.yml stop
    ```
Arrancar el contenedor:
    ```
docker-compose -f backend/docker-compose.dev.yml start
    ```
Eliminar los contenedores:
    ```
docker-compose -f backend/docker-compose.dev.yml down
    ```
La aplicación estará disponible en http://localhost:8081 y la API en `https://localhost:525
