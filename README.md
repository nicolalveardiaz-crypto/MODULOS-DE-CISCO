# MODULOS DE CISCO

## Modulo 7

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

## MODULO 8 

### Tipos de medios de red

Los medios de red son los canales por donde viaja la información desde el origen hasta el destino. Existen tres tipos principales. 

   - Hilos metálicos: Transmiten datos mediante impulsos eléctricos
   - Fibra óptica: Utiliza pulsos de luz.
   - Transmisión inalámbrica: Emplea ondas electromagnéticas.

Para elegir un medio de red se deben considerar factores como la distancia, el entorno de instalación, la cantidad y velocidad de datos y el costo.

### MODULO 9

### Encapsulación y la Trama de Ethernet

La encapsulación consiste en meter un mensaje dentro de otro formato para su envío; el proceso inverso es la desencapsulación.
   
   - Ethernet: Define reglas de formato, tamaño y temporización.
   - La Trama: Incluye direcciones MAC, preámbulo para sincronización, tipo de trama y una secuencia de verificación para detectar errores de transmisión.

### La Capa de Acceso

Es la primera línea de conexión que permite a los usuarios acceder a dispositivos finales, archivos e impresoras.
   
   - Evolución del Hardware: Hubs: Obsoletos; causaban colisiones al enviar mensajes simultáneos.
   - Switches: Dispositivos de capa 2 que eliminan colisiones y mejoran el rendimiento.
   - Funcionamiento del Switch: Utiliza una tabla de direcciones MAC para dirigir los datos solo al puerto correcto. Esta tabla se actualiza dinámicamente aprendiendo la dirección MAC de origen de cada trama que recibe.

## MODULO 10

### Propósito de la Dirección IPv4

Es una dirección lógica única que identifica a un dispositivo en una red LAN o en el mundo.
    
   - Asignación: Se configura en la interfaz de red, generalmente en la tarjeta de red del dispositivo.
   - Comunicación: Cada paquete enviado contiene una IPv4 de origen y una de destino.
   - Importancia: Esta información permite que los datos lleguen correctamente a su destino y que el receptor sepa a dónde devolver la respuesta.

## MODULO 11 

### La Estructura de la Dirección IPv4

Es una dirección de 32 bits con una estructura jerárquica dividida en dos partes: porción de red y porción de host.

   - Red: Los primeros tres octetos.
   - Host: El último octeto.
   - Direccionamiento Jerárquico: Permite que los enrutadores solo necesiten saber cómo llegar a la red general en lugar de conocer la ubicación de cada dispositivo individual.
   - Redes Lógicas: Gracias a esta división, pueden existir múltiples redes lógicas dentro de una misma red física, siempre que tengan porciones de red diferentes.

## MODULO 12

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
   - Mecanismo: Se toman prestados bits de la porción de host para crear estas subredes adicionales
   
## MODULO 13

