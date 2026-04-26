# MODULOS DE CISCO

## Modulo 5

### Protocolo de comunicación

Son reglas esenciales para la comunicación en red. 
   
   - Formato y Tamaño: Estructura y dimensiones de los mensajes.
   - Sincronización: Velocidad de transmisión y gestión de tiempos.
   - Codificación: Conversión de bits a señales (luz, sonido o electricidad).
   - Encapsulación: Agregado de direcciones de origen y destino.
   - Patrón: Define si se requiere confirmación de recepción o no.

### Estándares de Comunicación

Reglas comunes que aseguran que dispositivos de distintos fabricantes funcionen entre sí.
  
   - Función: Permiten que los dispositivos se reconozcan y compartan datos en paquetes.
   - IETF: Organización que gestiona los estándares de Internet.
   - RFC: Documentos numerados que registran la evolución y aprobación de cada estándar.

### Modelos de Comunicación de Red

La comunicación se organiza en una pila de protocolos donde cada capa sirve a la superior.
   
   - TCP/IP: Modelo práctico de 4 capas.
   - Modelo OSI: Modelo de referencia universal creado por la ISO para diseño y resolución de problemas, enfocado en funciones teóricas.

### Descripción de la capa del modelo OSI

Divide el proceso en 7 niveles especializados.
   
   1. Físico: Transmisión de bits por medios físicos.
   2. Enlace de datos: Intercambio de tramas en un medio común
   3. Red: Direccionamiento y ruta de datos individuales
   4. Transporte: Segmentación y reensamblaje de datos.
   5. Sesión: Gestión del diálogo entre aplicaciones.
   6. Presentación: Formato común de los datos
   7. Aplicación: Interfaz para la comunicación proceso a proceso.

## MODULO 6

### Tipos de medios de red

Los medios de red son los canales por donde viaja la información desde el origen hasta el destino. Existen tres tipos principales. 

   - Hilos metálicos: Transmiten datos mediante impulsos eléctricos
   - Fibra óptica: Utiliza pulsos de luz.
   - Transmisión inalámbrica: Emplea ondas electromagnéticas.

Para elegir un medio de red se deben considerar factores como la distancia, el entorno de instalación, la cantidad y velocidad de datos y el costo.

## MODULO 7

### Encapsulación y la Trama de Ethernet

La encapsulación consiste en meter un mensaje dentro de otro formato para su envío; el proceso inverso es la desencapsulación.
   
   - Ethernet: Define reglas de formato, tamaño y temporización.
   - La Trama: Incluye direcciones MAC, preámbulo para sincronización, tipo de trama y una secuencia de verificación para detectar errores de transmisión.

### La Capa de Acceso

Es la primera línea de conexión que permite a los usuarios acceder a dispositivos finales, archivos e impresoras.
   
   - Evolución del Hardware: Hubs: Obsoletos; causaban colisiones al enviar mensajes simultáneos.
   - Switches: Dispositivos de capa 2 que eliminan colisiones y mejoran el rendimiento.
   - Funcionamiento del Switch: Utiliza una tabla de direcciones MAC para dirigir los datos solo al puerto correcto. Esta tabla se actualiza dinámicamente aprendiendo la dirección MAC origen de cada trama que recibe.

## MODULO 8 

### Propósito de la Dirección IPv4

Es una dirección lógica única que identifica a un dispositivo en una red LAN o en el mundo.
    
   - Asignación: Se configura en la interfaz de red, generalmente en la tarjeta de red del dispositivo.
   - Comunicación: Cada paquete enviado contiene una IPv4 de origen y una de destino.
   - Importancia: Esta información permite que los datos lleguen correctamente a su destino y que el receptor sepa a dónde devolver la respuesta.

### La Estructura de la Dirección IPv4

