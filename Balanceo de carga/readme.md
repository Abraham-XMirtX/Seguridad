# Balanceo de cargas

En esta actividad vamos configurar una máquina con PfSense para que actúe como un balanceador de cargas de dos redes con acceso a internet.

## Configuración Máquina Virtual para PfSense.

Tenemos que tener 3 interfaces de red para simular un balanceo de carga con el PfSense.

  *  La primera tarjeta de red en Adaptador Puente.

  ![img](img/001.png)

  *  La segunda tarjeta de red Interna.

  ![img](img/002.png)

  *  La tercera tarjeta de red Adaptador Puente

  ![img](img/003.png)

Ya tenemos en la máquina virtual con 3 tarjetas de red.

## Configurar Las tarjeta de red.

En la práctica anterior teniamos configurado dos tarjeta de red, por lo tanto solo vamos a configurar la tercera tarjeta de red.

![img](img/005.png)

Vamos a configurar para que em0 y em2 sean para el adaptador puente.

![img](img/006.png)

em1 como comprobamos es para la LAN Interna.

![img](img/007.png)

![img](img/008.png)

Ya tenemos las 3 interfaces configuradas.

![img](img/009.png)

Configuramos en el Equipo cliente la interfaz de red con la siguiente dirección IP.

![img](img/011.png)

Nos conectamos al pfsense desde un navegador.

![img](img/012.png)

Entramos al pfsense.

![img](img/013.png)

Vamos a System y Routing.

![img](img/014.png)

Comprobamos nuestras interfaces.

![img](img/015.png)

![img](img/016.png)

Ahora vamos a crear un grupo y dentro vamos a meter las dos interfaces para el balanceo de carga.

![img](img/017.png)

Lo llamamos balanceo.

![img](img/018.png)

Vamos a Firewall y reglas.

![img](img/019.png)

Vamos a la interfaz de LAN y le damos editar y vamos a Gateway y seleccionamos el grupo creado.

![img](img/020.png)

![img](img/021.png)

Comprobamos en Gateway que ahora nuestra puerta de enlace es el grupo de balanceo de carga, es decir las dos interfaces.

![img](img/022.png)

Realizamos una comprobación para saber como va su trama.

![img](img/023.png)
