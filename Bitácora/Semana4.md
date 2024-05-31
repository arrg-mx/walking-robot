
# Reporte Semana 4
Control de servomotores

## Deberes
- 1)Conexion de servo a la tarjeta Jetson
- 2)Instalación de ROS Noetic en Jetson
  > Pendiente

-3)Instalacion de máquina virtual con ROS Noetic para continuar con la programación.


  ## 1)Conexion de servo a la tarjeta Jetson
### Conexion puerto serie del driver a la Jetson
![ConexionServoSerial](/Bitácora/Imágenes/WiringServoJetson.png)
### Pinout Servo
![PinoutServo](/Bitácora/Imágenes/PinMotorServo.png)

 > Nota: 
 Tuve que instalar  *$ pip3 install pyserial* en la terminal de la jetson y ademas agregar en la primera celda del Jupyternotebook *!pip3 install pyserial*


  ## 3)Instalacion de máquina virtual con ROS Noetic para continuar con la programación.

Se instaló la máquina virtual Semestre 2024-1

A continuación se desarrollará a partir del siguiente repositorio:
> https://github.com/noshluk2/ROS2-Ultimate-guide-for-Custom-Robotic-Arms-and-Panda-7-DOF/tree/master/bazu

Contiene tutoriales para desarrollar un brazo robótico. 

1. Abrir terminal y activar ROS Noetic
   > rosact ros1
3. Entrar a carpeta de desarrollador ROSDev
4. Crear espacio de trabajo
  > $ mkdir -p bazu_ws/src
4. Entrar al espacio de trabajo y compilar
  > $ cd bazu_ws

  > $ catkin_make

5.Entrar a la carpeta src y crear el paquete description y agregar la libreria rospy
  > $ catkin_create_pkg bazu_description rospy

6. Descargar la carpeta de github y copiar los archivos dentro de bazu a nuestra carpeta local de bazu_ws/src
7. Regresar a la carpeta del espacio de trabajo y hacer un catkin
  > $ catkin_make

8. Agregar alias
   >$ cd
   
   >$ gedit .bash_aliases
9. Dentro del bash_aliases añadir la linea y guardar el archivo
   > source ~/ROSDev/bazu_ws/devel/setup.bash
10. Probamos que el paquete funciona, entramos a ROSDev/bazu_ws_devel y ejecutamos
    >$ roslaunch bazu joint_trajectory_controller_bazu.launch







    

    

