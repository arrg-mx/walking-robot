
# Reporte Semana 2
Introducción al driver para los servomotores

## Deberes
- 1)Caracterización de los servomotores (ángulos)
 > **Pendiente**
- 2)Investigación puertos UART RX,TX
- 3)Investigación librería python smbus2
- 4)Prueba de ensamble eslabones

##  1) Caracterización de los servomotores (ángulos)
> **Completado** 

## 2) Investigación puertos UART RX,TX
Un UART es un tipo de circuito integrado que se usa para enviar y recibir datos a través de un puerto serie en un equipo o dispositivo periférico. Los UART son ampliamente utilizados y conocidos por su sencillez. Sin embargo, a diferencia de SPI e I2C, los UART no admiten múltiples dispositivos subordinados.

Un puerto UART (Universal Asynchronous Receiver/Transmitter) es un componente de hardware que permite la comunicación serial entre dispositivos. "RX" significa "Receptor" y "TX" significa "Transmisor".

RX (Receptor): Es el pin de entrada en el que un dispositivo recibe datos de otro dispositivo.
TX (Transmisor): Es el pin de salida en el que un dispositivo envía datos a otro dispositivo.
Por lo tanto, cuando se conectan dos dispositivos a través de un puerto UART, el pin TX de un dispositivo se conecta al pin RX del otro dispositivo, y viceversa. Esta conexión permite la comunicación bidireccional de datos entre los dispositivos. Es común encontrar puertos UART en microcontroladores, módulos de comunicación inalámbrica, dispositivos de IoT, entre otros.

El UART opera de manera asíncrona, lo que significa que no requiere un reloj de sincronización entre el transmisor y el receptor. En lugar de eso, los dispositivos acuerdan de antemano una velocidad de transmisión (baud rate) para la comunicación, lo que determina la duración de cada bit y el intervalo entre bits. Esto permite la comunicación serial entre dispositivos que pueden estar utilizando diferentes relojes o velocidades de procesamiento.


## 3) Investigación librería python smbus2
Comunicación con sensores y dispositivos periféricos: Muchos sensores y dispositivos periféricos utilizan el protocolo SMBus para la comunicación con la CPU u otros componentes de un sistema electrónico. La librería SMBus proporciona una forma de interactuar con estos dispositivos desde el software del sistema.
Monitoreo del sistema: El protocolo SMBus también se utiliza para acceder a información de monitoreo del sistema, como la temperatura, el voltaje y la velocidad del ventilador de la CPU. La librería SMBus permite a los programas acceder a estos datos y realizar acciones basadas en ellos, como ajustar la velocidad del ventilador para mantener la temperatura dentro de límites seguros.
Configuración del sistema: Algunos dispositivos pueden ser configurados a través del protocolo SMBus. Por ejemplo, se pueden ajustar parámetros de funcionamiento o activar características específicas de un dispositivo mediante comandos enviados a través del bus SMBus.

> FUENTE: https://pypi.org/project/smbus2/
> https://www.youtube.com/watch?v=G7aQB6x0LHc

## 4) Prueba de ensamble eslabones

