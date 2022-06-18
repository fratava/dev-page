---
# Title, summary, and page position.
linktitle: Configuración
weight: 3
icon: mouse
icon_pack: fas

# Page metadata.
title: ''
type: book  # Do not modify.
---

# Configurando el clúster

Una vez que hemos terminado con la parte del hardware, vamos a configurar la parte de software del clúster.

## Topología del clúster

### Tree
{{< figure src="https://cdn.ftapia.dev/images/tree-topo.svg" width="600" align="center" >}}

### Dragonfly
{{< figure src="https://cdn.ftapia.dev/images/dragonfly.svg" width="600" align="center" >}}


## Instalando el sistema operativo

Una vez diseñada nuestra topología, vamos a instalar el sistema operativo en nuestros Raspberrys. Para este proyecto hemos seleccionado a Ubuntu 20.04 64-bit LTS debido a que en nuestro clúster utilizamos la versión de 8 GB ram en los Raspberry y podemos obtener un mejor rendimiento con esta versión del sistema operativo. En caso de que cuentes con una versión de 1 GB o 2 GB de ram, te sugerimos utilizar la versión de 32-bit de Ubuntu 20.04 LTS, ya que en la versión de 64-bits no obtendrás mayor rendimiento y utilizarás más ram, lo cual se reflejará en un menor rendimiento.

La forma más sencilla de instalar el sistema operativo en las tarjetas microSD es utilizando la heramienta Raspberry Pi Imager. En la siguiente sección detallamos paso a paso el proceso.

### Raspberry Pi Imager

