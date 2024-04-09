Hugo Sebastian Martínez Hernández - 202002793  
---


# Práctica 2 Redes 1

**Descripción** 
Después de realizar un trabajo decente en la municipalidad de Chuarrancho, el camino de la vida lo guía hacia un nuevo trabajo, esta vez fue contratado por la administración del Colegio usacsito, quienes desean expandir su oferta educativa y como resultado fue creada la Academia Técnica de Formación Empresarial – TECAP. Recientemente ellos se interesaron en la infraestructura para la comunicación entre ambos sitios, por lo que se le encargó el realizar una simulación de como sería la topología del mismo, incluyendo acceso a las redes privadas y redundancia de enlaces.

![Topologia completa](https://media.discordapp.net/attachments/764502305009303622/1227080977273065482/image.png?ex=66271b37&is=6614a637&hm=9416587c458d4c7ef8d461ad0c533d74478216099e2ef2da0aedbba8cc9ab1e4&=&format=webp&quality=lossless&width=737&height=389)

## Configuración del Router R1

> Configuración de las IP's
```
enable
configure terminal
hostname R1
interface fa0/0
ip address 132.168.1.2 255.255.255.248
no shutdown
exit
interface fa0/1
ip address 132.168.2.2 255.255.255.248
no shutdown
exit
interface se0/0
ip address 10.0.0.1 255.255.255.252
no shutdown
exit
```	
> Configuración de las rutas estáticas
```	
enable
configure terminal
ip route 132.168.0.0 255.255.255.0 132.168.2.1
ip route 132.168.0.0 255.255.255.0 132.168.1.1
ip route 10.0.0.0 255.255.255.252 10.0.0.2
ip route 132.178.1.0 255.255.255.248 10.0.0.2
ip route 132.178.2.0 255.255.255.248 10.0.0.2
ip route 132.178.0.0 255.255.255.0 10.0.0.2
```	

## Configuración del Router R2

> Configuración de las IP's
```
enable
configure terminal
hostname R2
interface fa0/0
ip address 132.168.1.1 255.255.255.248
no shutdown
exit
interface fa0/1
ip address 132.168.0.2 255.255.255.0
no shutdown
exit
```	
> Configuración de las rutas estáticas
```	
enable
configure terminal
ip route 132.168.1.0 255.255.255.248 132.168.1.2
ip route 10.0.0.0 255.255.255.252 132.168.1.2
ip route 132.178.1.0 255.255.255.248 132.168.1.2
ip route 132.178.2.0 255.255.255.248 132.168.1.2
ip route 132.178.0.0 255.255.255.0 132.168.1.2
```	

## Configuración del Router R5

> Configuración de las IP's
```
enable
configure terminal
hostname R5
interface fa0/0
ip address 132.178.1.2 255.255.255.248
no shutdown
exit
interface fa0/1
ip address 132.178.0.2 255.255.255.0
no shutdown
exit
```	
> Configuración de las rutas estáticas
```	
enable
configure terminal
ip route 132.178.1.0 255.255.255.248 132.178.1.1
ip route 10.0.0.0 255.255.255.252 132.178.1.1
ip route 132.168.1.0 255.255.255.248 132.178.1.1
ip route 132.168.2.0 255.255.255.248 132.178.1.1
ip route 132.168.0.0 255.255.255.0 132.178.1.1
```	

## Configuración del Switch SW2

> Configuración del PortChannel LACP
```	
enable
configure terminal
interface range fa0/5-6
channel-group 1 mode active
exit
interface port-channel 1
switchport mode trunk
end
wr
```

## Configuración del VPC0

![Configuracion VPC0](https://media.discordapp.net/attachments/764502305009303622/1227080057239900270/image.png?ex=66271a5b&is=6614a55b&hm=971cbf28127869831560d6965ac9ec0a40bd2c26e1c39f3642ebd23a06bfe587&=&format=webp&quality=lossless&width=692&height=389)

## Creación de PortChannel con PAGP

**SW0**
```
enable
configure terminal
interface range fa0/5-6
channel-group 1 mode desirable
exit
interface port-channel 1
switchport mode trunk
end
wr
```

**SW1**
```
enable
configure terminal
interface range fa0/5-6
channel-group 1 mode auto
exit
interface port-channel 1
switchport mode trunk
end
wr
```

## Creación de PortChannel con LACP

**SW2-SW3**
```
enable
configure termina
interface range fa0/5-6
channel-group 1 mode active
exit
interface port-channel 1
switchport mode trunk
end
wr
```

## Creación de IP virtual con HSRP

**Router 2 (Principal)**
```
enable
configure terminal
interface fa0/1
standby version 2
standby 1 ip 132.168.0.1
standby 1 priority 150
standby 1 preempt 
```

**Router 3**
```
enable
configure terminal
interface fa0/1
standby version 2
standby 1 ip 132.168.0.1
```

## Comandos empleados para la verificación

**Verificación del HSRP**

```show standby```

**Ping extendido**

```ping -t 192.168.1.2```

**Verificación del LACP y PAGP**
```show etherChannel ```