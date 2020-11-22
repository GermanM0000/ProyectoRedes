# Manual de Comandos
```shell
vtp ?
```
Es un protocolo de mensajes de nivel 2 usado para configurar y adminsitrar VLANs en equipo cisco.

```shell
vtp mode server
```
Es el modo por defecto. Desde él se pueden crear, eliminar o modificar VLANs. Su cometido es anunciar su configuración al resto de switches del mismo dominio VTP y sincronizar dicha configuración con la de otros servidores, basándose en los mensajes VTP recibidos a través de sus enlaces trunk. Debe haber al menos un servidor. Se recomienda autenticación MD5.

```shell
vtp mode client
```

En este modo no se pueden crear, eliminar o modificar VLANs, tan sólo sincronizar esta información basándose en los mensajes VTP recibidos de servidores en el propio dominio. Un cliente VTP sólo guarda la información de la VLAN para el dominio completo mientras el switch está activado. Un reinicio del switch borra la información de la VLAN.

```shell
vlan #
```
Ayudan
en la administración de la red,
separando segmentos lógicos de una red
de área local (los departamentos de una
empresa, por ejemplo) que no deberían
intercambiar datos usando la red local

```shell
switchport mode trunk
```
Se usa para interconectar diferentes tipo de equipos de red, manejo de trafico de distintas redes en un mismo puerto y cada paquete ira etiquetado y cuando se envian a una VLAN se resuelve correctamente.


```shell
#IP virtual vlan
int vlan 63 
ip add 70.0.63.251
```

Determina para una Vlan diferentes ip las cuales pueden ser asignadas y conectadas para futuras configuraciones

```shell
standby # ip [ip-virtual]
standby # priority NUM
stadby # preempt
```
Se implementa para proporcionar redundancia en la capa 3 del modelo OSI, suele implemntar en la capa de distribucion, Este utiliza una IP y una direccion MAC virtual donde un Gateway asume el control en el momento de ocurrir una falla. Al tener varios disponsitivos conectados, un dispositivo es elegido como primario o active y otro como secundario o standby el resto de dispositivos estaran escuchando en un estado listen, todo eso depende de la prioridad que se le asigne o la MAC.

```shell
EIGRP ?
```
EIGRP es utilizado en redes TCP/IP y de Interconexión de Sistemas Abierto (OSI) como un protocolo de enrutamiento del tipo vector distancia avanzado, propiedad de Cisco, que ofrece las mejores características de los algoritmos vector distancia y de estado de enlace.

```shell
OSPF ?
```

El protocolo OSPF (Open Shortest Path First) es uno de una familia de protocolos de enrutamiento IP y es un protocolo de puerta de enlace interior (IGP) para Internet, que se utiliza para distribuir información de enrutamiento IP a través de un único sistema autónomo (AS) en una red IP. El protocolo OSPF es un protocolo de enrutamiento de estado de enlace, lo que significa que los enrutadores intercambian información de topología con sus vecinos más cercanos.

```shell
#PORT-CHANNEL

channel-group # mode on
```
Es una tecnología de Cisco construida de acuerdo con los estándares 802.3 full-duplex Fast Ethernet. Permite la agrupación lógica de varios enlaces físicos Ethernet, esta agrupación es tratada como un único enlace y permite sumar la velocidad nominal de cada puerto físico Ethernet usado y así obtener un enlace troncal de alta velocidad.