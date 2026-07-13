# Red Multicampus UAA

Diseño e implementación de una infraestructura de red multicampus para la Universidad Autónoma de Aguascalientes utilizando segmentación mediante VLANs, direccionamiento IPv4 con VLSM y enrutamiento estático en Cisco Packet Tracer.

El proyecto contempla la interconexión de tres sedes (Campus Central, Campus Sur y Campus Posta), permitiendo la comunicación entre departamentos mediante una arquitectura segmentada y escalable. Cada campus incorpora múltiples áreas funcionales aisladas mediante VLANs independientes y conectadas entre sí mediante configuraciones de routing.

Se consideró e implementó la comunicación entre sedes a través de enlaces dedicados y ruteo estático, permitiendo el intercambio de información entre todos los segmentos de la red.

Este proyecto integra conceptos de switching, routing, segmentación lógica, subneteo avanzado y administración de redes empresariales, ofreciendo una solución que simula la infraestructura de comunicaciones de una institución distribuida en múltiples campus universitarios.

## Tecnologías Utilizadas

- Cisco Packet Tracer
- IPv4
- VLSM (Variable Length Subnet Mask)
- VLANs
- Router-on-a-Stick
- Static Routing
- Switching
- Routing
- Redes LAN
- Redes Multicampus

## Arquitectura General

La red está compuesta por tres sedes:

* Campus Central
* Campus Sur
* Campus Posta

Cada una con 5 departamentos:

- Alumnos
- Docentes
- Control Escolar
- Recursos Humanos
- Redes

## Segmentación mediante VLANs

```tabla
|  VLAN   |   Departamento   |
|---------|------------------|
| VLAN 10 |      Redes       |
| VLAN 20 |     Alumnos      |
| VLAN 30 | Recursos Humanos |
| VLAN 40 |  Control Escolar |
| VLAN 50 |     Docentes     |
```

Cada departamento fue aislado mediante VLANs independientes para mejorar la seguridad, organización y administración de la red.

## Direccionamiento IP

Se realizó la planificación del direccionamiento mediante VLSM para optimizar el aprovechamiento de direcciones IPv4.

### Campus Central

```tabla
|   Departamento   | Hosts |
|------------------|-------|
|      Alumnos     |  200  |
|     Docentes     |  100  |
|  Control Escolar |   25  |
|      Redes       |   10  |
| Recursos Humanos |    8  |
```

### Campus Sur

```tabla
|   Departamento   | Hosts |
|------------------|-------|
|      Alumnos     |  100  |
|     Docentes     |   40  |
|  Control Escolar |   15  |
|      Redes       |    4  |
| Recursos Humanos |    2  |
```

### Campus Posta

```tabla
|   Departamento   | Hosts |
|------------------|-------|
|      Alumnos     |   50  |
|     Docentes     |   10  |
|  Control Escolar |    2  |
|      Redes       |    2  |
| Recursos Humanos |    1  |
```

## Interconexión de Campus

Los campus fueron interconectados mediante enlaces dedicados utilizando subredes /30:

- Campus Central <-> Campus Sur
- Campus Central <-> Posta
- Campus Sur <-> Posta

Esta configuración permite la comunicación directa entre sedes mediante ruteo estático.

## Configuraciones Implementadas

### Switching

- Creación de VLANs.
- Asignación de puertos a VLANs.
- Puertos Trunk.
- Cascadeo entre switches.
- Comunicación entre VLANs.

### Routing

- Router-on-a-Stick.
- Subinterfaces.
- Gateways para cada VLAN.
- Ruteo estático entre campus.

## Pruebas de Funcionamiento

Se realizaron pruebas de conectividad mediante el comando:

```bash
ping
```

Validando:

- Comunicación dentro de la misma VLAN.
- Comunicación entre VLANs.
- Comunicación entre diferentes campus.
- Funcionamiento correcto del ruteo estático.
- Correcta propagación de tráfico entre sedes.

Las pruebas se realizaron desde equipos pertenecientes a diferentes departamentos y campus para verificar la correcta implementación de la infraestructura de red.

## Estructura del Proyecto

```text
Red-Multicampus-UAA/
│
├── docs/
│   └── Documentacion-Tecnica-Red.pdf
│
├── network-planning/
│   └── Mapa-de-red.xlsx
│
├── packet-tracer/
│   └── Red-Multicampus-UAA.pkt
│
├── README.md
└── .gitignore
```

## Competencias Técnicas Aplicadas

Durante el desarrollo del proyecto se aplicaron conocimientos en:

- Diseño de redes LAN.
- Segmentación mediante VLANs.
- Planeación de direccionamiento IPv4.
- Subneteo mediante VLSM.
- Configuración de switches.
- Configuración de routers.
- Router-on-a-Stick.
- Ruteo estático.
- Diagnóstico y solución de problemas de conectividad.
- Diseño de infraestructuras de red multicampus.
- Administración de redes empresariales.

## Infraestructura de cada Campus

### Campus Central

Infraestructura:

- 2 switches.
- VLANs segmentadas por departamento.
- Router configurado mediante Router-on-a-Stick.
- Enlaces hacia Campus Sur y Posta.

### Campus Sur

Infraestructura:

- 1 switch.
- VLANs segmentadas por departamento.
- Router configurado mediante Router-on-a-Stick.
- Enlaces hacia Campus Central y Posta.

### Campus Posta

Infraestructura:

- 1 switch.
- VLANs segmentadas por departamento.
- Router configurado mediante Router-on-a-Stick.
- Enlaces hacia Campus Central y Sur.


## Documentación

El repositorio incluye:

- Reporte técnico completo del proyecto.
- Cálculos VLSM para cada campus.
- Tablas de direccionamiento IP.
- Diseño lógico de la red.
- Configuración de VLANs.
- Configuración de routers.
- Configuración de switches.
- Evidencias de funcionamiento.
- Mapa operacional de toda la infraestructura.

## Autores

- Suárez Vega, Vladimir
- Venegas Cons, Aída Montserrat
- Zermeño Ojeda, Paola Sarahi

## Nota

Proyecto desarrollado originalmente con fines académicos y educativos para practicar y fortalecer conocimientos relacionados con redes de computadoras, direccionamiento IPv4, subneteo mediante VLSM, segmentación mediante VLANs, switching, routing y diseño de infraestructuras de red multicampus.

### Historial del Proyecto

- Desarrollo original: **junio de 2026**.
- Publicación y documentación en GitHub: **julio de 2026**.