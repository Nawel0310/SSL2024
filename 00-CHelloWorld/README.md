# ¿Por dónde empezamos?

Para asegurar una ejecución fluida del programa, es esencial contar con dos elementos clave:

- **Compilador**: Este componente es fundamental para llevar a cabo la ejecución del programa de manera precisa y eficiente.
  
- **Entorno de Desarrollo Integrado (IDE)**: Este software ofrece funcionalidades avanzadas que simplifican el proceso de desarrollo. Proporciona herramientas adicionales y una interfaz intuitiva que mejorará la experiencia del usuario.

Asegurarnos de tener estos dos componentes correctamente configurados es el primer paso para iniciar nuestro proyecto de manera exitosa.

# Instalaciones
## Compilador:
Antes de comenzar con cualquier instalación es importante aclarar QUÉ es lo que vamos a bajar y POR QUÉ, por lo que resulta fundamental responder la siguiente pregunta: **¿Qué es un compilador y para qué sirve?**
  
  - Un compilador es un programa que traduce código escrito en un lenguaje de programación de alto nivel (en nuestro caso, el lenguaje "C") a un código de máquina el cuál es entendido y ejecutado por la computadora.

- Considerando la definición anteriormente proporcionada, procederemos a instalar el "gcc", uno de los diversos compiladores disponibles para el lenguaje "C":
  
1) Instalaremos el MinGW, el cual resumidamente, es una colección de herramientas para el desarrollo de software en Windows, lo que nos permitirá hacer uso del gcc. Para poder obtener el MinGW haremos uso de MSYS2, una terminal Unix la cual ayudará durante el proceso de instalación del MinGW, para ello [instale la terminal desde aquí](https://github.com/msys2/msys2-installer/releases/download/2024-01-13/msys2-x86_64-20240113.exe).

2) Una vez descargado, seguiremos las instrucciones proporcionadas por el instalador, sin necesidad de cambiar ninguna ruta o configuración por defecto.
  
3) Finalizado el proceso, debería aparecernos una terminal como la siguiente:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/d8d538d6-05cc-4fea-9c73-166471c3c212)

Lo que debemos hacer ahora pegar el siguiente comando: <u>pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain</u>

Este comando nos permitirá instalar el conjunto de herramientas de MinGW para su versión de 64bits, para posteriormente hacer uso del gcc.
Una vez presionado "enter", nos mostrará el siguiente menú:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/f78dbf38-4e6c-4673-b58a-6622916e93f6)

Nos permite elegir que dependencias queremos instalar, como queremos instalar todas simplemente presionamos "enter" nuevamente.

![image](https://github.com/Nawel0310/SSL2024/assets/131374182/7e889ed2-f895-427a-b02e-787546beeaa0)
Procedemos con la instalación colocando "Y" y luego "enter".

## Variable de Entorno:
Una vez instaladas todas las dependencias necesarias, debemos definir una "Variable de Entorno", sin embargo es importante tener en cuenta lo siguiente: **¿Qué es una variable de entorno y por qué debo definir una cuando instalo el MinGW?**
 - Una variable de entorno es básicamente una variable que se configura en el sistema operativo y permite a varios programas acceder a ella en tiempo de ejecución. Estas variables suelen tener información como la configuración del sistema, rutas de acceso a directorios,etc.
- Para instalar MinGW, es importante definir una variable de entorno, ya que le proporcionamos al sistema la información para encontrar las herramientas propias de MinGW, en nuestro caso, la ubicación del gcc. Sin esta configuración el sistema operativo no podría encontrar las herramientas en cuestión, lo que podría reusltar en errores de compilación.
- Para poder agregar una variable de entorno seguimos los siguientes pasos:
  
1) Buscamos en Windows "Editar variables de entorno de esta cuenta".
2) Elegimos la variable "Path" y presionamos en "Editar".
3) Ahora presionaremos en "Nuevo" y agregamos la siguiente ruta: _C:\msys64\ucrt64\bin_. Es decir, lo que hacemos acá es agregar la ubicación de la carpeta en donde se encuentra instalado el MinGW.
4) Finalmente le damos a "Aceptar" y nuestra variable de entorno estará definida.
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/8a70033e-1148-49d7-bc49-36cb142cd62a)

