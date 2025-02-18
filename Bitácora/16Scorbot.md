# REVISIÓN DEL CONTROLADOR SCORBOT QUE ES SIMILAR

1. Descargar archivo
2. Extraer en ROS2DEV
3. revisar en terminal
4. acceder a la carpeta
5.  hacer rm build install y log por que ya estaba compilado previamente con otra computadora y las rutas del cmake interfieren, entonces las borramos.
6.  hacer ~colcon build para crear estas carpeta denuevo y compilar dentro de nuestra ruta.
7.hacer carpeta world dentro de bringup description ya que marcaba error por que se habia borrado en la importacion por estar vacía
8. ~source install/setup.bash
   
10. ~ros2 launch scorbot_bringup trajectory_controller_scorbot.launch.py esto abre gazebo y rviz

    
11. ~ros2 launch scorbot_description scorbot_display.launch.xml abre RVIZ con el controlador de posición


> nota:el paquete del scorbot tiene un jupyter notebook llamado reporte examen, que explica mejor todo.

 ![Scorbot_launch](/Bitácora/Imágenes/scorbot_description display launch.png)


SE HIZO CON EL CONTROLADOR DEL DOFBOT DEL PROFE ERIK

asegurarse de meter los paquetes dentro de una carpeta src, se hizo la instalacion requerida para los controladores segun el ipynb conceptos basicos dentro del paquete en la parte, "configuracion básica de una junta" 

ROBOT SCARA examen description