Descargamos Raspberry Pi Imager para nuestro sistema operativo desde [https://www.raspberrypi.org/software/](https://www.raspberrypi.org/software/). Una vez instalado lo abrimos y veremos la pantalla principal.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_1.png" width="600" align="center" >}}

Ahí seleccionaremos el sistema operativo en el botón "CHOOSE OS". Encontraremos varias versiones de Raspbian un fork de Debian, y un pestaña de otros sistemas operativos. Damos click.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_2.png" width="600" align="center" >}}

En esta pestaña encontraremos a Ubuntu y otros sistemas, seleccionamos nuevamente la pestaña de Ubuntu para buscar la versión que utilizaremos.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_3.png" width="600" align="center" >}}

Buscamos la versión "Ubuntu Server 20.04 LTS de 64-bits".

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_4.png" width="600" align="center" >}}

YA que la hemos seleccionado, regresamos a la pantalla principal y ahora seleccionamos el botón "CHOOSE STORAGE". Se desplejará un menú en dónde tenedremos que elegir el disco en el cuál deseamos instalar el sistema operativo. En nuestro caso escogeremos la microSD de 32 GB.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_5.png" width="600" align="center" >}}

Recomendamos ampliamente hacer una configuración del sistema en esta etapa. En la siguiente imagen se muestran la configuraciones que tendremos en este clúster. Cambiaremos el nombre del hostname para tener un máster, un nodo1, nodo2 y nodo3. Esto va a cambiar según tu topología y el número de nodos que tengas. Habilitamos el servidor SSH. Aquí existen dos opciones:

* Habilitar un username y un password. Esto es recomendable si van a existir varios administradores.
* Utulizar tu llave pública. Esto es altamente *recomendable* si sólo existe un administrador. El utilizar la llave pública es una buena práctica de seguridad en el clúster, ya que sólo el que poseé la llave pública puede acceder al clúster.

Opcionalmente se puede configurar la zona horaria y el idioma del teclado.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_6.png" width="600" align="center" >}}

Una vez que tenemos nuestra configuración, damos click en el botón "WRITE" y esperamos a que finalice el proceso.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_7.png" width="600" align="center" >}}

Nos pedirá autorización para poder copiar los archivos en el disco que seleccionamos.

{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_8.png" width="600" align="center" >}}

Una vez finalizado el proceso, retiramos la microSD o USB de nuestra computadora.

{{% callout warning %}}
Hemos detectado que en algunos modelos de microSD falla la instalación del sistema operativo. Nuestra recomendación es utilizar tarjetas microSD de buena calidad como SanDisk, Samsung o Kingston.
{{< figure src="https://cdn.ftapia.dev/images/rpi_imager_9.png" width="600" align="center" >}}
{{% /callout %}}

## SSH

## Ansible


## Configurando el nodo maestro

Una vez que completamos el paso anterior, colacamos la memoria SD en el el slot de la placa, conectamos el eliminador de corriente y el cable ethernet tanto en la placa como en el switch.
Esperamos un par de minutos mientras se inicia el sistema operativo y abrimos la terminal de nuestro sistema operativo y tecleamos:

```bash
ssh pi@192.168.0.xx
```

la contraseña es raspberry. Una vez que nos permite logearnos, veremos algo como esto

```shell
 The programs included with the Debian GNU/Linux system are free software;
 the exact distribution terms for each program are described in the
 individual files in /usr/share/doc/*/copyright.

 Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
 permitted by applicable law.
 Last login: Tue Dec 22 23:34:38 2020 from 192.168.0.xx

 Wi-Fi is currently blocked by rfkill.
 Use raspi-config to set the country before use.

 pi@raspberrypi:~ $ 
```

{{% callout info %}}
Para obtener la ip de tu Raspberry, la conectamos al switch y después al router. Entramos a la página de gestión de nuestro router, generalmente la dirección del router es 192.168.0.1 la contraseña en la mayoría de los casos, se encuentra en el router. Una vez que nos logeamos, buscamos los dispotivos activos en nuestra red. Nuestro nodo maestro aparecerá como raspberry.
{{% /callout %}}

y vamos a seguir el siguiente tutotrial. 

### Cambiando el hostname y contraseña

El nombre del hostname será "master", pero podemos usar este tutorial para todos los nodos.

{{< youtube 0mPOSlQ3gxo >}}

### Instalando los paquetes necesarios

Cuando reiniciamos la Raspberry Pi 4, vamos a actualizar los paquetes e instalar otro. Primero vamos actualizarlos

```bash
sudo apt update
```

Después vamos a instalar los paquetes necesarios para la mayoría de pruebas que vamos a realizar. 

```bash
sudo apt-get install build-essential
sudo apt-get install manpages-dev
sudo apt-get install gfortran
sudo apt-get install nfs-common
sudo apt-get install nfs-kernel-server
sudo apt-get install emacs
sudo apt-get install openmpi-bin
sudo apt-get install libopenmpi-dev
sudo apt-get install openmpi-doc
sudo apt-get install keychain
sudo apt-get install nmap
sudo apt-get install htop
sudo apt-get install git
```

### CPU (overclock)

La CPU del Raspeberry Pi 4 está basada en un arquitectura ARM. Cuenta con un procesador quad-core Cortex-A72 de 64 bits. Por defecto, tiene una frecuencia de reloj de 1.5GHz para proteger al procesador de las altas temperaturas. En nuestro caso, buscamos obtener la mejor relación entre la frecuencia del reloj, voltaje y temperatura. Es necesario aclarar que no en todos los procesadores se puede elevar la frecuencia de reloj más allá de los 2.0 GHz. Esto se debe principalmente a que cuando se fabrican los procesadores, el silicio puede tener algunas imperfecciones, las cuales afectan directamente la velocidad del reloj. Tras un serie de pruebas, hemos observado que todos los Raspberry Pi 4 pueden alcanzar 2.0 GHz sin aumento drástico de temperatura (utilizando disipadores), y sólo algunos pudieron alcanzar los 2.14 GHz sin fallas por parte del sistema operativo. Por lo tanto, podemos hacer un overclock al procesador y llevarlo de manera segura hasta los 2.0 GHz.

Para poder realizar overclock, encendemos nuestro dispositivo y editamos el archivo config.txt. Es necesario contar con privilegios de super usuario para esto. Entonces tecleamos 

```bash
sudo nano /boot/config.txt
```

Ahora, dentro del editor de texto tendremos que buscar la sección marcada como [pi4], bajo la cual están los ajustes específicos para este modelo de Raspberry Pi. Esto es muy bueno porque significa que si utilizáis la misma tarjeta SD con el sistema operativo en otra Raspberry Pi de generación anterior, no se aplicarán los parámetros de overclock.

Hay que ir al final del bloque de ajustes bajo [pi4] y añadir las siguientes líneas:

```bash
over_voltage=6
arm_freq=2000
```

El primer ajuste, "over_voltage=6", incrementa el voltaje de funcionamiento en aproximadamente 0.15V. Esto es necesario ya que la mayoría de Raspberry Pi 4 no arrancarán a 2.0 GHz sin este extra. Más tarde, si se quiere, se puede cambiar el valor 4 por un 2, lo que supondría un incremento de voltaje de 0.05V para reducir el calor generado, pero no hay garantías de que funcione correctamente.

{{% callout warning %}}
Es altamente recomendable no poner más de 6 al valor de over_voltage, ya que podría ser peligroso para la integridad del procesador.
{{% /callout %}}

{{% callout warning %}}
Si la pantalla se queda en blanco o el dispositivo comienza un ciclo infinito de reinicios, tendríamos que meter la tarjeta SD en otro equipo y volver a editar el fichero fichero config.txt y esta vez edita el parámetro arm_freq, reduciendo su valor de 50 en 50 MHz. Si tienes que hacer esto, significa que tu procesador no es candidato a hacer overclock. En este caso sería mejor establecer una frecuencia de reloj de referencia para todos los nodos, por ejemplo 1800 (1.8 GHz).
{{% /callout %}}

El segundo ajuste, "arm_freq=2000", establece la frecuencia de funcionamiento de los cuatro cores ARM a 2.0 GHz. Te recomendamos no elevar más este valor, ya que este es el máximo establecido por el firmware (que, por cierto, hasta hace poco era 1.75 GHz).

Una vez que añadimos estas líneas pulsamos ++ctrl+o++ y ponemos ++enter++, después tecleamos ++ctrl+x++. 

El siguiente paso, muy importante antes de reiniciar, es actualizar a la última versión del firmware, la que nos asegura que será compatible con la velocidad de 2.0 GHz. Para ello, hay que introducir el siguiente comando:

```bash
sudo rpi-update
```

Esto cargará el actualizador de Raspberry Pi, que se encargará de manera automática de actualizar el firmware a la última versión. Cuando termine, reiniciamos el sistema con el comando

```bash
sudo reboot
```

Cuando vuelva a iniciar, podemos hacer un seguimiento de la frecuancia del reloj con el comando 

```bash
watch -n 1 vcgencmd measure_clock arm
```

Y listo, hemos configurado nuestro dispositivo para obtener velocidades más altas de procesamiento.

## Configurando los demás nodos

### Configuración inicial

Para cada uno de los nodos, cambiamos el [hostname](#cambiando-el-hostname-y-contrasena) por nodox y cambiamos la frecuencia del procesador como lo vimos en la sección [overclock](#cpu-overclock).

{{% callout info %}}
Es recomendable ir conectando y configurando un raspberry a la vez para no tener conflicto con las direcciones ip.
{{% /callout %}}

{{% callout info %}}
La contraseña debe ser la misma para cada nodo que conectemos. Esto es para facilitar su manejo.
{{% /callout %}}

### Instalando los paquetes

Para instalar los paquetes necesarios, podemos iniciar sesión en cada nodo de la siguiente manera:

```bash
ssh pi@192.168.0.xx
```
e instalarlos como lo vimos [anteriormente](#instalando-los-paquetes-necesarios).

Otra manera de instalarlos es utilizar el paquete fabric en python. Para ello, lo instalamos en el nodo maestro de la siguiente manera

```bash
sudo apt install fabric
```

Una vez instalado, creamos un archivo llamado fabfile.py y escribimos:

```python
from fabric.api import *

env.hosts = [
    'pi@192.168.0.27',
    'pi@192.168.0.28',
    'pi@192.168.0.29',
]

env.password = 'tupassword'

@parallel
def cmd(command):
    sudo(command)
```

En el comando `env.hosts` ponemos la dirección de cada uno de los nodos. Para este ejemplo, estamos utilizando un maestro y tres nodos de computación. Los nodos los hemos configurado para que sigan una secuencia de direcciones ip, pero puede ser cualquier orden de ip's.

La forma en que instalamos los paquetes es la siguiente:

```bash
fab cmd:"apt-get install -y update"
fab cmd:"apt-get install -y build-essential"
fab cmd:"apt-get install -y manpages-dev"
fab cmd:"apt-get install -y gfortran"
fab cmd:"apt-get install -y nfs-common"
fab cmd:"apt-get install -y nfs-kernel-server"
fab cmd:"apt-get install -y emacs"
fab cmd:"apt-get install -y openmpi-bin"
fab cmd:"apt-get install -y libopenmpi-dev"
fab cmd:"apt-get install -y openmpi-doc"
fab cmd:"apt-get install -y keychain"
fab cmd:"apt-get install -y nmap"
fab cmd:"apt-get install -y htop"
fab cmd:"apt-get install -y git"
```

{{% callout success %}}
Hemos terminado la segunda parte de nuestro proceso. En esta parte, hemos configurado el master y los nodos con la paquetería necesaria. Ahora, nuestro objetivo será que se comuniquen entre ellos y que trabajen coordinadamente. 
{{% /callout %}}