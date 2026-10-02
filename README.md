# dhcpv4-basico-packet-tracer
Laboratorio básico de configuración de servidor DHCPv4 en router Cisco e interfaces de red, con pruebas de conectividad exitosas.

# 🌐 Configuración de Servidor DHCPv4 en Cisco Packet Tracer

Pequeño proyecto de redes enfocado en la automatización de asignación de direcciones IP mediante un router Cisco actuando como servidor DHCP.

## 🛠️ Topología Utilizada
* **Router Cisco (1941)**: Configurado como puerta de enlace (`192.168.10.1`) y servidor DHCP.
* **Switch Catalyst (2960)**: Dispositivo de capa 2 para la distribución local.
* **PCs (End Devices)**: Equipos clientes configurados para recibir IP por DHCP.

---

## ⚙️ Comandos Principales Aplicados

### 1. Configuración de la Interfaz del Router (Gateway)
enable
configure terminal
interface g0/0
ip address 192.168.10.1 255.255.255.0
no shutdown

### 2. Creación del Pool DHCP y Exclusión de IPs
ip dhcp excluded-address 192.168.10.1 192.168.10.10
ip dhcp pool MI_RED_LOCAL
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
dns-server 8.8.8.8

---

## 📊 Evidencias y Capturas de Prueba

* **Asignación DHCP Exitosa en PCs:**
  *(Aquí puedes subir la captura de la IP Configuration mostrando el "DHCP request successful")*

* **Prueba de Conectividad (Ping 0% de pérdida):**
  *(Aquí puedes subir la captura de la consola con el comando ping respondiendo sin pérdida de paquetes)*
  
