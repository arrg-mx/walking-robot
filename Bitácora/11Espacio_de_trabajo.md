# Creación de nuestro workspace

creación de la carepte de desarrollo ROSNoetic_dev
> mkdir ROSNoetic_dev

creacion del workspace del hexapodo

> cd ROSNoetic_dev

> mkdir hexapod_ws

creacion de la carpeta src dentro del workspace

> cd hexapod_ws

> mkdir src

realizar un colcoin build en el workspace (desde hexapod_ws)
> cd ..

> colcon build

NOTA:en caso de no tener colcon instalado ejecutar desde la carpeta raiz de todo
> cd

> pip3 install colcon-common-extensions

> podemos asegurarnos que se instalo con $colcon --help

Una vez que se ejecuta el colcon en la carpeta del espacio de trabajo surgen las carpetas: build, install, log, src
