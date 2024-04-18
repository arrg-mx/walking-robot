
# Reporte Semana 1
Introducción al driver para los servomotores

## Deberes
- 1)Caracterización de los servomotores (ángulos)

- 2)Investigación puertos UART RX,TX
- 3)Investigación librería python smbus2
- 4)Prueba de ensamble eslabones

##  1) Caracterización de los servomotores (ángulos)
> **Completado** 

## 2) Investigación puertos UART RX,TX
### Esquemático de la tarjeta (Top y Bottom View)


![Jetson_Top](/Bitácora/Imágenes/Schematic_Jetson_Top.png)
![Jetson_Bottom](/Bitácora/Imágenes/Schematic_Jetson_Bottom.png)

### Pinout de [J6] 40-pin Exp Header
![Jetson_J6](/Bitácora/Imágenes/JETSON_J6.png)
### Pinout de [J7] Fan Header
![Jetson_J7](/Bitácora/Imágenes/JETSON_J7.png)
### Pinout de [J11] Optional Alternate Button Header
![Jetson_J11](/Bitácora/Imágenes/JETSON_J11.png)
### Pinout de [J12] Button Header
![Jetson_J5](/Bitácora/Imágenes/JETSON_J12.png)




>  FUENTE: https://developer.nvidia.com/embedded/learn/jetson-nano-2gb-devkit-user-guide#id-.JetsonNano2GBDeveloperKitUserGuidevbatuu_v1.0-Introduction


## 3) Investigación librería python smbus2
### Esquemático del driver
![DRIVER_SERVO](/Bitácora/Imágenes/DRIVER_SERVO.png)
### Instalación del driver CH340
Es necesario para detectar el puerto COM

![CH340](/Bitácora/Imágenes/CH340DRIVER.png)
### Inicializar motores
 Double-click to open the servo debugging software. Click [Settings]-- [Serial Port Settings] to select the corresponding port number, the baud rate is 115200, and finally click [Open Port].


![SERVODEBUG](/Bitácora/Imágenes/Servo_DEBUG.png)

>  FUENTE: http://www.yahboom.net/study/YB-SD15M
## 4) Prueba de ensamble eslabones
