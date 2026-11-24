# Enrutamiento y servicios centralizados

OSPFv2 anuncia seis LAN y dos redes de tránsito en el área 0. Los identificadores lógicos de R1, R2 y R3 son 1.1.1.1, 2.2.2.2 y 3.3.3.3. Las interfaces hacia los usuarios son pasivas. Las adyacencias se forman en los enlaces entre routers. Norte aprende los prefijos de ambas sedes y reenvía el tráfico entre ellas (pp. 20–24).

| Servicio en VLAN 99 | Función comprobada en el escenario |
|---|---|
| DHCP | Cinco ámbitos para clientes. Las subinterfaces de usuario retransmiten las solicitudes al servidor 192.168.99.40. El servidor elige el ámbito según la red indicada por el relay. Los servidores usan direcciones estáticas. |
| DNS | El registro A de www.andes.test apunta al servidor HTTP 192.168.99.20. El cliente consulta primero al servidor DNS 192.168.99.10. |
| HTTP | Clientes de distintas sedes solicitan la página corporativa tras resolver el nombre y establecer la conexión TCP. |
| SMTP y POP3 | Los clientes del laboratorio envían correo al servidor mediante SMTP y recuperan mensajes mediante POP3. |

El modo Simulation permite seguir el descubrimiento, oferta, solicitud y confirmación de DHCP, la consulta y respuesta DNS y la transferencia HTTP. Una concesión válida resuelve la configuración local; el acceso por nombre requiere también ruta de retorno, DNS y servicio de destino.

Fuente: pp. 24–38. [Pruebas por capa](verificacion.md).