Es una dirección de 32 bits con una estructura jerárquica dividida en dos partes: porción de red y porción de host.

   - Red: Los primeros tres octetos.
   - Host: El último octeto.
   - Direccionamiento Jerárquico: Permite que los enrutadores solo necesiten saber cómo llegar a la red general en lugar de conocer la ubicación de cada dispositivo individual.
   - Redes Lógicas: Gracias a esta división, pueden existir múltiples redes lógicas dentro de una misma red física, siempre que tengan porciones de red diferentes.

### MODULO 9

### Unidifusión, difusión y multidifusión de IPv4

Define los tres métodos de envío de datos:
   
   - Unidifusión (Unicast): Comunicación uno a uno. El paquete va de un único origen a un único destino.
   - Difusión (Broadcast): Comunicación de uno a todos en la red local. Los routers no reenvían estos paquetes por defecto. La dirección limitada es 255.255.255.255.
   - Multidifusión (Multicast): Comunicación de uno a un grupo específico de suscritos. Utiliza el rango 224.0.0.0 a 239.255.255.255.

### Tipos de direcciones IPv4

   - Públicas vs. Privadas: Las públicas son para Internet; las privadas son para redes internas y requieren NAT para salir a la web.
   - Direcciones Especiales: Loopback: El host se dirige a sí mismo.
   - APIPA: Direcciones automáticas si no hay servidor DHCP.

Clasificación Histórica:
    
   - Clase A: Redes gigantes.
   - Clase B: Redes medianas.
   - Clase C: Redes pequeñas.

### Segmentación de la red

   - El Problema: Un dominio de difusión (broadcast) demasiado grande genera tráfico excesivo y reduce el rendimiento de la red.
   - La Solución (Subredes): Dividir una red grande en redes más pequeñas llamadas subredes.
   - Beneficios: Reduce el tráfico innecesario.
   - Mecanismo: Se toman prestados bits de la porción de host para crear estas subredes adicionales.

## MODULO 10

### Problemas con IPv4

   - Agotamiento: La falta de direcciones IPv4 impulsó la creación de IPv6, que usa 128 bits.
   - Mejoras: IPv6 incluye mejoras como ICMPv6, que facilita la configuración automática de dispositivos.
   - Técnicas de Transición: Para permitir la coexistencia de ambos protocolos, se usan tres métodos:
   - Doble pila: Los dispositivos ejecutan IPv4 e IPv6 simultáneamente.
   - Tunelización: Se encapsula un paquete IPv6 dentro de uno IPv4 para viajar por redes antiguas.
   - Traducción (NAT64): Traduce paquetes entre IPv6 e IPv4 para que dispositivos de distintas versiones se entiendan.

### Asignación de direcciones IPv6

Se escriben como 32 valores hexadecimales agrupados en 8 segmentos de 16 bits (hextetos). No distinguen entre mayúsculas y minúsculas. Reglas de compresión: Para acortar las direcciones, existen dos reglas clave:
   
   - Omitir ceros iniciales: Se pueden eliminar los ceros a la izquierda en cualquier hexteto.
   - Doble dos puntos: Reemplaza una cadena continua de uno o más hextetos compuestos solo por ceros. Solo se puede usar una vez por dirección para evitar ambigüedades.

## MODULO 11 

### Direccionamiento Estático y Dinámico

   - Asignación Estática: El administrador configura manualmente la IP, máscara y puerta de enlace en cada host. Ofrece mayor control, pero es lento y propenso a errores en redes grandes.
   - Asignación Dinámica (DHCP): Método preferido que asigna direcciones automáticamente.
   - Uso en el hogar: Los routers domésticos suelen actuar como servidores DHCP para asignar IPs a laptops y móviles automáticamente a través del ISP.

### Configuración de DHCPv4

Explica el proceso de intercambio de mensajes para obtener una IP:

   - DHCP Discover: El cliente envía una difusión buscando un servidor.
   - DHCP Offer: El servidor ofrece una dirección disponible.
   - DHCP Request: El cliente solicita permiso para usar esa dirección específica.
   - Confirmación: El servidor confirma la recepción y asigna la IP.

## MODULO 12

