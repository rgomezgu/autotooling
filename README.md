# autotooling
autotools tutorial implementation


AUTOTOOLS

Se trata de una herramienta para la construcción automática de proyectos software, que facilita su portabilidad.

En Enigmedia se utiliza un script de configuración para el core linux, que utiliza las autotools para compilar el core, y utiliza cmake (cmake es una alternativa a las autotools) para generar un paquete debian (.deb) con los ejecutables y librerías que resultan de la compilación.

 

Como paso previo a realizar posibles modificaciones a dicho script, conviene realizar un pequeño tutorial que permita familiarizarse con las autotools.

Se ha realizado un proyecto siguiendo los siguientes tutoriales de autotools:

http://markuskimius.wikidot.com/programming:tut:autotools/

http://www.heiner-eichmann.de/autotools/adding_module.html

El proyecto realizado se ha subido al repositorio, porque tener la solución puede facilitar mucho el trabajo de quien quiera realizar el tutorial por primera vez.

Se trata de un programa "Hola Mundo", que se linka con una librería que calcula la raíz cuadrada de un número.

En realidad en el (primer) tutorial se compila un programa "Hola Mundo" que llama a una función que proporciona los segundos transcurridos desde el 1-1-1970.

Sin embargo se ha decido modificar el proyecto y utilizar los mismos ficheros fuente que se utilizaron en el tutorial de cmake:

a) para mostrar que ambas herramientas permiten hacer lo mismo, y

b) porque un ejecutable que se linka con una librería es un caso muy común.

 

Otros tutoriales recomendados:

https://www.lrde.epita.fr/~adl/dl/autotools.pdf (este es el más completo. Recomendable si hay tiempo)

https://autotools.io/index.html
Guía detallada

Para compilar y empaquetar el siguiente proyecto software, se deben seguir los siguientes pasos:

    Descargar el proyecto del repositorio: https://github.com/rgomezgu/autotooling.git
    cd autotooling
    autoheader (se genera config.h.in)
    automake (se generan los Makefile.in). Para que automake funcione necesita que en el directorio raíz (autotooling) estén presentes los siguientes ficheros: compile, install-sh, missing y decomp. Una forma de generarlos: autoreconf -i.
    autoconf (se genera el script configure)
    ./configure (se generan los Makefile)
    make
    En este momento se ha generado un programa en src que calcula la raíz cuadrada de un número: ./executable 25
    cd src
    ./executable 25
