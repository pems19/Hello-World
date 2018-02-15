Configuracion de drivers para DEVkit 2.0
=============


-	[Introducción](#introducción)

-	[Requisitos](#requisitos)

-	[Paso 1: Controladores FTDI](#paso-1-controladores-ftdi)
-	[Paso 2: Administrador de dispositivos](#paso-2-administrador-de-dispositivos)
-	[Paso 3: Actualización del controlador](#paso-3-actualización-del-controlador)
-	[Paso 4: Configurar USB Serial Port](#paso-4-configurar-usb-serial-port)
-	[Paso 5: Instalación driver CH340 ](#paso-5-instalación-driver-ch340)
-	[Paso 6: Comprobación](#paso-6-comprobación)



Introducción
------------

En esta guía se describen los pasos a seguir para instalar los controladores necesarios para lograr el funcionamiento adecuado del DEVkit V2.0 en un entorno Windows.



Requisitos
------------
- NXTIoT Devkit 
- Sistema Windows 7/8/8.1/10
- Controladores FTDI CDM ([Descarga](http://www.ftdichip.com/Drivers/VCP.htm))
- Controladores CH340    ([Descarga](https://sparks.gogo.co.nz/assets/_site_/downloads/CH34x_Install_Windows_v3_4.zip))


Paso 1: Controladores FTDI
------------
Descargar ([Descarga](http://www.ftdichip.com/Drivers/VCP.htm)) e instalar los controladores FTDI CDM
![ftdi1](https://github.com/pems19/Hello-World/blob/master/pics/ftdi1.png?raw=true)


Paso 2: Administrador de dispositivos
------------

Conectar el DEVkit  al sistema Windows por medio del cable USB.
Abrir el Administrador de dispositivos Panel de control > Hardware y Sonido > Dispositivos e impresoras > Administrador de dispositivos

Dentro de la lista de dispositivos se encuentra un apartado llamado “Otros dispositivos” y contendrá un dispositivo etiquetado como “FT232R USB UART”

![admin01](https://github.com/pems19/Hello-World/blob/master/pics/admin01.png?raw=true)



Paso 3: Actualización del controlador
------------

Presionamos click derecho en el dispositivo “FT232R USB UART” y seleccionamos la opción “Actualizar software de controlador”

En la siguiente ventana elegimos la opción “Buscar software de controlador en el equipo”

A continuación seleccionamos “Elegir en una lista de controladores de dispositivo en el equipo”  

Dentro de la lista del menú de actualización seleccionamos la opción “Universal Serial Bus Controllers” y pulsamos siguiente.

![admin02](https://github.com/pems19/Hello-World/blob/master/pics/admin02.png?raw=true)

En la siguiente ventana seleccionamos en el recuadro de fabricante “FTDI” y modelo “USB Serial Converter” damos click en siguiente.


![admin03](https://github.com/pems19/Hello-World/blob/master/pics/admin03.png?raw=true)

![admin04](https://github.com/pems19/Hello-World/blob/master/pics/admin04.png?raw=true)



Paso 4: Configurar USB Serial Port
------------

Una vez configurado el dispositivo como USB Serial Converter vamos a asignarlo como dispositivo en el puerto serie.
Pulsamos click derecho sobre el dispositivo y seleccionamos la opción “Actualizar software de controlador”
En la siguiente ventana elegimos la opción “Buscar software de controlador en el equipo”
A continuación seleccionamos “Elegir en una lista de controladores de dispositivo en el equipo”   
En el cuadro emergente seleccionamos en el cuadro de fabricante “FTDI” y en modelo “USB Serial Port”

![admin05](https://github.com/pems19/Hello-World/blob/master/pics/admin05.png?raw=true)

![admin06](https://github.com/pems19/Hello-World/blob/master/pics/admin06.png?raw=true)



Paso 5: Instalación driver CH340 
------------
Ahora instalaremos el driver para el Chip de comunicación CH340G  ([Descarga](https://sparks.gogo.co.nz/assets/_site_/downloads/CH34x_Install_Windows_v3_4.zip))
Descomprimir el archivo ZIP en una carpeta, encontraremos 2 carpetas. 

![ch01](https://github.com/pems19/Hello-World/blob/master/pics/ch01.png?raw=true)

Abrimos la carpeta CH341SER que es la que contiene el instalador del driver CH340, y ejecutamos el archivo “SETUP.EXE”
A continuación presionamos el botón “INSTALL” 

![ch02](https://github.com/pems19/Hello-World/blob/master/pics/ch02.png?raw=true)


El programa nos dará la comprobación que el driver fue exitosamente instalado.

![ch03](https://github.com/pems19/Hello-World/blob/master/pics/ch03.png?raw=true)


Paso 6: Comprobación 
------------
En el administrador de dispositivos estará enlistado el DEVkit en la categoría “Ports (COM & LPT)


![comp01](https://github.com/pems19/Hello-World/blob/master/pics/comp01.png?raw=true)

La IDE de Arduino ahora podrá detectar nuestro dispositivo como una placa “Arduino UNO”


![comp02](https://github.com/pems19/Hello-World/blob/master/pics/comp02.png?raw=true)



