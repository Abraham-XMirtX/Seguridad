# VPN Windows 2012 Server

![img](img/vpn.png)

## 1. Configuración de la Máquina Virtual

Tenemos que agregar una nueva máquina virtual en `VirtualBox`.
y dos tarjeta de red.

- Una Tarjeta  **Interna**
- Una Tarjeta  **Externa**

![img](img/001.png)

## 2. Instalación del Windows Server 2012.

- Utilizamos asistente de `Windows`.
- Instalación por `defecto`

![](img/002.png)

- Seleccionamos el idioma, en nuestro caso el `Español`

![](img/003.png)

- Seleccionamos la versión con entorno gráfico `GUI`.

![](img/004.png)

- Lo dejaremos por defecto.

![](img/005.png)

- Esperamos que finalize la instalación.

Nos pedirá la contraseña para el administrador de `Windows Server 2012`

![](img/006.png)

Ya tenemos instalado el `Windows Server 2012`, este el panel de control del servidor.

![](img/007.png)

## 3. Configuración de las tarjetas de red

Solo tenemos que ir `cambiar la Configuración de la red`.

![](img/008.png)

### 3.1 Configuración tarjeta de red Externa

Vamos a la tarjeta de red `Externa` y le damos a `propiedades`.

- Desactivamos todas las casillas menos la de `TCP/IP Versión 4`

![](img/010.png)

Configuramos la dirección IP.

![](img/011.png)

Vamos a la pestaña de `WINS` y configuramos.

![](img/012.png)


### 3.2 Configuración Tarjeta de Red Interna

Dejamos una IP estatica en la tarjeta de red `Interna`

![](img/013.png)


## 4. Instalación del rol de Remote Access.

Tenemos que ir **administrador del sistema->Agregar nuevo rol**.

![](img/014.png)

- Seleccionamos `acceso remoto`

![](img/015.png)

- Le damos a siguiente.

![](img/016.png)

- Seleccionamos la característica **DirectAccess y VPN(RAS)**

![](img/017.png)

- Le damos siguiente.

![](img/018.png)

- Lo dejamos por defecto

![](img/019.png)

- Le damos instalar.

![](img/020.png)

- Seleccionamos **abrir el asisten para introducción**

![](img/021.png)

- Seleccionamos Implementar solo **VPN**

![](img/022.png)

## 5. Configuración de Enrutamiento y accesso remoto para VPN

Vamos a `configurar y habilitar enrutamiento y acceso remoto`


![](img/023.png)

- Le damos siguiente.

![](img/024.png)

- Dejamos la que viene por defecto.

![](img/025.png)

- Marcamos solo **VPN**

![](img/026.png)

- Configuramos la tarjeta de red `Externa` y habilitar seguridad en la interfaz.

![](img/027.png)

- Seleccionamos de un **intervalo de direcciones especificado.**

![](img/028.png)

- Le damos a nuevo y configuramos el intervalo de de direcciones para **IPv4**

![](img/029.png)

- Configuramos el intervalo.

![](img/030.png)

- Ya lo tenemos configurado, seguimos.

![](img/031.png)

- Seleccionamos la primera.

![](img/032.png)

- Le damos a finalizar.

![](img/033.png)

- Le damos Aceptar el relevo de mensajes.

![](img/034.png)

Ya tenemos configurado lo de VPN.


![](img/035.png)

- Seleccionamos `IPv4` y vemos la configuración en la tarjeta de red `Externa`

![](img/036.png)

- Seleccionamos y le damos propiedades.

![](img/037.png)

- Vamos a filtros entrantes y vemos los paquetes.

![](img/038.png)

## 6. Configuración Equipo Cliente para VPN

Vamos a la configuración de red del equipo cliente.

![](img/039.png)

- Vamos a la configuración para establecer la **VPN**

![](img/040.png)

- Seleccionamos el de **VPN**

![](img/041.png)

- Usar mi conexión con **VPN**

![](img/042.png)

- Escribimos la IP de nuestra **VPN**

![](img/044.png)

- Le damos a conectar.

![](img/045.png)

- Comprobamos que tenemos agregado VPN en la red.

![](img/046.png)

- Vamos a `VPN` y configuramos, en la pestaña de `Seguridad`

![](img/047.png)

- Al darle conectar nos muestra un mensaje. No podemos acceder a la VPN.

![](img/048.png)

- Vamos al servidor y creamos un usuario nuevo llamado `prueba` Vamos a propiedades y le damos a permitir acceso.

![](img/049.png)

- Le damos a conectar desde el equipo cliente a la VPN.

![](img/050.png)

- Comprobación

![](img/051.png)
