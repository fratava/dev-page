---
# Title, summary, and page position.
linktitle: Materiales
weight: 1
icon: screwdriver
icon_pack: fas

# Page metadata.
title: ''
type: book  # Do not modify.
---

En la primer parte del proyecto, vamos a revisar los accesorios que son necesarios para poder crear nuestro clúster. En la siguiente sección, vamos a mostrar los materiales que son necearios para nuestro cluster de Raspeberry Pi 4.

### Materiales necesarios

- Raspberry Pi 4 (2, 4 ó 8 GB de RAM)
- Memoria micro SD [^1] [^2]
- Adaptador de corriente
- Cable de red Cat 5e
- Switch ethernet (preferentemente Gigabit)

{{< figure src="https://cdn.ftapia.dev/images/cluster_material.jpg" width="600" align="center" >}}

### Materiales opcionales
- Carcasa 
- Disipadores
- Ventiladores
- Cable micro HDMI a HDMI

Estos accesorios se recomiendan para terner un mejor rendiemiento y poder elevar la frecuencia de reloj del procesador. Además, protejen a la placa del polvo y otros elementos. El cable micro HDMI es sólo si no cuentas con una computadora principal.

{{< figure src="https://cdn.ftapia.dev/images/piezas_rpi.jpg" width="600" align="center" >}}

### Armado del clúster

El armado del cluster es sencillo. En caso de que se haya comprado disipadores, se tiene que pegar sobre la cpu, gpu y la RAM. Si cuentas con ventilador y carcasa, tendrás que atornillarlos. 

{{< figure src="https://cdn.ftapia.dev/images/rpi_armado.jpeg" width="600" align="center" >}}


Ese paso hay que hacerlo para cada uno de los Raspberry Pi 4 que vayamos a utilizar para el clúster.

Después, conectaremos los cables ethernet a cada uno de los Raspberry. Es recomendable sólo conectar un Rapsberry a la vez al switch para configurarlos individualmente. También debemos conectar los adaptadores de corriente. Al final, debemos tener algo como la siguiente imagen.

{{< figure src="https://cdn.ftapia.dev/images/cluster_armado.jpg" width="600" align="center" >}}


{{% callout info %}}
Hemos terminado de ensamblar nuestro clúster. Ahora, vamos a configurar a nuestro maestro y los nodos de computación. 
{{% /callout %}}

[^1]: Altamente recomendamos utilizar microSD UHS-I Clase 10 (escritura 100 MB/s) de marcas reconocidas para tener un mejor performance.
[^2]: Existe la posibilidad de utilizar USB-A 3.0 para cargar el sistema operativo. Si tu presupuesto lo permite, es la mejor opción ya que el estandar USB 3.0 tiene un mejor ancho de banda.