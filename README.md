# ConéctateGT - Comunidad FunPython & MicroPythonESP32

🤖 Es un evento en línea de un día dónde aprenderás los fundamentos de IoT 🌎

[Transmición en YouTube](https://youtu.be/56bGFpmzRbI)

<p align="center">
  <img width="250" src="media/logo_conectate_gt.png">
</p>

## FunPyhton 

FUNPYTHON ES UNA COMUNIDAD Y RED DE INVESTIGACIÓN E INNOVACIÓN QUE BUSCA UNIR A MENTES CREATIVAS MEDIANTE EL INTERCAMBIO DE IDEAS, EXPERIENCIAS Y
COLABORACIÓNES.

[Triptico informativo sobre Funpython](https://github.com/FunPythonEC/ConectateGT/blob/master/media/FunPython_triptico.pdf)

### Jhon Merchan 🗣️

<p align="center">
  <img width="700" src="media/jhonMerchan_afiche.jpg">
</p>

## MicroPython

<img src="media/upython-with-micro.jpg" width="80%"> 

[Micropython](http://micropython.org/) es una implementacion ligera de python3. creada por el fisico y programador Damien George en 2014 gracias a una exitosa campaña en [Kickstarter](https://www.kickstarter.com/projects/214379695/micro-python-python-for-microcontrollers), junto a la Pyboard, la placa oficial de micropython, desde entonces se ha portado a diferentes plataformas.

A nivel de microcontroladores micropython es un sistema operativo, que incluye un subconjunto de librerias importantes de python (la libreria socket es muy similar a la que usamos en un ordenador)y algunas navitvas para controlar proyectos electronicos, ademas de una sheel interactiva, ademas micropython permite utilizar codigo C++ para optimizar su velocidad. Micropython trata de ser multiplataforma al tener compatiblidad con codigo Python normal y poder enviar tu código de la computadora al microcontrolador con total tranquilidad.

[Más información sobre python y microcontroladores](pythononhardware.funpython,org) 

### _Hola Mundo en Ubuntu 20 vs MicroPython_

<img src="media/holamundo.png" width="100%"> 

## Instalar MicroPython

Guia paso a paso con imagenes para instalar MicroPython y sus prerequisitos.

[Tutorial en Windows 10](https://github.com/FunPythonEC/ConectateGT/blob/master/Instalando_MicroPython.md)

## Instalar librerias y uso del sistema de archivos

Guia paso a paso para instalar la libreria del sensor de temperatura/humedad/presion en el ESP32 y guia para manipular archivos de la memoria del ESP32 utulizando la terminal o CMD. 

[Tutorial para instalar librerias](https://github.com/FunPythonEC/ConectateGT/blob/master/Instalar_librerias.md)

[Tutorial sistema de archivos ESP32](https://github.com/FunPythonEC/ConectateGT/blob/master/sistema_de_archivos.md)

# DEMO

[Ejemplos básicos con MicroPython](https://github.com/FunPythonEC/ConectateGT/blob/master/ejemplos.md)


Cambiar los parametros de credenciales de la red WiFI.

```python
# Informacion de la red WiFi
# Nombre de red y contraseña

WIFI_SSID = ''
WIFI_PASSWORD = ''
```
Cambiar las credenciales para conectar al servidor MQTT.

```python
# Informacion del servidor MQTT
# Cambiar el número del node#

MQTT_URL = b'galiot.galileo.edu' 
MQTT_USER = b'node' 
MQTT_TOPIC = b'temp'

```

### Subscribirse a la paleta de colores para las luces led rgb.

**Anillo de leds RGB**

NeoPixel ring | ESP32
--------------|------
DIN | 25
VCC | +5V
GND | GND

```python
# cantidad de leds rgb y pin de conexión 

num_leds = 10
pin_salida = 25
```
[demo/subscribe_rgb.py](https://github.com/FunPythonEC/ConectateGT/blob/master/mqtt/subscribe_rgb.py)

[demo/neopixel_arcoiris.py](https://github.com/FunPythonEC/ConectateGT/blob/master/demo/neopixel_arcoiris.py)

![Luces, micropython, accion](media/arcoriiris.jpeg)


### Publicar en el servidor MQTT los valores de temperatura y presión.

#### Sensor de temperatura/humedad

BMP180 | ESP32
-------|------
SCL | 22
SDA | 21
VCC | +3V3
GND | GND

```python

i2c = I2C(scl=Pin(22), sda=Pin(21), freq=10000)
```

[demo/publish_bme280.py](https://github.com/FunPythonEC/ConectateGT/blob/master/demo/publish_bme280.py)

[demo/publish_bmep085.py(beta)](https://github.com/FunPythonEC/ConectateGT/blob/master/demo/publish_bmp085.py)



