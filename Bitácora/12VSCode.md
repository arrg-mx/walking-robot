#Instalación de VS CODE

Visual studio no esta configurado para esta distribución de Ubuntu en Jetson Nano por lo que se deecidio 
usar una conexión Remota desde otro equipo por SSH.

El procedimiento fue 

1. Abrir visual studio code desde otro equipo
2. Instalar la extensión SSH Remote
3. Agregar la nueva conexión SSH como hexapod@192.168.50.197 en Linux
 > para obtener la IP se uso $ hostname -I en la terminal de mi hexapodo
5. Abrir un folder, para verificar que estamos enlazados.
