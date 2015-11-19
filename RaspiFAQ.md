* ¿Puede controlar un motor?

* ¿Qué necesito para hacer un robot?

* ¿Dónde puedo comprar en Granada?

* ¿Cuál es el usuario por defecto?

	Es “pi”

* ¿Cuál es la contraseña por defecto del usuario pi?

	Es “raspberry”

* ¿Cuál es la contraseña del usuario root?

	El usuario root no tiene contraseña para evitar acceso indeseados. Para ejecutar algún comando como root podemos usar el comando “sudo”

	sudo comando

	nos solicitará la contraseña del usuario actual

	Si necesitamos por alguna razón permanecer como root (lo cual se desaconseja en todos los Linux) podemos usar 

	sudo su -i

	ó 

	sudo su -

	Cuando acabemos podemos salir con Ctrl-D o con “exit”

* ¿Cómo debo apagar mi raspberry?

La mejor forma de apagarlas es usando el comando  halt

sudo halt 
ó
sudo shutdown -h

* ¿qué significan las luces?

	PWR 	5V alimentación ok
	OK 	Acceso a la SD 
	FDX 	Ethernet Full Duplex conectada
	LNK 	Ethernet conectado
	10M	Ethernet de 100 Mbps conectada

* ¿Qué versión tengo?

	Podemos saber la versión de Raspberry que tenemos usando el siguiente comando

	cat /proc/cpuinfo

	Obtendremos una información similar a esta

	Processor       : ARMv6-compatible processor rev 7 (v6l)
	BogoMIPS        : 847.05
	Features        : swp half thumb fastmult vfp edsp java tls
	CPU implementer : 0x41
	CPU architecture: 7
	CPU variant     : 0x0
	CPU part        : 0xb76
	CPU revision    : 7
	Hardware        : BCM2708
	Revision        : 0002
	Serial          : 000000000abc0ab1

	Según el valor que aparezca en el campo Revision tendremos una versión u otra

	Existen 3 versiones:

	Modelo y Revision		Hardware Revision Code de cpuinfo
	Model B Revision 1.0				0002
	Model B Revision 1.0 + ECN0001 (no fuses, D14 removed)	0003
	Model B Revision 2.0			0004, 0005, 0006




