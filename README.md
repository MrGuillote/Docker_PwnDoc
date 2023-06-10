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
