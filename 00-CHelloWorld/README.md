# ¿Por dónde empezamos?

Para asegurar una ejecución fluida del programa, es esencial contar con dos elementos clave:

- **Compilador**: Este componente es fundamental para llevar a cabo la ejecución del programa de manera precisa y eficiente.
  
- **Entorno de Desarrollo Integrado (IDE)**: Este software ofrece funcionalidades avanzadas que simplifican el proceso de desarrollo. Proporciona herramientas adicionales y una interfaz intuitiva que mejorará la experiencia del usuario.

Asegurarnos de tener estos dos componentes correctamente configurados es el primer paso para iniciar nuestro proyecto de manera exitosa.

# Instalaciones
## Compilador:
- Antes de comenzar con cualquier instalación es importante aclarar QUÉ es lo que vamos a bajar y POR QUÉ, por lo que resulta fundamental responder la siguiente pregunta: **¿Qué es un compilador y para qué sirve?**
  
  - Un compilador es un programa que traduce código escrito en un lenguaje de programación de alto nivel (en nuestro caso, el lenguaje "C") a un código de máquina el cuál es entendido y ejecutado por la computadora.

- Considerando la definición anteriormente proporcionada, procederemos a instalar el "gcc", uno de los diversos compiladores disponibles para el lenguaje "C":
  
1) Instalaremos el MinGW, el cual resumidamente, es una colección de herramientas para el desarrollo de software en Windows, lo que nos permitirá hacer uso del gcc. Para poder obtener el MinGW haremos uso de MSYS2, una terminal Unix la cual ayudará durante el proceso de instalación del MinGW, para ello [instale la terminal desde aquí.](https://github.com/msys2/msys2-installer/releases/download/2024-01-13/msys2-x86_64-20240113.exe)

2) Una vez descargado, seguiremos las instrucciones proporcionadas por el instalador, sin necesidad de cambiar ninguna ruta o configuración por defecto.
  
3) Finalizado el proceso, debería aparecernos una terminal como la siguiente:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/952e38c0-164c-42a4-933f-fbd14071bc62)

Lo que debemos hacer ahora pegar el siguiente comando: <u>pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain</u>

Este comando nos permitirá instalar el conjunto de herramientas de MinGW para su versión de 64bits, para posteriormente hacer uso del gcc.
Una vez presionado "enter", nos mostrará el siguiente menú:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/5c5241a7-28ea-4ea9-8a50-9b1a53cc9ca5)

Nos permite elegir que dependencias queremos instalar, como queremos instalar todas simplemente presionamos "enter" nuevamente.

![image](https://github.com/Nawel0310/SSL2024/assets/131374182/7e889ed2-f895-427a-b02e-787546beeaa0)
Procedemos con la instalación colocando "Y" y luego "enter".

## Variable de Entorno:
- Una vez instaladas todas las dependencias necesarias, debemos definir una "Variable de Entorno", sin embargo es importante tener en cuenta lo siguiente: **¿Qué es una variable de entorno y por qué debo definir una cuando instalo el MinGW?**
  - Una variable de entorno es básicamente una variable que se configura en el sistema operativo y permite a varios programas acceder a ella en tiempo de ejecución. Estas variables suelen tener información como la configuración del sistema, rutas de acceso a directorios,etc.
  - Para instalar MinGW, es importante definir una variable de entorno, ya que le proporcionamos al sistema la información para encontrar las herramientas propias de MinGW, en nuestro caso, la ubicación del gcc. Sin esta configuración el sistema operativo no podría encontrar las herramientas en cuestión, lo que podría reusltar en errores de compilación.
- Para poder agregar una variable de entorno seguimos los siguientes pasos:
1) Buscamos en Windows "Editar variables de entorno de esta cuenta".
2) Elegimos la variable "Path" y presionamos en "Editar".
3) Ahora presionaremos en "Nuevo" y agregamos la siguiente ruta <u>C:\msys64\ucrt64\bin</u>. Es decir, lo que hacemos acá es agregar la ubicación de la carpeta en donde se encuentra instalado el MinGW.
4) Finalmente le damos a "Aceptar" y nuestra variable de entorno estará definida.
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/8a70033e-1148-49d7-bc49-36cb142cd62a)

## Verificando la versión:




# SSL2024
Código escrito en Visual Studio Code. Compilado con gcc.

1) Salida del programa correcta:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/326de0b8-01d5-46e8-890e-1c8eacc47ad0)

2) Salida del programa mediante un output.txt:
![image](https://github.com/Nawel0310/SSL2024/assets/131374182/5482e5b5-5cbc-40c3-a2ec-a3302a4b0396)
