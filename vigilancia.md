# Raspberry Pi: Introducción al uso y programación ([162319GE102](https://www.juntadeandalucia.es/educacion/seneca/seneca/jsp/gestionactividades/DetActForPub.jsp?X_EDIACTFOR=161807))

## CEP de Linares-Andújar

11, 12 y 17 de Mayo de 2016

![CC](./imagenes/Licencia_CC.png)
## José Antonio Vacas  @javacasm

### [https://github.com/javacasm/RaspberryLinares](https://github.com/javacasm/RaspberryLinares)

# Vigilancia

Podemos usar su cámara (la original o una USB)

Usaremos un software standard de Linux: motion

	sudo apt-get install motion

Editamos la configuracion

	sudo nano /etc/motion/motion.conf

![motion](./imagenes/motion.jpg)

Lo arrancamos

	sudo montion -n


Podremos acceder a la imagen en vivo de la cámara con

	 http://rasperry_ip:8001
