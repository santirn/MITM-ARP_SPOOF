# MITM ARP SPOOF
Man in the middle. Envenenamiento ARP con Kali Linux. Este POC está realizado bajo una red privada donde el atacado es plenamente consciente del ataque. 


Ponemos la tarjeta de red en modo monitor para escuchar todos los paquetes que circulan por nuestra NIC y averiguar la dirección MAC del enrutador víctima.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/1.jpg)

Escuchamos solo los paquetes que circulan con el nombre del SSID del enrutador víctima para seleccionar el host víctima.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/2.jpg)

Ahora nos toca averiguar las direccion IP. Con la herramienta fping almacenaremos las IPs y MACs en nuestra tabla ARP de todos los dispositivos a los que tengamos alcance en la red.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/3.jpg)


Mediante un grep buscamos en nuestra tabla ARP la IP con la MAC.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/4.jpg)

Lanzamos el envenenamiento a ambos equipos.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/5.jpg)

Activamos nuestro linux como enrutador para redirigir los paquetes recividos por las víctimas.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/6.jpg)

Mediante un lector de paquetes de red como es WireShark indagamos hasta encontrar con el suculento premio.
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/7.jpg)

Si has tenido éxito en tu búsqueda podrás encontrar algo como esto:
![](https://github.com/santirn/MITM-ARP_SPOOF/blob/master/8.jpg)
