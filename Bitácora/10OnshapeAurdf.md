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
> ros2 pkg create --build-type ament_cmake hexapod_description --dependencies urdf xacro

Después dentro de hexapodLegC_description crear las siguientes carpetas
> mkdir legC

> mkdir legC/config.json

> mkdir launch

> mkdir rviz
Después configurar en json:
> {
"documentId": "7c09b0c31d867776bda81da9", 
"outputformat" :"urdf",
"packageName": "hexapod_description/hexapodv1",
"robotName": "hexapod",
"assemblyName":"ensambleC"
}

>donde document id viene en la URL de documento y assembly name es el nombre del ensamble en de documento.
Luego editamos CMakeLists.txt y agregamos las nuevas carpetas
install(
  DIRECTORY 
    rviz
    launch
    hexapodv1
  DESTINATION
    share/${PROJECT_NAME}/
)
>antes del ament_package()


>pip install numpy==1.24

>ejecutamos dentro de la carpeta de description $ onshape-to-robot legC
Despues creamos las siguientes carpetas

>touch launch/hexapodv1.launch.py

>touch launch/start_rviz.launch.py

>touch rviz/hexapodv1.rviz

Dentro del archivo hexapodv1.launch.py ingresamos el siguiente codigo:

    import os
    from launch import LaunchDescription
    from launch_ros.actions import Node

    #Función que el sistema de lanzamiento buscará
    def generate_launch_description():

    ####### ENTRADAS DE DATOS #####
    urdf_file = 'robot.urdf'
    package_description = "hexapod_description"

    ###### FIN DE ENTRADAS DE DATOS #####
    print("Fetching URDF ==>")
    
    # Ruta correcta al archivo URDF en la carpeta 'src'
    robot_desc_path = os.path.join(
        '/home/tsmusr/ROS2Dev/hexapod_ws/src',  # Ruta fija a src
        package_description, 'hexapodv1', urdf_file  # Combinación correcta de directorios
    )

    # Verifica si el archivo URDF existe
    if not os.path.exists(robot_desc_path):
        raise FileNotFoundError(f"El archivo URDF no se encuentra en la ruta: {robot_desc_path}")

    # Nodo de Robot State Publisher
    robot_state_publisher_node = Node(
        package="robot_state_publisher",
        executable="robot_state_publisher",
        name="robot_state_publisher_node",
        emulate_tty=True,
        parameters=[{'use_sim_time': True,
                     'robot_description': open(robot_desc_path).read()}],  # Leer directamente el archivo URDF
        output="screen"
    )

    # Crear y devolver el objeto de descripción de lanzamiento
    return LaunchDescription(
        [
            robot_state_publisher_node
        ]
    )


LUEGO en el archivo start_rviz.launch

    import os

    from ament_index_python.packages import get_package_share_directory
    from launch import LaunchDescription
    from launch.substitutions import Command
    from launch_ros.actions import Node

    #this is the function launch system will look for

    def generate_launch_description():
    
    package_description="hexapod_description"

    #RVIZ Configuration
    rviz_config_dir = 
             os.path.join(get_package_share_directory(package_description),'rviz','hexapod.rviz')

     rviz_node = Node(
        package='rviz2',
        executable='rviz2',
        output='screen',
        name='rviz_node',
        parameters=[{'use_sim_time':True}],
        arguments=['-d',rviz_config_dir]
    )

    #create and return launch description object
    return LaunchDescription(
        [
            rviz_node
        ]
    )


FINALMENTE Compilamos desde hexapod_ws
>source install/setup.bash

>colcon build --packages-select hexapod_description

>source install/setup.bash

>ros2 launch hexapod_description hexapodv1.launch.py

Se abre otra terminal

>source install/setup.bash

>ros2 launch hexapod_description start_rviz.launch.py

se abre otra terminal

>source install/setup.bash

>ros2 run joint_state_publisher_gui joint_state_publisher_gui 
