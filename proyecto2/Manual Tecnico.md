## Asignación de Subredes usando VLSM para la sede Jutiapa

1. **VLAN Ventas de 25 hosts:**
   - Requiere al menos 25 hosts.
   - Necesitamos una máscara de subred que permita al menos 25 hosts. La máscara de /27 permite hasta 30 hosts (32 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.168.31.0/27
   - Rango de direcciones utilizables: 192.168.31.1 - 192.168.31.30
   - Dirección de broadcast: 192.168.31.31

2. **VLAN Informática de 12 hosts:**
   - Requiere al menos 12 hosts.
   - Necesitamos una máscara de subred que permita al menos 12 hosts. La máscara de /28 permite hasta 14 hosts (16 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.168.31.32/28
   - Rango de direcciones utilizables: 192.168.31.33 - 192.168.31.46
   - Dirección de broadcast: 192.168.31.47

3. **VLAN RRHH de 10 hosts:**
   - Requiere al menos 10 hosts.
   - Necesitamos una máscara de subred que permita al menos 10 hosts. La máscara de /28 permite hasta 14 hosts (16 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.168.31.48/28
   - Rango de direcciones utilizables: 192.168.31.49 - 192.168.31.62
   - Dirección de broadcast: 192.168.31.63

4. **VLAN Contabilidad de 4 hosts:**
   - Requiere al menos 4 hosts.
   - Necesitamos una máscara de subred que permita al menos 4 hosts. La máscara de /29 permite hasta 6 hosts (8 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.168.31.64/29
   - Rango de direcciones utilizables: 192.168.31.65 - 192.168.31.70
   - Dirección de broadcast: 192.168.31.71

![Tabla_Q](Imagenes/Tabla_Jutiapa.jpeg)

## Asignación de Subredes usando VLSM para la sede Escuintla

1. **VLAN Ventas de 20 hosts:**
   - Requiere al menos 20 hosts.
   - Necesitamos una máscara de subred que permita al menos 20 hosts. La máscara de /27 permite hasta 30 hosts (32 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.148.31.0/27
   - Rango de direcciones utilizables: 192.148.31.1 - 192.148.31.30
   - Dirección de broadcast: 192.148.31.31

2. **VLAN RRHH de 5 hosts:**
   - Requiere al menos 5 hosts.
   - Necesitamos una máscara de subred que permita al menos 5 hosts. La máscara de /29 permite hasta 6 hosts (8 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.148.31.32/29
   - Rango de direcciones utilizables: 192.148.31.33 - 192.148.31.38
   - Dirección de broadcast: 192.148.31.39

![Tabla_Q](Imagenes/Tabla_Escuintla.jpeg)

<!-- SEDE QUICHE Y PETEN -->


## Asignación de Subredes usando VLSM para la sede Quiche

1. **VLAN Ventas de 36 hosts:**
   - Requiere al menos 36 hosts.
   - Necesitamos una máscara de subred que permita al menos 36 hosts. La máscara de /26 permite hasta 62 hosts (64 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.178.31.0/26
   - Rango de direcciones utilizables: 192.178.31.1 - 192.178.31.62
   - Dirección de broadcast: 192.178.31.63

2. **VLAN Informatica de 21 hosts:**
   - Requiere al menos 21 hosts.
   - Necesitamos una máscara de subred que permita al menos 21 hosts. La máscara de /27 permite hasta 30 hosts (32 direcciones - 2 direcciones para red y broadcast).
   - Dirección de red: 192.178.31.64/27
   - Rango de direcciones utilizables: 192.178.31.65 - 192.178.31.94
   - Dirección de broadcast: 192.178.31.95

3. **VLAN RRHH de 12 hosts:**
   - Requiere al menos 12 hosts.
   - Necesitamos una máscara de subred que permita al menos 12 hosts. La máscara de /28 permite hasta 14 hosts (16 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.178.31.96/28
   - Rango de direcciones utilizables: 192.178.31.97 - 192.178.31.110
   - Dirección de broadcast: 192.178.31.111

4. **VLAN Contabilidad de 10 hosts:**
   - Requiere al menos 10 hosts.
   - Necesitamos una máscara de subred que permita al menos 10 hosts. La máscara de /28 permite hasta 14 hosts (16 direcciones - 2 direcciones para red y broadcast). 
   - Dirección de red: 192.178.31.112/28
   - Rango de direcciones utilizables: 192.178.31.113 - 192.178.31.126
   - Dirección de broadcast: 192.178.31.127

![Tabla_Q](Imagenes/Tabla_Quiche.png)

## Asignación de Subredes usando VLSM para sede Peten

1. **VLAN Ventas de 30 hosts:**
   - Requiere al menos 30 hosts.
   - Necesitamos una máscara de subred que permita al menos 30 hosts. La máscara de /27 permite hasta 30 hosts (32 direcciones - 2 direcciones para red y broadcast).
   - Dirección de red: 192.158.31.0/27
   - Rango de direcciones utilizables: 192.158.31.1 - 192.158.31.30
   - Dirección de broadcast: 192.158.31.31

2. **VLAN Informatica de 15 hosts:**
   - Requiere al menos 15 hosts.
   - Necesitamos una máscara de subred que permita al menos 15 hosts. La máscara de /27 permite hasta 30 hosts (32 direcciones - 2 direcciones para red y broadcast).
   - Dirección de red: 192.158.31.32/27
   - Rango de direcciones utilizables: 192.158.31.33 - 192.158.31.62
   - Dirección de broadcast: 192.158.31.63

3. **VLAN RRHH de 10 hosts:**
   - Requiere al menos 10 hosts.
   - Necesitamos una máscara de subred que permita al menos 10 hosts. La máscara de /28 permite hasta 14 hosts (16 direcciones - 2 direcciones para red y broadcast).
   - Dirección de red: 192.158.31.64/28
   - Rango de direcciones utilizables: 192.158.31.65 - 192.158.31.78
   - Dirección de broadcast: 192.158.31.79

![Tabla_P](Imagenes/Tabla_Peten.png)

## 


## Comandos usados en Jutiapa

**SW de Capa 3**

```
-- creacion de vlans
enable
configure terminal
vtp mode server
vtp domain jutiapa
vtp password 123
vtp version 2
interface range f0/1-2
switchport trunk allowed vlan all
vlan 14
name rrhh
exit
vlan 24
name contabilidad
exit
vlan 34
name ventas
exit
vlan 44
name informatica
exit
exit
wr

-- Para subinterfaces
interface vlan 14
ip address 192.168.31.49 255.255.255.240
exit
interface vlan 24
ip address 192.168.31.65 255.255.255.248
exit
interface vlan 34
ip address 192.168.31.1 255.255.255.224
exit
interface vlan 44
ip address 192.168.31.33 255.255.255.240
exit
ip routing

-- rpvst
spanning-tree vlan 1 root primary
spanning-tree vlan 14 root primary
spanning-tree vlan 24 root primary
spanning-tree vlan 34 root primary
spanning-tree vlan 44 root primary
spanning-tree mode rapid-pvs
```

**SW Clientes**

```
-- Aceso a las vlans
enable
configure terminal
vtp mode client
interface range f0/2-3
switchport mode trunk
switchport trunk allowed vlan all
exit
vtp domain jutiapa
vtp password 123
exit
wr

-- rpvst
spanning-tree mode pvst 
```

**LACP **
```
enable
conf t
interface range fa0/1-2
shutdown
channel-group 1 mode active
no shutdown
exit
interface port-channel 1
switchport mode trunk
switchport trunk allowed vlan all
end
wr
```

**SW0 Cliente**
```
-- Accesso a las vlan LISTO
enable
configure terminal
interface f0/10
switchport mode access
switchport access vlan 14
no shutdown
exit
interface f0/11
switchport mode access
switchport access vlan 24
no shutdown
exit
interface f0/12
switchport mode access
switchport access vlan 34
no shutdown
exit
exit
```

**SW1 Cliente**
```
enable
configure terminal
interface f0/10
switchport mode access
switchport access vlan 44
no shutdown
exit
interface f0/11
switchport mode access
switchport access vlan 14
no shutdown
exit
interface f0/12
switchport mode access
switchport access vlan 24
no shutdown
exit
exit
wr
```

**Router J1**

```
enable
configure terminal
int fa0/0
ip address 192.167.31.2 255.255.255.248
no shutdown
```

**Router J2**

```
enable
configure terminal
int fa0/0
ip address 192.167.31.3 255.255.255.248
no shutdown
```

**HSRP**

```
ROUTER J1
enable
conf t
interface fa0/0
standby 1 ip 192.167.31.1
standby 1 priority 150
standby 1 preempt
exit

J2
enable
conf t
standby 1 ip 192.167.31.1
exit
show standby
```

**Configuracion de IP's para J1, J2 y Router Jutiapa**

```
J1 - R JUTIAPA
Dirección de red: 11.0.0.0/30 (Primera subred)
Rango de direcciones utilizables: 11.0.0.1 - 11.0.0.2
Broadcast: 11.0.0.3

-- IP
enable
configure terminal
int fa1/0
ip address 11.0.0.1 255.255.255.252
no shutdown
exit
exit
wr

J2 - R JUTIAPA
Dirección de red: 12.0.0.0/30 (Primera subred)
Rango de direcciones utilizables: 12.0.0.1 - 12.0.0.2
Broadcast: 12.0.0.3

-- IP
enable
configure terminal
int fa1/0
ip address 12.0.0.1 255.255.255.252
no shutdown
exit
exit
wr

ROUTER Jutiapa
enable
configure terminal
int fa4/0
ip address 11.0.0.2 255.255.255.252
no shutdown
exit
exit
wr

enable
configure terminal
int fa5/0
ip address 12.0.0.2 255.255.255.252
no shutdown
exit
exit
wr
```

**RIP**

```
-- RIP
enable
configure termina
interface fa0/0 -- int que va al switch
ip address 192.168.1.1 255.255.255.0
no shutdown

route rip
version 2
network 192.168.1.0 #red_general se agregan todas
version 2
exit
```

## Comandos usados en Escuintla

**SW2**

```
-- creacion de vlans
enable
configure terminal
vtp mode server
vtp domain escuintla
vtp password 123
vtp version 2
vlan 14
name rrhh
exit
vlan 24
name ventas
exit
exit
wr
-- Accesso a las vlan
enable
configure terminal
interface f0/10
switchport mode access
switchport access vlan 14
no shutdown
exit
interface f0/11
switchport mode access
switchport access vlan 24
no shutdown
exit
exit
wr

-- rpvst
enable
configure terminal
spanning-tree mode pvst
interface fa0/1
switchport mode trunk
```

**Router ESCUINTLA**

```
enable
configure terminal
interface fa4/0
no shutdown
interface fa4/0.14
encapsulation dot1Q 14
ip address 192.148.31.1 255.255.255.248
no shutdown
exit
interface fa4/0.24
encapsulation dot1Q 24
ip address 192.148.31.9 255.255.255.224
no shutdown
exit
exit
wr

enable
configure terminal
interface fa4/0
no shutdown
interface fa4/0.14
encapsulation dot1Q 14
ip address 192.148.31.33 255.255.255.248
no shutdown
exit
interface fa4/0.24
encapsulation dot1Q 24
ip address 192.148.31.1 255.255.255.224
no shutdown
```