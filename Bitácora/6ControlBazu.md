
# Reporte Semana 6
Todo esto se realizó en la máquina virtual 
> TSR2024-1


## Deberes
- 1)Integrar los paquetes que hacen falta para poder mover el modelo en RVIZ 
- 2)Mover el modelo en RVIZ

  ## 1)Integrar los paquetes que hacen falta para poder mover el modelo en RVIZ 
En el reporte 4 se realizó la instalación de la carpeta bazu, sin embargo al ejecutar el topico en ROS y RVIZ marca varios errores, por lo que hace falta integrarle otros archivos, estos archivos sirven para tener de manera independiente el effort controller y el position controller.
  De manera que la distribución de archivos dentro de las carpetas queda de la siguiente manera:
![Set Servo ID](/Bitácora/Imágenes/bazulaunch.png)
![Set Servo ID](/Bitácora/Imágenes/bazuurdf.png)
![Set Servo ID](/Bitácora/Imágenes/bazusrc.png)
![Set Servo ID](/Bitácora/Imágenes/bazuconfig.png)

Ahora para compilar debemos ejecutar
> $ catkin_make
Y refrescar la fuente
> $ source devel/setup.bash

  ## 2)Mover el modelo en RVIZ
Debemos enviar el mensaje a través del publicador (por consola con ROS), entonces debemos publicar en dos lados, en rviz y en python para que se simule y se muevan los motores en tiempo real. 

> $ roslaunch bazu position_controller_bazu.launch
Abrir otra terminal para leer los topicos
> $ rostopic list






    

    
