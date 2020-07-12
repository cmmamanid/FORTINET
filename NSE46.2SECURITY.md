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
 
 ### Configuración predeterminada de Fábrica
 
 - Port1: 192.168.1.99/24
 - servicios habilitados PING, HTTP, HTTPS y SSH
 - DHCP server sobre Port1
 - Credenciales por defecto:
  ```
 user:admin
 password:enblanco
  ```
 - Puedes acceder a Fortigate por CLI
 
 ### Servicio de suscripción FortiGuard
 
 - Requiere conexión a internet y un contrato
 - Provee FDN
 - Actualización de Paquetes: FortiGuard Antivirus y IPS
 
 ```
 update.fortiguard.net
 TCP port 443(SSL)
 ```
 
 - Live queries: FortiGuard Web Filtering, DNS Filtering y Antispam
 
 ```
 service.fortiguard.net
 UDP port 53 o 8888
 
 securewf.fortiguard.net
 HTTPS sobre puerto 53 o 8888
 ```
### Métodos de administración:

- CLI (console, SSH, telnet, GUI widget)
- GUI (FortiExplore, Web Browser [HTTP,HTTPS])

### Comandos Básicos

Muestra el estado actual del fortigate
```
get system status
```
Muentra todos los valores de los atributos de configuración de una interface
```
show full-configuration system interface <port>
```
Muestra los valores de configuración de una interface
```
show system interface <port>
```





