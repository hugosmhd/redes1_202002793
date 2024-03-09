Hugo Sebastian Martínez Hernández - 202002793  
Eddy Alejandro Murga Barillas - 201503741
---


# Proyecto 1 - Redes 1

## Resumen de direcciones IP y VLAN

| Departamento  | VLAN | ID de red       |
|:------------- |:----:| ---------------:|
| Contabilidad  | 14   | 192.168.14.0/24 |
| Secretaria    | 24   | 192.168.24.0/24 |
| RRHH          | 34   | 192.168.34.0/24 |
| IT            | 44   | 192.168.44.0/24 |
sss

<table>
    <thead>
        <tr>
            <th>Departamento</th>
            <th>VLAN</th>
            <th>Nombres dispositivos finales</th>
            <th>IP Host</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3 align="center">Contabilidad</td>
            <td rowspan=3 align="center">14</td>
            <td align="center">CONTABILIDAD_1</td>           
            <td align="center">192.168.14.1</td>
        </tr>
        <tr>
            <td align="center">CONTABILIDAD2</td>
            <td align="center">192.168.14.2</td>
        </tr>
        <tr>
            <td align="center">S_CONTABILIDAD</td>
            <td align="center">192.168.14.3</td>
        </tr>
        <tr>
            <td rowspan=3 align="center">Secretaria</td>
            <td rowspan=3 align="center">24</td>
            <td align="center">SECRETARIA1</td>           
            <td align="center">192.168.24.1</td>
        </tr>
        <tr>
            <td align="center">SECRETARIA2</td>           
            <td align="center">192.168.24.2</td>
        </tr>
        <tr>
            <td align="center">SECRETARIA3</td>           
            <td align="center">192.168.24.3</td>
        </tr>
        <tr>
            <td rowspan=4 align="center">RRHH</td>
            <td rowspan=4 align="center">34</td>
            <td align="center">RRHH1</td>           
            <td align="center">192.168.34.1</td>
        </tr>
        <tr>
            <td align="center">RRHH2</td>           
            <td align="center">192.168.34.2</td>
        </tr>
        <tr>
            <td align="center">RRHH</td>           
            <td align="center">192.168.34.3</td>
        </tr>
        <tr>
            <td align="center">S_RRHH</td>           
            <td align="center">192.168.34.4</td>
        </tr>
        <tr>
            <td rowspan=3 align="center">IT</td>
            <td rowspan=3 align="center">44</td>
            <td align="center">IT_1</td>           
            <td align="center">192.168.44.1</td>
        </tr>
        <tr>
            <td align="center">IT_2</td>           
            <td align="center">192.168.44.2</td>
        </tr>
        <tr>
            <td align="center">S_IT</td>           
            <td align="center">192.168.44.3</td>
        </tr>
    </tbody>
</table>

## Capturas de la implementación de las topologías.
Topologia completa:  
![Topología completa](https://media.discordapp.net/attachments/764502305009303622/1215816339080609972/image.png?ex=65fe2034&is=65ebab34&hm=5231ebc2942e137c62ea6b17b62dbfad753d8c48d87630894c0380c884b21bf4&=&format=webp&quality=lossless&width=543&height=389)

Backbone:  
![Backbone](https://media.discordapp.net/attachments/764502305009303622/1215816674029338745/image.png?ex=65fe2083&is=65ebab83&hm=5dd9b27608e2620522f9af6ec278a877ced27a989381f07ef3df8683f1f8a758&=&format=webp&quality=lossless&width=628&height=389)

Centro Administrativo:  
![Centro Administrativo](https://media.discordapp.net/attachments/764502305009303622/1215816922784989356/image.png?ex=65fe20bf&is=65ebabbf&hm=33df8332593d9eab83c4f6cf9436abcdc78d77edd036d4178c93035ed2b970fe&=&format=webp&quality=lossless&width=448&height=389)

Área de Trabajo:  
![Area de trabajo](https://media.discordapp.net/attachments/764502305009303622/1215817118960980118/image.png?ex=65fe20ed&is=65ebabed&hm=8c89958dc8bbf871f5af83d082575b3a74bc4d8907f46b7579ce0f0d204221ff&=&format=webp&quality=lossless&width=809&height=389)

## Detalle de los comandos usados

**Comandos usados para el SW0**, que se configuro como servidor:

```plaintext
enable
configure terminal
vtp mode server
vtp domain P4
vtp password usac
vtp version 2
vlan 14
name contabilidad
exit
vlan 24
name secretaria
exit
vlan 34
name rrhh
exit
vlan 44
name it
exit

interface range f0/1-5
switchport trunk encapsulation dot1q
switchport mode trunk
switchport trunk allowed vlan all
exit

spanning-tree vlan 1 root primary
spanning-tree vlan 14 root primary
spanning-tree vlan 24 root primary
spanning-tree vlan 34 root primary
spanning-tree vlan 44 root primary
spanning-tree mode pvst
exit

wr
```

**Comandos usados para los switches clientes de Capa 3**:

```plaintext
enable
configure terminal
vtp mode client
vtp domain P4
vtp password usac

interface range f0/1-4
switchport trunk encapsulation dot1q
switchport mode trunk
switchport trunk allowed vlan all
exit

spanning-tree mode pvst 
exit
wr
```

**Comandos usados para los switches clientes de Capa 2**:

```plaintext
enable
configure terminal
vtp mode client
vtp domain P4
vtp password usac
exit
wr
```

**Comandos usados para SW9 modo transparente Capa 3**:

```plaintext
enable
configure terminal
vtp mode server
vtp domain P4
vtp password usac
vtp version 2
vlan 14
name contabilidad
exit
vlan 24
name secretaria
exit
vlan 34
name rrhh
exit
vlan 44
name it
exit

interface range f0/1-3
switchport trunk encapsulation dot1q
switchport mode trunk
switchport trunk allowed vlan all
exit

vtp mode transparent
exit
wr
```

**Comandos usados para S4 Capa 2, que va conectado hacia el SW9**:

```plaintext
enable
configure terminal
vlan 44
name it
exit

interface f0/11
switchport mode access
switchport access vlan 44
no shutdown
exit
exit
wr
```

## Ping entre hosts

1. Ping desde el Centro Administrativo desde el host IT_2 con IP: 192.168.44.2 hacia el Área de trabajo hacia el host IT_1 con IP: 192.168.44.1

**RESPUESTA EXITOSA, ya que están en la misma VLAN**

![Ping 1](https://media.discordapp.net/attachments/764502305009303622/1215821213255860294/image.png?ex=65fe24be&is=65ebafbe&hm=8634d7dd918955ff918217f94998fbb5c99d6d34edf0ca2003b8c51bc6f9f030&=&format=webp&quality=lossless&width=550&height=324)

2. Ping desde el Backbone desde el host S_RRHH con IP: 192.168.34.4 hacia el Área de trabajo hacia el host SECRETARIA1 con IP: 192.168.24.1

**RESPUESTA FALLIDA, ya que están en VLANs diferentes**

![Ping 2](https://media.discordapp.net/attachments/764502305009303622/1215822534096977930/image.png?ex=65fe25f9&is=65ebb0f9&hm=b489a2a7fa05973c6f4d79ed17f103cd28173e953c6b6cc8808248a99271b9bf&=&format=webp&quality=lossless&width=653&height=389)
