## 1. Introducción

En la actualidad, el uso de plataformas en la nube se ha convertido en una solución fundamental para el desarrollo, implementación y distribución de aplicaciones web. Una de las herramientas más utilizadas es Microsoft Azure, la cual permite a los desarrolladores desplegar aplicaciones de manera eficiente y escalable.

El presente trabajo describe de manera detallada el proceso de despliegue de una aplicación web desarrollada en Angular, desde la preparación del entorno local hasta su publicación en la nube. Asimismo, se documentan los principales inconvenientes presentados durante el proceso y las soluciones aplicadas.

----------

## 2. Objetivos

### 2.1 Objetivo general

Desplegar una aplicación web en la plataforma Microsoft Azure, comprendiendo cada una de las etapas del proceso.

### 2.2 Objetivos específicos

-   Configurar el entorno de desarrollo local.
-   Instalar y gestionar dependencias del proyecto.
-   Ejecutar la aplicación en un entorno local.
-   Implementar la aplicación en la nube.
-   Identificar y solucionar errores durante el despliegue.

----------

## 3. Desarrollo del proceso

### 3.1 Preparación del entorno de desarrollo

Inicialmente, se realizó la configuración del entorno de trabajo en un sistema operativo Windows. Para ello, se instalaron las siguientes herramientas:

-   Node.js (entorno de ejecución JavaScript).
-   Git (sistema de control de versiones).

Posteriormente, se descargó el proyecto desde un repositorio, el cual contenía una aplicación desarrollada en Angular.

----------

### 3.2 Exploración del proyecto

Una vez descargado el proyecto, se procedió a revisar su estructura de carpetas mediante comandos como:

dir

Durante esta fase se presentó el primer inconveniente:

**Error presentado:**

npm error enoent Could not read package.json

**Causa del error:**  
El comando se estaba ejecutando en una carpeta incorrecta (`source`), donde no existía el archivo necesario para la gestión de dependencias.

**Solución:**  
Se identificó que el proyecto real se encontraba dentro de la carpeta `pokedex-angular`. Al ingresar a dicha carpeta, se encontró correctamente el archivo `package.json`.

----------

### 3.3 Instalación de dependencias

Una vez ubicada la carpeta correcta, se ejecutó el siguiente comando:

npm install

Este proceso permitió instalar todas las dependencias necesarias para la ejecución del proyecto.

----------

### 3.4 Ejecución de la aplicación en entorno local

Posteriormente, se procedió a ejecutar la aplicación en el entorno local mediante:

npm  start

o

npm run build

Esto permitió verificar el correcto funcionamiento de la aplicación antes de su despliegue.

----------

### 3.5 Configuración del repositorio

El proyecto fue gestionado mediante un repositorio en GitHub, configurando las credenciales del usuario y permitiendo el control de versiones del código.

----------

### 3.6 Creación del servicio en Azure

Dentro del portal de Microsoft Azure, se creó un servicio de aplicación (App Service), el cual permite alojar aplicaciones web.

Se configuraron parámetros como:

-   Sistema operativo
-   Entorno de ejecución (Node.js)
-   Plan de servicio

----------

### 3.7 Despliegue de la aplicación

El despliegue se realizó mediante la integración con GitHub, utilizando el Deployment Center de Azure. Esto permitió automatizar el proceso de publicación de la aplicación.

----------

### 3.8 Problemas durante el despliegue

Durante esta etapa se identificaron los siguientes inconvenientes:

#### Problema 1: Error ENOENT

-   **Descripción:** No se encontraba el archivo `package.json`.
-   **Causa:** Ejecución en directorio incorrecto.
-   **Solución:** Ubicación correcta del proyecto.

#### Problema 2: Fallos en la compilación

-   **Causa:** Dependencias no instaladas o scripts mal configurados.
-   **Solución:** Revisión del archivo `package.json`.

#### Problema 3: Ruta incorrecta en Azure

-   **Causa:** El proyecto no estaba en la raíz del repositorio.
-   **Solución:** Configuración adecuada de la ruta o reorganización del proyecto.

----------

### 3.9 Verificación del despliegue

Finalmente, se accedió a la URL publica generada por Azure para verificar que la aplicación funcionara correctamente. Se realizaron pruebas de navegación y funcionamiento general del sistema.

----------

## 4. Conclusión

El despliegue de una aplicación en Microsoft Azure permitió comprender la importancia de la correcta configuración del entorno de desarrollo, la organización de los archivos del proyecto y la gestión de dependencias.

En conclusión, Azure se posiciona como una herramienta eficiente para la publicación de aplicaciones web, siempre y cuando se sigan buenas prácticas en el desarrollo y configuración del proyecto.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5OTQxMTEyMzhdfQ==
-->