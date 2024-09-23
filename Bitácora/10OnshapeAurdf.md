# Conversión de ensamble ONSHAPE A URDF
> https://www.youtube.com/watch?v=TJeCpGnX508&t=195s

Primero instalamos 
> sudo pip install onshape-to-robot

luego agregamos el repositorio
> sudo add-apt-repository ppa:openscad/releases

> sudo apt-get update

> sudo apt-get install openscad -y

> sudo apt-get install meshlab -y

luego obtenemos nuestra API key de Onshape por que onshape to robot la necesita de esta pag web https://dev-portal.onshape.com/keys:

The API key's access key is oHISbRJUvbh6Ia6ao682Nn2z and the secret key is DKSkAOk3KgUVR44pqp5R24mw9GGcATouJtPttQjtDVx7oBNG 
Please transfer this securely to your application now as you will not be able to display this secret key string again.

Ahora crearemos un archivo que almacene esta API KEY para no tener que recordarla y tambien para que se pueda leer a traves de otros programas. Este earchivo estara dentro del workspace, dentro de la carpeta src, el archivo se llamara Keys.txt 
Luego dentro del mismo directorio se crea el archivo "keys.sh"
>touch keys.sh
y se le otorgan permisos
>chmod -x keys.sh

Dentro de este archivo se encuentra:
export ONSHAPE_API=https://cad.onshape.com
export ONSHAPE_ACCESS_KEY=oHISbRJUvbh6Ia6ao682Nn2z
export ONSHAPE_SECRET_KEY=DKSkAOk3KgUVR44pqp5R24mw9GGcATouJtPttQjtDVx7oBNG

> luego se da un source al archivo con $ source keys.sh
> despues $ echo ONSHAPE_ACCES_KEY oHISbRJUvbh6Ia6ao682Nn2z

Regresamos a la carpeta source y creamos un paquete
> ros2 pkg create --build-type ament_cmake hexapodLegC_description --dependencies urdf xacro
Después dentro de hexapodLegC_description crear las siguientes carpetas
> mkdir legC

> mkdir legC/config.json

> mkdir launch

> mkdir rviz
Después configurar en json:
> {
"documentId": "7c09b0c31d867776bda81da9", 
"outputformat" :"urdf",
"packageName": "hexapodLegC_description/legC",
"robotName": "hexapod",
"assemblyName":"ensambleC"
}

>donde document id viene en la URL de documento y assembly name es el nombre del ensamble en de documento.
Luego editamos CMakeLists.txt y agregamos las nuevas carpetas
>pip install numpy==1.24

>ejecutamos dentro de la carpeta de description $ onshape-to-robot legC
Despues creamos las siguientes carpetas
>touch launch/legC.launch.py

>touch launch/start_rviz.launch.py

>touch rviz/legC.rviz