### Límites de la Red

   - Gateway (Puerta de enlace): Es la dirección IP del router que conecta la red local con otras redes. Los hosts deben conocerla para enviar datos fuera de su LAN.
   - Rol del Router: Actúa como el límite físico y lógico entre la red interna y el Internet externo.
   - Servicios: Generalmente, el router inalámbrico actúa como servidor DHCP para los hosts internos y como cliente DHCP para recibir una IP pública del proveedor de servicios.

### Funcionamiento de NAT

La NAT (Traducción de Direcciones de Red) es el proceso que convierte direcciones IPv4 privadas en una dirección pública enrutable en Internet.

   - Proceso de Salida: Cuando un paquete sale de la red local, el router reemplaza la IP privada de origen por su propia IP pública.
   - Proceso de Entrada: Para los paquetes que regresan, el router realiza el proceso inverso para entregar la información al host correcto.
   - Ventaja: Permite que cientos de dispositivos internos compartan una sola dirección IP pública, ahorrando espacio de direcciones.

## MODULO 13

### MAC e IP

Para que un host envíe datos en una red Ethernet, necesita dos direcciones principales:

   - Dirección física (MAC): Se encarga de la comunicación local entre tarjetas de red dentro de la misma red.
   - Dirección lógica (IP): Identifica el origen y el destino final del paquete, ya sea en la red local o en una remota.
     
El router desencapsula la trama en cada salto, analiza la IP de destino para encontrar la mejor ruta y vuelve a encapsular el paquete en una nueva trama hasta llegar al destino final.

### Contención de Difusiones

Este concepto explica cómo se gestionan los mensajes que deben llegar a todos los dispositivos de una red.

   - Dirección MAC de difusión: Es una dirección de 48 bits que todos los hosts aceptan.
   - Dominios de difusión: Son áreas de la red donde se propagan estos mensajes. Si hay demasiado tráfico de difusión, el rendimiento cae; para solucionarlo, se usan routers para dividir la red en varios dominios más pequeños.

## MODULO 14

### La Necesidad del Enrutamiento

A medida que las redes crecen, es fundamental dividirlas para mejorar el rendimiento y la organización. El enrutamiento en la capa de distribución permite:

   - Contención de difusión: Limita el tráfico innecesario a la red local.
   - Seguridad: Separa grupos de computadoras con información sensible.
   - Gestión geográfica y lógica: Interconecta ubicaciones distantes y agrupa usuarios por departamentos o necesidades comunes.
   - Punto clave: Mientras que los conmutadores usan direcciones MAC de Capa 2, los enrutadores toman decisiones basadas en direcciones IP de Capa 3 para mover datos entre redes diferentes.

### La Tabla de Enrutamiento

Cada enrutador posee una tabla que contiene las rutas hacia las redes conocidas y las interfaces por las que debe enviar los datos.

   - Proceso: Al recibir un paquete, el enrutador busca la IP de destino en su tabla. Si la encuentra, encapsula el paquete en una nueva trama y lo envía.
   - Destinos: El paquete puede ir directamente al host final o a otro enrutador en el camino.
   - Puerta de enlace predeterminada: Es la dirección IP de la interfaz del router conectada a la red local; los hosts la usan para enviar mensajes fuera de su propia red.
   - Actualización: Las tablas se llenan de forma dinámica o estática (configurada manualmente por un administrador).

### Crear una LAN

Una LAN es una red local bajo un mismo control administrativo que utiliza tecnologías como Ethernet o Wi-Fi para altas velocidades de transmisión.

   - Estructura: Se puede tener una sola red grande o varias pequeñas conectadas por un dispositivo de capa de distribución.
   - Ventajas de dividir: Colocar hosts en redes remotas reduce el impacto del tráfico excesivo en un solo dominio de difusión.
   - Consideraciones: Aunque dividir la red mejora el tráfico, requiere enrutamiento, lo cual añade cierta complejidad en la configuración y puede generar una ligera latencia entre redes.

## MODULO 15

### TCP y UDP

