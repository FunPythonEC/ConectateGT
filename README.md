# ConéctateGT - Comunidad Funython & MicroPythonESP32

🤖 Es un evento en línea de un día dónde aprenderás los fundamentos de IoT 🌎

<p align="center">
  <img width="250" src="media/logo_conectate_gt.png">
</p>
<br />

## Jhon Merchan en FunPython 


<p align="center">
  <img width="400" src="media/jhonMerchan_afiche.jpg">
</p>
<br />

![Triptico informativo sobre Funpython](media/FunPython_triptico.pdf)


## MicroPython

<img src="media/upython-with-micro.jpg" width="80%"> 

[Micropython](http://micropython.org/) es una implementacion ligera de python3. creada por el fisico y programador Damien George en 2014 gracias a una exitosa campaña en [Kickstarter](https://www.kickstarter.com/projects/214379695/micro-python-python-for-microcontrollers), junto a la Pyboard, la placa oficial de micropython, desde entonces se ha portado a diferentes plataformas.

A nivel de microcontroladores micropython es un sistema operativo, que incluye un subconjunto de librerias importantes de python (la libreria socket es muy similar a la que usamos en un ordenador)y algunas navitvas para controlar proyectos electronicos, ademas de una sheel interactiva, ademas micropython permite utilizar codigo C++ para optimizar su velocidad. Micropython trata de ser multiplataforma al tener compatiblidad con codigo Python normal y poder enviar tu código de la computadora al microcontrolador con total tranquilidad.


### _Hola Mundo en Ubuntu 20 vs MicroPython_

<img src="media/holamundo.png" width="100%"> 

## Instalar MicroPython

Guia paso a paso con imagenes para instalar MicroPython y sus prerequisitos.

[Tutorial en Windows 10](https://github.com/FunPythonEC/ConectateGT/blob/master/Instalando_MicroPython.md)

## Isntalar librerias y sistema de archivos

Guia paso a paso para instalar la libreria del sensor de temperatura/humedad/presion en el ESP32 y guia para manipular archivos de la memoria del ESP32 utulizando la terminal o CMD. 


[Tutorial para instalar librerias](https://github.com/FunPythonEC/ConectateGT/blob/master/Instalar_librerias.md)

[Tutorial sistema de archivos ESP32](https://github.com/FunPythonEC/ConectateGT/blob/master/sistema_de_archivos.md)

# DEMO


Cambiar los pines de conexión de los sensores y luces.

```python
# linea 10 - 11
# cantidad de leds rgb y pin de conexión 

num_leds = 50
pin_salida = 17

# linea 12 pines de I2C

i2c = I2C(scl=Pin(22), sda=Pin(23), freq=10000)

```

Cambiar los parametros de credenciales de la red WiFI.

```python
# linea 35 - 36
# Informacion de la red WiFi

WIFI_SSID = ''
WIFI_PASSWORD = ''
```

Cambiar las credenciales para conectar al servidor MQTT.


```python
# linea 35 - 36
# Informacion del servidor MQTT
# Cambiar el numero del node#

MQTT_URL = b'galiot.galileo.edu' 
MQTT_USER = b'node' 
MQTT_TOPIC = b'temp'

```


Publicar en el servidor MQTT los valores de temperatura y presión.

[mqtt/publish.py](https://github.com/FunPythonEC/ConectateGT/blob/master/mqtt/publish.py)

Subscribirse a la paleta de colores para las luces led rgb.

[mqtt/subscribe.py](https://github.com/FunPythonEC/ConectateGT/blob/master/mqtt/publish.py)