## Verificando la versión:
- Vamos a verificar la versión del gcc que instalamos. Para ello abrimos cualquier terminal (en este caso, el CMD de Windows), e introducimos el comando: _gcc --version_.

![image](https://github.com/Nawel0310/SSL2024/assets/131374182/3b4cdcad-5076-434d-848a-4bf77d59d180)

- En nuestro caso, tenemos la versión 8.1.0, el cual implementa el estándar C11 del lenguaje C. Esta estandarización posee características importantes al lenguaje, como la mejora en la biblioteca estándar, el soporte para alineación en memoria, tipos de datos genéricos y threads. Para mayor información consultar [este enlace](https://devdocs.io/c/11).

## Instalando el IDE
- Instalaremos un IDE, el cual resumidamente es un software que proporciona un conjunto completo de herramientas para desarrollar software en un único entorno. Lo que nos facilitara el trabajo considerablemente. En nuestro caso instalaremos Visual Studio Code.
- Para instalar VSC seguiremos los siguientes pasos:
  
1) Descargaremos el programa desde [este enlace](https://code.visualstudio.com/download).
2) Seguimos los pasos de instalación proporcionados por el instalador.
Si seguimos todos los pasos correctamente, deberíamos ver una interfaz similar a la siguiente:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/57af47df-dd1f-4f73-82f1-456555a72b5a)
3) Una vez instalado el IDE, nos iremos a la parte de extensiones (Ctrl + Shift + X) e instalaremos la extensión "C/C++ extension for VS Code", la cual es una herramienta que nos proporcionan un conjunto de características que permiten facilitar el desarrollo en programas hechos con C y C++ (permitiendonos resaltar la sintaxis, autocompletado, debuggear, integración con el gcc, etc).
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/53f5a6ea-d0bf-4997-9480-ae6cc23f98ec)
Con todo esto ya configurado y listo, procederemos a ejecutar nuestro programa, tanto en consola como en un archivo de texto.

## Compilando el Programa
Finalmente vamos a ejecutar nuestro "Hola Mundo":
- Lo primero será clonar este repositorio de manera local. Para ello nos ubicaremos en el directorio en donde querramos clonar nuestro proyecto (con el comando "cd <ruta>" podemos especificar en que ruta pararnos). Hecho esto haremos uso del comando git clone <URL de este repositorio>

IMPORTANTE: Debemos estar parados en la rama "master" para poder visualizar de manerca correcta nuestro proyecto. Si no lo estamos, podemos usar el comando "git checkout master" y ya estaríamos en la rama correspondiente.
Si seguimos los pasos de manera correcta, deberíamos estar viendo lo siguinte en nuestro IDE:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/b81392bf-fbe8-43c1-8a2e-6bda2a1cf3ad)

Ahora vamos a compilar el programa.
- Para ello, hacemos click en el botón superior de "Run C/C++ File":
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/95012d90-1bca-42da-afdb-5cf6d7738822)
- Nos pedirá elegir un compilador. Elegiremos el "gcc" que instalamos previamente (suele ser la primera opción):
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/590c0c26-a9a2-460e-9ba0-9e9e5f6de4a6)
- Ahora compilara nuestro programa y si todo salió de manera correcta, la consola nos mostrará dos mensajes, uno de confirmación y otro con la salida esperada:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/cf281641-d63f-41e7-8cc4-f85b52e4116e)
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/39b48bd4-98bc-4535-bb15-0072b3cff446)

IMPORTANTE: Al compilar el proyecto por primera vez se creará un ejecutable llamado "hello.exe". Este archivo contiene todas las instrucciones en lenguajes de máquina para que nuestra computadora pueda llevar a cabo su ejecución. Inclusive podemos ejecutar este programa únicamente desde una terminal, por ejemplo con el CMD de Windows:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/7c083e86-6e9a-4462-b67d-8d49d6c1574c)

## Salida mediante un .txt
- También existe la posibilidad redirigir la salida de nuestro programa a un archivo con extensión ".txt". Para ello, desde cualquier terminal, nos paramos en la ruta de nuestro proyecto y ejecutamos el comando "hello.exe > output.txt". El operador ">" indica a dponde debe redirigirse la salida del programa, (no importa si borramos este archivo, puesto que al momento de ejecutar el comando para redirigir la salida, en caso de que no exista, se creará).
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/311066f1-13b4-4645-afc7-0e877161994c)
