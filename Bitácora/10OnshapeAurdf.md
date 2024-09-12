# Conversión de ensamble ONSHAPE A URDF
> https://www.youtube.com/watch?v=TJeCpGnX508&t=195s

Primero instalamos 
> sudo pip install onshape-to-robot

luego agregamos el repositorio
> sudo add-apt-repository ppa:openscad/releases

> sudo apt-get update

> sudo apt-get install openscad -y

> sudo apt-get install meshlab .y

luego obtenemos nuestra API key de Onshape por que onshape to robot la necesita de esta pag web https://dev-portal.onshape.com/keys:

The API key's access key is oHISbRJUvbh6Ia6ao682Nn2z and the secret key is DKSkAOk3KgUVR44pqp5R24mw9GGcATouJtPttQjtDVx7oBNG 
Please transfer this securely to your application now as you will not be able to display this secret key string again.

Ahora crearemos un archivo que almacene esta API KEY para no tener que recordarla y tambien para que se pueda leer a traves de otros programas. Este earchivo estara dentro del workspace 
