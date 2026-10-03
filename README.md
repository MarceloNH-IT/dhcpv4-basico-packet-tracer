# 🌐 Configuración de Servidor DHCPv4 en Cisco Packet Tracer

Pequeño proyecto de redes enfocado en la automatización de asignación de direcciones IP mediante un router Cisco actuando como servidor DHCPv4, utilizando un switch de capa 2 y equipos cliente (PCs).

# 🛠️ Topología Utilizada
* **Router Cisco (1941)**: Configurado como puerta de enlace (`192.168.10.1`) y servidor DHCP.
* **Switch Catalyst (2960)**: Dispositivo de capa 2 para la distribución local.
* **PCs (End Devices)**: Equipos cliente configurados para recibir dirección IP de forma dinámica.

---

# ⚙️ Comandos Principales Aplicados

### 1. Configuración de la Interfaz del Router (Gateway)
```text
enable
configure terminal
interface g0/0
ip address 192.168.10.1 255.255.255.0
no shutdown
exit
```
# 2. Creación del Pool DHCP y Exclusión de IPs Estáticas
```text
ip dhcp excluded-address 192.168.10.1 192.168.10.10
ip dhcp pool MI_RED_LOCAL
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
dns-server 8.8.8.8
exit
```
📊 Evidencias y Pruebas de Funcionamiento
Asignación DHCP Exitosa en PCs:
(Aquí puedes insertar o arrastrar las imágenes de tus capturas de PC0 y PC1 mostrando el "DHCP request successful")

Prueba de Conectividad (Ping 0% de pérdida):
(Aquí puedes insertar o arrastrar la captura de la consola con el comando ping respondiendo exitosamente)



