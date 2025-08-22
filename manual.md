# Manual Técnico – Práctica 1  
**Curso:** Redes de Computadoras 1  
**Alumno:** Sergio [Tu Apellido]  
**Carnet:** 201800673  
**Universidad San Carlos de Guatemala – Facultad de Ingeniería**

---

## 📌 1. Tabla de Direcciones IP

La red base utilizada es: **192.168.73.0/24**  
Máscara: **255.255.255.0**  
Rango de hosts: **192.168.73.1 – 192.168.73.254**

| Piso | Departamento / Área         | Dispositivos | Rango de IPs asignadas        |
|------|-----------------------------|--------------|--------------------------------|
| 1    | Recepción                   | 12 PCs       | 192.168.73.1 – 192.168.73.12  |
| 1    | Contabilidad                | 8 PCs        | 192.168.73.13 – 192.168.73.20 |
| 1    | Legal                       | 5 PCs        | 192.168.73.21 – 192.168.73.25 |
| 1    | Sala de Reuniones           | 5 PCs        | 192.168.73.26 – 192.168.73.30 |
| 2    | Arquitectura                | 6 PCs        | 192.168.73.31 – 192.168.73.36 |
| 2    | Urbanismo                   | 6 PCs        | 192.168.73.37 – 192.168.73.42 |
| 2    | Sala de Revisión de Planos  | 5 PCs        | 192.168.73.43 – 192.168.73.47 |
| 3    | Dirección General           | 4 PCs        | 192.168.73.48 – 192.168.73.51 |
| 3    | Ingeniería Civil            | 6 PCs        | 192.168.73.52 – 192.168.73.57 |
| 3    | Servidores Principales      | 3 Servidores | 192.168.73.250 – 192.168.73.252 |

---

## 📌 2. Configuración de Switches

Todos los switches utilizados son modelo **Cisco 2960**.  

Configuración básica en CLI (ejemplo para el switch del departamento de Recepción en el Piso 1):  

```bash
enable
configure terminal
line console 0
password 201800673
login
end
exit
```
👉 Hostnames asignados:

Piso 1: SW_L1, SW_L1_RECEPCION, SW_L1_CONTABILIDAD, SW_L1_LEGAL, SW_L1_REUNIONES

Piso 2: SW_L2, SW_L2_ARQUITECTURA, SW_L2_URBANISMO, SW_L2_REUNIONES

Piso 3: SW_L3, SW_L3_DIRECCION, SW_L3_INGENIERIA, SW_L3_SERVIDORES

## 📌 3. Configuración de VPCs

Cada PC/Laptop/Servidor fue configurado con una IP estática en la red 192.168.73.0/24.

Ejemplo (PC1 del área de Recepción):

IP Address: 192.168.73.1
Subnet Mask: 255.255.255.0
Gateway: (no requerido)

## 📌 4. Pruebas de Conectividad

Se realizaron pruebas de ping entre dispositivos de distintas áreas para verificar comunicación:

Recepción (192.168.73.1) → Contabilidad (192.168.73.13)

Legal (192.168.73.21) → Sala de Reuniones (192.168.73.26)

Arquitectura (192.168.73.31) → Urbanismo (192.168.73.37)

Arquitectura (192.168.73.32) → Revisión de Planos (192.168.73.43)

Dirección General (192.168.73.48) → Ingeniería Civil (192.168.73.52)

Dirección General (192.168.73.49) → Servidor 1 (192.168.73.250)

Recepción (192.168.73.2) → Arquitectura (192.168.73.35)

Contabilidad (192.168.73.18) → Ingeniería Civil (192.168.73.55)

Urbanismo (192.168.73.40) → Servidor 2 (192.168.73.251)

Sala de Reuniones (192.168.73.29) → Sala de Revisión de Planos (192.168.73.45)

Se pueden obserbar dispositivos conectados en las capturas de pantalla

## 📌 5. Capturas en Modo Simulación

En el Simulation Mode de Packet Tracer se capturaron:

ARP: Petición/respuesta de dirección MAC.

ICMP: Paquete de ping de un host en Recepción a un host en Urbanismo.

no me sube ;((
asdfasd