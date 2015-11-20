# GPIO

![1](./imagenes/GPIORasp.png)

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

Hay que tener cuidado con no equivocarse. Podemos usar una etiqueta

![1](./imagenes/etiquetas.png)

Las distinas versiones tienen algunos pines distintos

![1](./imagenes/GPIOV2.png)

Las versiones de 40 pines

![40](./imagenes/RP2_Pinout.png)

## Librerías

Hay 4 librerías GPIO

* Shell (línea de comandos)
* Rpi. GPIO
* wiringPi (Gordon Henderson wiringpi.com)
* BCM 2835

Veamos como llaman a los distintos pines

![1](./imagenes/NombresGPIO.png)

## Wiring

Para instalarlo tenemos que tener instalado parte del entorno de desarrollo de python

	sudo apt-get install python-dev python-setuptools git-core

Descargamos el código (también podíamos haber descargado el fichero zip)

	git clone git://git.drogon.net/wiringPi

La compilamos

	./build

Y ya podemos udarla 

	gpio readall


![readall](./imagenes/readall.png)

## Conectando un led

Este es el esquema para conectar un led

![led](./imagenes/led.png)

El montaje sería

![esquema](./imagenes/esquemaled.png)

Hagamos un programa que parpadea el led conectado 

	import time
	# Importamos la librería wiringpi
	import wiringpi2
	#Configuramos la numeración de los pines con respecto al
	#estandar de la librería wiringpi (pin de entrada salida 
	#	GPIO0)

	io = wiringpi2.GPIO(wiringpi2.GPIO.WPI_MODE_PINS)

	#Configuramos el pin 0 como salida
	io.pinMode(0,io.OUTPUT)

	# Ciclo for que ejecutamos 3 veces
	for x in range (0,3):
		io.digitalWrite(0,io.HIGH) #encendemos el led
		time.sleep(0.5) # esperamos medio segundo
		io.digitalWrite(0,io.LOW) # apagamos el led
		time.sleep(0.5) # esperamos medio segundo

Para ejecutar estos programas necesitamos permiso de administrador

	sudo python blink.py

# Conectado un pulsador

![pulsador](./imagenes/pulsador.png)

Usando el código

![codigo](./imagenes/codigopulsador.png)