# Pruebas y recuperación en Packet Tracer

| Pregunta | Evidencia del informe | Interpretación |
|---|---|---|
| ¿Está el host en su dominio de difusión? | VLAN de acceso, VLAN permitidas en los troncales y estado de subinterfaces, pp. 9–19 | Permite aislar errores de capa 2 antes de revisar rutas. |
| ¿Hay conectividad entre sedes? | Vecinos OSPF, rutas aprendidas y pruebas entre PC, pp. 20–25 | Las pruebas alcanzan destinos remotos a través del router de tránsito. |
| ¿Recibe parámetros un cliente nuevo? | Configuración IPv4 del cliente y secuencia DHCP, pp. 25–28, 36–37 | Se distingue la asignación remota de una dirección estática o una concesión anterior. |
| ¿Funciona la aplicación? | Acceso web y pruebas de envío y recepción de correo, pp. 29–36 | La prueba de aplicación añade evidencia más allá de la respuesta ICMP. |

**DNS detenido.** La p. 38 contrasta el ping a la IP con la consulta por nombre y muestra la verificación posterior a reactivar el servicio.

**DHCP detenido.** Una nueva solicitud pierde la posibilidad de obtener una concesión válida. Un cliente con concesión anterior puede conservarla. El informe registra la recuperación al habilitar DHCP (p. 39).

**Registro A incorrecto.** El servidor DNS sigue respondiendo, pero entrega otro destino. Se restaura el registro y se verifica el acceso HTTP (pp. 39–40).

La fuente documenta resultados funcionales simulados. No aporta medidas de disponibilidad, rendimiento físico ni un archivo .pkt para repetir independientemente la ejecución.
