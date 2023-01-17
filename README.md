# 29-ESP32CAM-MQTT-Basic

# Introducción

Arduino IDE es un Entorno de Desarrollo Integrado (IDE) para programar y desarrollar proyectos con placas Arduino. Incluye un editor de código, un compilador y una herramienta de carga para facilitar el proceso de escribir, depurar y cargar código en las placas Arduino. Además, Arduino IDE viene con una gran cantidad de bibliotecas y ejemplos pre-instalados que ayudan a los desarrolladores a empezar rápidamente con sus proyectos.

# Material Necesario

- [Instalar y Configurar Arduino IDE](https://github.com/RaulToribio/23-Instalar-y-Configurar-Arduino-IDE)

# Material de Referencia

- [Configuración del IDE para ESP32-CAM](https://edu.codigoiot.com/course/view.php?id=850)

# Instrucciones

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(1).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(1).png)

Dirigirse al menú “Sketch - Include Library”.

Seleccionar “Manage Libraries”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(2).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(2).png)

Buscar la biblioteca “PubSubClient - Nick O’ Leary”.

Clic en “Install”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(3).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(3).png)

Se habrá instalado la biblioteca.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(4).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(4).png)

Modificar los datos de red.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(5).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(5).png)

Utilizar la línea de comando `ifconfig`.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(6).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(6).png)

Obtener la dirección IP de nuestra máquina virtual.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(7).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(7).png)

Modificar la dirección IP del programa.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(8).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(8).png)

Utilizar la línea de comando `systectl status mosquitto` para conocer el estado de Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(9).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(9).png)

Mosquitto se encuentra activo.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(10).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(10).png)

Cargar el programa.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(11).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(11).png)

Presionar el botón “Reset” del ESP32CAM.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(12).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(12).png)

Se habrá conectado el ESP32CAM a la red.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(13).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(13).png)

En el monitor serial aparecerá #Error rc=-2”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(14).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(14).png)

Dirigirse a la página web del archivo de configuración de [Mosquitto](https://mosquitto.org/man/mosquitto-conf-5.html).

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(15).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(15).png)

Identificar el archivo “mosquitto.conf.gz” en la carpeta “/usr/share/doc/mosquitto/examples”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(16).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(16).png)

Abrir el archivo.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(17).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(17).png)

Clic en “Extract”.

Extraer en “Desktop”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(18).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(18).png)

Clic en “Show The Files”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(19).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(19).png)

Se abrirá la carpeta “Desktop”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(20).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(20).png)

Utilizar la línea de comando sudo `cp ~/Desktop/mosquitto.conf /etc/mosquitto/conf.d/mosquitto.conf` para copiar el archivo extraido en “Desktop” a “/etc/mosquitto/conf.d/”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(21).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(21).png)

Ingresar contraseña.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(22).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(22).png)

Ingresar la línea de comando `sudo nano /etc/mosquitto/conf-d/conquitto.conf` para modificar el archivo.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(23).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(23).png)

Se abrirá el editor de texto en terminal.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(24).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(24).png)

Descomentar “allow_anonymous true”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(25).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(25).png)

Descomentar “listener 1883 0.0.0.0”.

Esto permitirá recibir y enviar datos a través del puerto 1883 a cualquier dispositivo en la red local.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(26).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(26).png)

Presionar la combinación de teclas “Ctrl + O” para guardar los cambios.

Presionar la combinación de teclas “Ctrl + X” para salir del editor de texto en terminal.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(27).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(27).png)

Utilizar el la línea de comando `systemctl status mosquitto` para conocer el estado de Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(28).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(28).png)

Mosquitto se encuentra activo.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(29).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(29).png)

Utilizar la línea de comando `systemctl stop mosquitto` para detener Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(30).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(30).png)

Ingresar contraseña.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(31).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(31).png)

Se habrá detenido Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(32).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(32).png)

Utilizar el la línea de comando `systemctl status mosquitto` para conocer el estado de Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(33).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(33).png)

Mosquitto se encuentra inactivo.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(34).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(34).png)

Utilizar la línea de comando `systemctl start mosquitto` para iniciar Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(35).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(35).png)

Ingresar contraseña.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(36).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(36).png)

Se habrá iniciado Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(37).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(37).png)

Utilizar el la línea de comando `systemctl status mosquitto` para conocer el estado de Mosquitto.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(38).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(38).png)

Mosquitto se encuentra activo.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(39).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(39).png)

Utilizar la línea de comando `sudo ufw enable` para activar “Ubuntu Firewall”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(40).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(40).png)

Se habrá activado “Ubuntu Firewall”.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(41).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(41).png)

Utilizar la línea de comando `sudo ufw allow` para crear reglas de entrada y salida para el puerto 1883.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(42).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(42).png)

Se habrán creado las reglas de entrada y salida para el puerto 1883.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(43).png](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/ESP32CAM-MQTT-Basic%20(43).png)

El “Error rc=-2” habrá desaparecido.

# Evidencias

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/Evidencia%20A.jpg](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/Evidencia%20A.jpg)

Circuito para cargar el programa.

![https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/Evidencia%20B.jpg](https://raw.githubusercontent.com/RaulToribio/29-ESP32CAM-MQTT-Basic/main/Im%C3%A1genes/Evidencia%20B.jpg)

Circuito para correr el programa.

# Créditos

> [José Raúl Toribio Gabriel](https://github.com/RaulToribio)
> 

> [Codigo IoT](https://github.com/codigo-iot)
>