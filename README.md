# Laboratorio de Seguridad de Redes con FortiGate

## Información del proyecto

**Estudiante:** Noel Elias Nova Vargas  
**Matrícula:** 20242293  
**Asignatura:** Seguridad de Redes  
**Docente:** Jonathan Rondon  

## Descripción

Este proyecto presenta la implementación de un laboratorio de seguridad de redes utilizando FortiGate como dispositivo principal de seguridad.

La solución incluye segmentación mediante VLAN, direccionamiento IP, DHCP, políticas de firewall, NAT, inspección de tráfico, protección contra ataques DoS y mecanismos adicionales de seguridad.

## Segmentación de la red

| VLAN | Descripción | Red |
|---|---|---|
| VLAN 10 | Usuarios | 10.229.3.0/25 |
| VLAN 20 | Servidores / WEB | 10.229.3.128/28 |
| VLAN 30 | Base de datos | 10.229.3.144/28 |

## Direccionamiento principal

- **FortiGate VLAN 10:** 10.229.3.1
- **FortiGate VLAN 20:** 10.229.3.129
- **WEB-SERVER:** 10.229.3.130
- **FortiGate VLAN 30:** 10.229.3.145
- **DB-SERVER:** 10.229.3.146
- **LINUX-CLIENT:** 10.229.3.11

## Controles de seguridad implementados

- VLAN y segmentación de red
- DHCP
- Firewall
- NAT
- Ruta por defecto
- Acceso HTTPS
- Control de acceso a la base de datos
- Web Application Firewall (WAF)
- Web Filter
- File Filter
- Deep Inspection
- Protección contra ataques DoS
- Cuarentena del atacante

## Pruebas realizadas

### Acceso HTTPS

Se comprobó el acceso desde el cliente hacia el servidor web mediante HTTPS utilizando TCP/443.

### Bloqueo de usuarios hacia la base de datos

Se comprobó que los usuarios de VLAN 10 no pueden acceder directamente al servidor de base de datos mediante TCP/3306.

### Comunicación WEB → DB

Se comprobó que el servidor web puede comunicarse con la base de datos mediante TCP/3306.

También se comprobó que otros puertos no necesarios no están permitidos.

### Protección DoS

Se generaron múltiples solicitudes hacia el servidor web y FortiGate detectó el comportamiento, bloqueando al cliente y colocándolo temporalmente en cuarentena.

## Documentación

El informe completo del proyecto se encuentra en la carpeta:

`Documentacion/`

## Evidencias

Las capturas de pantalla y evidencias de las pruebas se encuentran en:

`Evidencias/`

## Configuraciones

Las configuraciones utilizadas en el laboratorio se encuentran en:

`Configuraciones/`

## Video de demostración

**Enlace:** PENDIENTE DE AGREGAR

## Autor

**Noel Elias Nova Vargas**  
**Matrícula: 20242293**
