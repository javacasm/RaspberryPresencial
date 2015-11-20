# GPIO

* Son los pines que podemos usar como salidas o como entradas, pero siempre de tipo digital.
* Utilizan 3.3V
* Podemos configurar cada uno como entrada o como salida
* Algunos de ellos se pueden usar como comunicaciones especializadas: SPI, I2C, UART


# Precauciones

* Antes de realizar cualquier tipo de conexión en los conectores o pines debemos de tener siempre la precaución de tener desconectada la alimentación de la Raspberry Pi. 
* Evitaremos derivaciones eléctricas o cortos .
* Conviene recordar que los pines de la CPU de la placa están conectados directamente a los diferentes conectores y pines, con lo que cualquier cosa que hagamos sobre los pines la estamos haciendo directamente sobre la CPU.
* También hay que tener en cuenta que los pines GPIO no soportan 5 V, sólo 3.3V y un máximo de 16 mA, por lo que hay que tomar precauciones en este sentido.

## Pines

![1](./imagenes/GPIORasp.png)
![1](./imagenes/GPIOv2.png)
![1](./imagenes/NombresGPIO.png)
![1](./imagenes/etiquetas.png)

## Librerías

Hay 4 librerías GPIO

* Shell (línea de comandos)
* Rpi. GPIO
* wiringPi (Gordon Henderson wiringpi.com)
* BCM 2835