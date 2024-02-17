# Practica 1 Laboratorio de Redes 1

**Estudiante**: Hugo Sebastian Martínez Hernández
**Carné**: 202002793
**Auxiliar**: Carlos Quixtán
**Sección**: A

Topología final:

![Topología Final](https://media.discordapp.net/attachments/764502305009303622/1208246739086213132/image.png?ex=65e29676&is=65d02176&hm=a861ce90ba6ed1bad232d678f1432dd28ea11900e16019d5e4002c6c260accc5&=&format=webp&quality=lossless&width=738&height=388)

## Configuración de las VPCs (una por cada área) en total 7

1. Configuración de VPC del área de Administración (Primer Nivel):
![PC111 Admon](https://media.discordapp.net/attachments/764502305009303622/1208199090253340743/image.png?ex=65e26a16&is=65cff516&hm=09a854356b8c44959155ea41431d0e98533fe60a57d2975e2accd3233a8f9f31&=&format=webp&quality=lossless&width=737&height=389)
2. Configuración de VPC del área de Gerencia (Primer Nivel):
![PC112 Gerencia](https://media.discordapp.net/attachments/764502305009303622/1208200451799916604/image.png?ex=65e26b5a&is=65cff65a&hm=b2a2eac59d00207d23a5e3b9cc4e0bf5bd41a9b8391017498b4f2a5ea01aa4e8&=&format=webp&quality=lossless&width=744&height=389)
3. Configuración de VPC del área de Recursos Humanos (Primer Nivel):
![PC114 R.H.](https://media.discordapp.net/attachments/764502305009303622/1208200717068804137/image.png?ex=65e26b9a&is=65cff69a&hm=501370f477a0b7869bf8e3dd110867bcf4b92b94e02756505c3cc1cb95c0bf48&=&format=webp&quality=lossless&width=743&height=389)
4. Configuración de VPC del área de Atención al Cliente (Primer Nivel):
![PC118 Atención al Cliente](https://media.discordapp.net/attachments/764502305009303622/1208200914834559037/image.png?ex=65e26bc9&is=65cff6c9&hm=c0bb5d2dea2d6549f68e5d3beb6744ba5f5c5371551d252068f512740cfbe32e&=&format=webp&quality=lossless&width=737&height=389)
5. Configuración de VPC del área de Oficina A (Segundo Nivel):
![PC211 Oficina A](https://media.discordapp.net/attachments/764502305009303622/1208201316581642331/image.png?ex=65e26c29&is=65cff729&hm=aaace8115259cdaef5add8e43cf038030054df71d7b86c446f8be4edcde1aa21&=&format=webp&quality=lossless&width=738&height=388)
6. Configuración de VPC del área de Oficina B (Segundo Nivel):
![PC214 Oficina B](https://media.discordapp.net/attachments/764502305009303622/1208201572153032784/image.png?ex=65e26c66&is=65cff766&hm=a7fbea875fe162db930bef956f815610e3d21d6d87f38c9d1cbebbb20f4334e1&=&format=webp&quality=lossless&width=738&height=389)
7. Configuración de VPC del área de Oficina C (Segundo Nivel):
![PC220 Oficina C](https://media.discordapp.net/attachments/764502305009303622/1208201762746671164/image.png?ex=65e26c93&is=65cff793&hm=35086d2ba1472f2dbdc1033143b93e76d8b2d15afb56653a8a75f45d53462d4b&=&format=webp&quality=lossless&width=733&height=389)

## Pings entre los hosts (comunicación entre áreas, solo 3 en total, ustedes eligen)

1. Ping desde Recursos humanos (Primer nivel) de la PC 115 hacia Oficina B (Segundo nivel) PC 215.
![Ping de PC 115 hacia 215](https://media.discordapp.net/attachments/764502305009303622/1208240017252818994/image.png?ex=65e29034&is=65d01b34&hm=b9bb8dceb8e88397c0b4dacdd4582f3310704d26940b530bb7e8a884b95b00d1&=&format=webp&quality=lossless&width=740&height=389)

2. Ping desde Administración (Primer nivel) de la PC 111 hacia Atención al cliente (Primer nivel) PC 119.
![Ping de PC 111 hacia 119](https://media.discordapp.net/attachments/764502305009303622/1208240704795443210/image.png?ex=65e290d8&is=65d01bd8&hm=93530ec7f3f7f73c04e058ad56d033d90cbc78276939a583e3b40018c48a2f74&=&format=webp&quality=lossless&width=738&height=388)

3. Ping desde Oficina A (Segundo nivel) de la PC 213 hacia Oficina C (Segundo nivel) PC 221.
![Ping desde PC 213 hacia 221](https://media.discordapp.net/attachments/764502305009303622/1208241276344995860/image.png?ex=65e29160&is=65d01c60&hm=e50b4d29098a0e9ca42b3a88330bfb7267991050fe1225c2a0becede2304040c&=&format=webp&quality=lossless&width=740&height=389)

## Demostración de la captura de un paquete ARP/ICMP (solo 1 en general), incluyendo captura de pantalla

1. Se empieza a simular el ping desde la PC 117 de Recursos Humanos (Primer nivel) hacia la PC 212 de la Oficina A (Segundo nivel).

![Ping desde la PC 117 hacia 212](https://media.discordapp.net/attachments/764502305009303622/1208244013753180170/image.png?ex=65e293ec&is=65d01eec&hm=70a35545dcac42d7b04d2ff4e72511e23bed0588ee3bc8a1c5ed8d740334f57b&=&format=webp&quality=lossless&width=741&height=389)

2. Mensaje de difusión para conocer la dirección MAC de la PC a la que se quiere hacer ping.
![Mensaje de difusión](https://media.discordapp.net/attachments/764502305009303622/1208244692349616189/image.png?ex=65e2948e&is=65d01f8e&hm=cf6a2d496fd4454ae86be88456e738f4fa88c732083174cb7e0abec6c37d2c9e&=&format=webp&quality=lossless&width=728&height=389)

3. Fin de simulación de la captura de paquete ARP/ICMP
![ARP/ICMP](https://media.discordapp.net/attachments/764502305009303622/1208246138327801866/image.png?ex=65e295e7&is=65d020e7&hm=cc6598b208d85a4c8e213a4cd4dd7adc37cd070cd743278ed6aa4faaf24a00b6&=&format=webp&quality=lossless&width=740&height=389)

4. Tabla final ARP de la PC 117 que ya conoce la dirección MAC de la PC 212 y la guarda en su tabla ARP.
![Tabla ARP 117](https://media.discordapp.net/attachments/764502305009303622/1208246444427972668/image.png?ex=65e29630&is=65d02130&hm=c7972f8ea709ba7100c60ef028e3a1866ee0de81edec3ac5fe5b14e03457c30c&=&format=webp&quality=lossless&width=738&height=389)
