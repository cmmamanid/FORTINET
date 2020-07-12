# FORTIGATE SECURITY
## FortiOS 6.2

En la actualidad se espera que un FW realice diversas funciones, más que gatekeepers, en el perimetro de nuestra red.

### Modos de implementación:
- Distributed enterprise firewall
- Next-generation firewall
- Internal segmentation firewall
- Data center firewall

*Un Fortigate además brinda funciones de DNS y DHCP server, y puede ser configurado para brindar web filter, anti-virus y servicios IPS.*

Fortigate VM: tiene las mismas características que un appliance físico a diferencia del FortiASIC, el cuál es el procesador de la gama media y alta de Fortigate.
Con el siguiente comando, se podrá conocer (via CLI) los puertos asociados a cada FortiASIC NP:

 ```
 diagnose npu npX list   -> donde NPX puede ser NP2, NP4 ó NP6 según corresponda
 ```
 
 ### SPUs
 La mayoría de los modelos FortiGATE tienen hardware de aceleración especializado, llamado SPU que puede descargar el procesamiento intensivo de recursos de los recursos de procesamiento principal (CPU).
 
 SPUs (Contd)
 - Content Processor: Inpección de contenido, SSL, Antivirus
 - Security Processor: IPS, relacionado con las interfaces de red
 - Network Processor: Procesamiento de paquetes, relacionado con las interfaces de red.
 - System-on-a-Chip Processor: Optimiza el rendimiento para un nivel de entrada
 
 ### Modos de Operación
 
 **NAT**
 - FortiGATE trabaja como un enrutador de capa 3
 - Interfaces tiene direcciones IP
 - Los paquetes son enrutados sobre IP
 
 **TRANSPARENT**
 - FortiGATE trabaja como un switch de capa 2 o un bridge
 - Interfaces no poseen direcciones IP
 - Los paquetes no son enrutados, solo reenviados o bloqueados
 
 
 
 
 
 
