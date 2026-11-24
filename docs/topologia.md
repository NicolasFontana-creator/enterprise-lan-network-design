# Topología y dominios de difusión

Tres routers Cisco 2911 enlazan las sedes en línea. Cuatro switches Cisco 2960 conectan once PC y cuatro servidores. Central utiliza dos switches y reúne tres PC de Administración. Norte y Sur utilizan un switch y cuatro PC cada una. Las subredes pertenecen exclusivamente al escenario simulado.

| Sede | VLAN | Sector | Subred IPv4 |
|---|---:|---|---|
| Central | 10 | Administración | 192.168.10.0/24 |
| Central | 99 | Servidores | 192.168.99.0/24 |
| Norte | 20 | Ventas | 192.168.20.0/24 |
| Norte | 50 | Soporte | 192.168.50.0/24 |
| Sur | 30 | Producción | 192.168.30.0/24 |
| Sur | 40 | Visitantes | 192.168.40.0/24 |

Los puertos de acceso asocian cada equipo a su VLAN. Los troncales IEEE 802.1Q transportan las VLAN habilitadas en cada sede. En Router-on-a-Stick, una subinterfaz de G0/0 por VLAN proporciona la puerta de enlace local. Así, una trama que debe salir de su subred llega etiquetada al router y se reenvía según la tabla IPv4.

| Enlace enrutado | Extremo inicial | Extremo final |
|---|---|---|
| Central–Norte | R1 G0/1 · 10.0.12.1/30 | R2 G0/1 · 10.0.12.2/30 |
| Norte–Sur | R2 G0/2 · 10.0.23.1/30 | R3 G0/1 · 10.0.23.2/30 |

Fuente: informe de redes, pp. 4–19. [Topología del informe](../figures/topologia.webp).
