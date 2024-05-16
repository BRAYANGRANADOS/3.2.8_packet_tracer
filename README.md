# 3.2.8_packet_tracer

## 3.2.8 Packet Tracer - Investigate a VLAN Implementation
![descarga](https://github.com/BRAYANGRANADOS/3.1.4_packet_tracer/assets/97776616/f6c3775a-7182-4223-b129-d2ffc1650301)

### PREGUNTAS PARTE 1

> [!NOTE]
> &#9312; c.	Haga clic en el botón Capture/Forward para avanzar por el proceso. Observe las peticiones ARP a medida que atraviesan la red. Cuando aparezca la ventana Buffer Full (Búfer lleno), haga clic en el botón View Previous Events (Ver eventos anteriores).
Preguntas:
¿Fueron correctos los pings? Explique.
> 
> &#9313; Examine el panel de simulación, ¿dónde envió el paquete el S3 después de recibirlo?
>
>  &#9314; b.	Haga clic en el botón Capture/Forward para avanzar por el proceso. Observe las peticiones ARP a medida que atraviesan la red. Cuando aparezca la ventana Buffer Full (Búfer lleno), haga clic en el botón View Previous Events (Ver eventos anteriores).
Pregunta:
¿Fueron correctos los pings? Explique.
>
>  &#9315; c.	Examine el panel de simulación.
Pregunta:
Cuando el paquete llegó al S1, ¿por qué también se reenvió a la PC7?
> 

### RESPUESTA PARTE 1
> [!IMPORTANT]
> &#9312; R// No, los pings no se realizaron correctamente, porque la PC1 está en una VLAN diferente que la PC6, lo que no permite que estos dispositivos se comuniquen entre sí porque están separados de manera lógica.
> 
> &#9313; R//El S3 lo envió a la PC4 porque estaba en la misma VLAN que la PC1.
>
> &#9314; R// Sí, porque tanto la PC1 como la PC4 pertenecen a la VLAN 10, por lo tanto, la ruta de la solicitud de ARP es la misma que antes. Como PC4 es el destino, responde a la petición ARP. Entonces, PC1 puede enviar el ping con la dirección MAC de destino para PC4.
>
> &#9315; R// Porque la PC7 también pertenece a la VLAN 10, y las solicitudes de ARP eran para la VLAN 10. Los switches reenvían los paquetes a cualquier dispositivo que esté conectado a la VLAN 10 en su puerto.
>

### PREGUNTAS PARTE 2
> [!NOTE]
> &#9312; b.	Elimine la configuración de inicio en los tres switches.
Preguntas:
¿Qué comando se utiliza para eliminar la configuración de inicio de los switches?
> 
> &#9313; ¿Dónde se almacena el archivo VLAN en los switches?
>
>  &#9314; c.	Elimine el archivo VLAN en los tres switches.
Pregunta:
¿Qué comando elimina el archivo VLAN almacenado en los switches?
>
### RESPUESTA PARTE 2
> [!IMPORTANT]
> &#9312; R// Switch# erase startup-config
> 
> &#9313; R//flash:vlan.dat
> 
> &#9314; R// Switch# delete vlan.dat
>
### PREGUNTAS DE REFLEXION
> [!NOTE]
> &#9312;	Si un equipo en la VLAN 10 envía un mensaje de difusión, ¿qué dispositivos lo reciben?
>
> &#9313; Si una computadora en la VLAN 20 envía un mensaje de difusión, ¿qué dispositivos lo reciben?
>
> &#9314; Si una computadora en la VLAN 30 envía un mensaje de difusión, ¿qué dispositivos lo reciben?
>
> &#9315; ¿Qué le sucede a una trama enviada desde un equipo en la VLAN 10 hacia un equipo en la VLAN 30?
>
> &#9316;5.	Desde el punto de vista de los puertos, ¿cuáles son los dominios de colisiones en el switch?
>
> &#9317; Desde el punto de vista de los puertos, ¿cuáles son los dominios de difusión en el switch?
>
### RESPUESTA DE REFLEXION
> [!IMPORTANT]
> &#9312; R// Todos los dispositivos que están en la VLAN 10.
> 
> &#9313; R// Todos los dispositivos que están en la VLAN 20.
>
> &#9314; R// Todos los dispositivos que están en la VLAN 30.
>
> &#9315; R//Lo descarta.
>
> &#9316; R// Cada puerto es un dominio de colisiones diferente.
>
> &#9317; R// Se dividen por la cantidad de VLAN en el switch.
>