Estos son los dos protocolos principales de la capa de transporte, cada uno con un enfoque distinto según la necesidad de la aplicación

   - UDP (User Datagram Protocol): Es un sistema de entrega de "mejor esfuerzo". No requiere confirmación de recepción, lo que lo hace extremadamente rápido. Es ideal para aplicaciones en tiempo real como VoIP o streaming de audio, donde la velocidad es crítica y la pérdida de algunos paquetes es preferible a los retrasos por retransmisión.
   - TCP (Transmission Control Protocol): Se enfoca en la confiabilidad. Divide el mensaje en segmentos numerados. Si un segmento no llega o no se confirma en un tiempo determinado, TCP lo retransmite. Esto asegura que el mensaje llegue completo y en el orden correcto.

### Números de Puerto

Los puertos son identificadores numéricos que permiten a los dispositivos rastrear conversaciones específicas entre clientes y servidores. Van del 1 al 65,535 y se dividen en tres categorías administradas por la ICANN:

   - Puertos Conocidos (1 - 1023): Reservados para servicios y aplicaciones comunes (ej. HTTP en el puerto 80 o FTP en el 21).
   - Puertos Registrados (1024 - 49151): Utilizados por empresas para aplicaciones específicas.
   - Puertos Privados o Dinámicos (49152 - 65535): Asignados dinámicamente por el dispositivo emisor para identificar una sesión de cliente única.

## MODULO 16

### La Relación Cliente Servidor

Se basa en un modelo de solicitud y respuesta. El servidor ofrece servicios y el cliente los solicita. Para que se entiendan, usan protocolos y estándares como el URI, que se divide en URN y URL.

### Servicios de Aplicaciones de Red

Los servicios cotidianos dependen de la suite TCP/IP. Los protocolos más comunes para que clientes y servidores se comuniquen de forma fiable incluyen DNS, HTTP, FTP, SSH y protocolos de correo.

### Sistema de Nombres de Dominios (DNS)

Es el "directorio" de Internet. Traduce nombres legibles en direcciones IP. Si un servidor DNS local no tiene la dirección, consulta a otros hasta encontrarla y devolverla al host solicitante.

### Clientes y Servidores Web

El navegador solicita páginas al servidor usando el protocolo HTTP. Como HTTP no es seguro, se usa HTTPS (puerto 443) para cifrar los datos. El servidor responde enviando código HTML, que le indica al navegador cómo mostrar el contenido y los gráficos.

### Clientes y Servidores FTP

El protocolo FTP sirve para transferir archivos. Utiliza dos puertos: el 21 para comandos de control y el 20 para el movimiento real de datos. Permite subir, bajar y administrar archivos de forma remota, ya sea mediante comandos o interfaces gráficas (GUI).

### Terminales Virtuales

   - Telnet: Permite acceso remoto por texto (puerto 23), pero es inseguro porque no cifra los datos.
   - SSH: Es la alternativa moderna y segura. Proporciona autenticación fuerte y cifrado, por lo que es el estándar para profesionales de red.

### Correo Electrónico y Mensajería

Utiliza tres protocolos clave:

   - SMTP: Para enviar correos.
   - POP3: Descarga los correos y suele borrarlos del servidor.
   - IMAP4: Sincroniza y mantiene los correos en el servidor.
     
## MODULO 17

Comandos de solución de problemas

Son herramientas de línea de comandos que ayudan a identificar fallos en la red. Los más importantes son:

   - ipconfig: Muestra la configuración IP básica (dirección IP, máscara de subred y gateway).
       - ipconfig /all: Muestra detalles extra como la dirección MAC y servidores DNS.
       - ipconfig /release y /renew: Sirven para liberar y renovar la dirección IP asignada por DHCP.
   - Ping: Es la herramienta más usada. Envía una "solicitud de eco" a una IP; si el destino responde con una "respuesta de eco", se confirma que hay conectividad.
   - Netstat: Lista todas las conexiones de red activas.
   - Tracert: Muestra el camino exacto que recorren los datos hasta llegar a su destino.
   - Nslookup: Consulta directamente a los servidores de nombres para obtener información sobre un dominio.
