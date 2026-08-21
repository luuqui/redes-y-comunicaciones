## **1. ¿Qué es una red? ¿Cuál es el principal objetivo para construir una red?**

**Desde el punto informático ("Qué es una red de computadoras?"), es un grupo de dispositivos interconectados, donde su objetivo es compartir recursos, ya sean dispositivos, información o servicios.** 
**El conjunto computadoras, software de red, medios y dispositivos de interconexión forma un sistema de comunicación. Ejemplos: red de la sala de PCs, red universitaria, etc.**
## **2. ¿Qué es Internet? Describa los principales componentes que permiten su funcionamiento.**

**Internet es una red global de redes interconectadas que utiliza el conjunto de protocolos estandarizados TCP/IP para permitir la comunicación y el intercambio de datos entre millones de dispositivos en todo el mundo. Funciona bajo un esquema descentralizado donde la información se divide en pequeños fragmentos llamados paquetes, los cuales viajan de manera independiente desde un origen hasta un destino a través de múltiples rutas posibles.**

**![[Pasted image 20260820185014.png]]**

### **Componentes principales**
**Para que este intercambio de información sea posible, Internet se sostiene sobre cuatro pilares fundamentales:**
**1. Sistemas finales o Hosts (Sistemas Terminales)**
- **Dispositivos: Computadoras, teléfonos, servidores web o dispositivos IoT situados en los extremos de la red.**
- **Función: Generan, envían, reciben y procesan los datos finales que consumen los usuarios o las aplicaciones.**
**2. Infraestructura de Red y Medios de Transmisión**
- **Conmutadores de paquetes (Routers y Switches): Dispositivos encargados de dirigir el tráfico. Los _routers_ evalúan las direcciones de red y toman decisiones de encaminamiento para reenviar los paquetes hacia su destino por la ruta óptima.**
- **Medios físicos: Enlaces por los que viajan las señales electromagnéticas u ópticas, tales como cables de fibra óptica submarinos y terrestres, cables par trenzado (Ethernet), enlaces de microondas y conexiones satelitales.**
**3. Proveedores de Servicios e Interconexión (ISPs e IXPs)**
- **ISPs (Internet Service Providers): Empresas u organizaciones que brindan acceso a la red (clasificados en Tier 1, Tier 2 y Tier 3 según su cobertura y capacidad de enrutamiento).**
- **IXPs (Internet Exchange Points): Puntos de intercambio de tráfico donde múltiples redes e ISPs se conectan físicamente entre sí para intercambiar datos de forma eficiente sin intermediarios distantemente localizados.**
**4. Protocolos y Servicios de Soporte (Software y Reglas)**
- **Pila TCP/IP: El lenguaje común de la red. IP (Internet Protocol) se encarga del direccionamiento global y la entrega de paquetes, mientras que TCP (Transmission Control Protocol) garantiza la entrega confiable y ordenada de los datos.**
- **DNS (Domain Name System): El sistema jerárquico que traduce nombres de dominio legibles por humanos (como `unlp.edu.ar`) en direcciones IP numéricas que entienden los routers.**

## **3. ¿Qué son las RFCs?**

**Las RFCs (_Request for Comments_ o Petición de Comentarios) son una serie de documentos técnicos y formales que definen los estándares, protocolos, metodologías y conceptos de funcionamiento de Internet.**
**A pesar de su nombre histórico (que sugiere una consulta informal), representan la especificación técnica oficial sobre la cual se construye y actualiza la red.**
###### **Características clave**
- **Organismo emisor: Son desarrolladas y publicadas principalmente por la IETF (_Internet Engineering Task Force_), la organización abierta encargada de la estandarización técnica de Internet.**
- **Identificación numérica: Cada documento recibe un número único e incremental al momento de su publicación (por ejemplo, RFC 791 define el protocolo IP, RFC 793 define TCP, y RFC 2616 define HTTP/1.1).**
- **Inmutabilidad: Una vez que una RFC se publica, nunca se modifica. Si un protocolo evoluciona o se detecta un fallo, se redacta una nueva RFC que _obsoleta_ (_obsoletes_) o _actualiza_ (_updates_) a la anterior.**
- **Acceso público y abierto: Son de acceso gratuito para cualquier desarrollador, ingeniero o estudiante, lo que garantiza la interoperabilidad global: cualquier fabricante puede implementar un protocolo correctamente siguiendo su especificación.**

## **4. ¿Qué es un protocolo?**

**Un protocolo define el formato, el orden de los mensajes intercambiados y las acciones que se llevan a cabo en la transmisión y/o recepción de un mensaje u otro evento.}**

**Protocolo de Red: conjunto de reglas que especifican el intercambio de datos u órdenes durante la comunicación entre las entidades que forman parte de una red. Permiten la comunicación y están implementados en las componentes.**

## **5. ¿Por qué dos máquinas con distintos sistemas operativos pueden formar parte de una misma red?**

**Dos máquinas con distintos sistemas operativos (por ejemplo, una con Linux y otra con Windows) pueden comunicarse en una misma red porque ambas implementan los mismos estándares abiertos y protocolos de comunicación (la pila de protocolos TCP/IP).**
**Lo que permite esta interacción no es el código interno de cada sistema operativo, sino el cumplimiento estricto de las especificaciones definidas en los estándares internacionales (RFCs).**

**Arquitectura en capas: El modelo en capas abstrae los detalles de implementación. La capa de red (IP) o de transporte (TCP) funciona exactamente igual sin importar si la aplicación corre sobre Windows, Linux, macOS o Android.**
**Interfaz de red común: Todos los sistemas operativos se comunican con el hardware utilizando los mismos estándares de enlace y medios físicos (como Ethernet o Wi-Fi).**

## **6. ¿Cuáles son las 2 categorías en las que pueden clasificarse a los sistemas finales o End Systems? Dé un ejemplo del rol de cada uno en alguna aplicación distribuida que corra sobre Internet**

**Los sistemas finales o _End Systems_ se clasifican principalmente en dos categorías según el rol que desempeñan en las aplicaciones distribuidas: Clientes y Servidores.**
###### **Clasificación de Sistemas Finales**

**1. Clientes**
- **Definición: Equipos terminales (smartphones, PCs, notebooks) que inician activamente las peticiones de servicio a través de la red.**
- **Características: Suelen conectarse de forma intermitente, pueden cambiar de dirección IP dinámicamente y no se comunican directamente entre sí en el modelo tradicional.**
**2. Servidores**
- **Definición: Equipos o sistemas de cómputo que permanecen a la escucha de solicitudes entrantes para proveer recursos, datos o servicios a múltiples clientes.**
- **Características: Suelen estar encendidos permanentemente ($24/7$), cuentan con direcciones IP fijas o muy estables y residen en centros de datos (_Data Centers_) con alta capacidad de procesamiento y ancho de banda.**
###### **Ejemplo práctico en una aplicación distribuida**

**Tomando como ejemplo la navegación Web (protocolo HTTP/HTTPS):**
- **Rol del Cliente: Tu navegador web (Google Chrome o Firefox corriendo en tu PC). Inicia la comunicación enviando una solicitud `HTTP GET` para obtener el contenido de una página web específica.**
- **Rol del Servidor: El servidor web de la facultad (por ejemplo, corriendo en la infraestructura de la UNLP). Recibe la solicitud, procesa los archivos HTML, CSS e imágenes correspondientes y los envía de vuelta como una respuesta `HTTP 200 OK` al cliente.**
- 
> **Nota para la cátedra: En arquitecturas Peer-to-Peer (P2P) como BitTorrent, un mismo sistema final actúa simultáneamente como cliente (descargando partes de un archivo de sus pares) y servidor (subiendo partes a otros pares), rompiendo la jerarquía rígida del modelo centralizado.**

## **7. ¿Cuál es la diferencia entre una red conmutada de paquetes de una red conmutada de circuitos?**

**La diferencia principal radica en cómo se asignan y gestionan los recursos de la red durante la comunicación:**

| **Característica**         | **Conmutación de Circuitos (Circuit Switching)**                                                     | **Conmutación de Paquetes (Packet Switching)**                                                            |
| -------------------------- | ---------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **Reserva de Recursos**    | **Dedicada.** Se establece un camino físico/lógico exclusivo (_circuito_) antes de transferir datos. | **Compartida.** No hay reserva previa; los recursos se asignan bajo demanda (_almacenamiento y reenvío_). |
| **Uso del Ancho de Banda** | Ineficiente si hay silencio/inactividad (el canal queda reservado aunque no se use).                 | Altamente eficiente; aprovecha al máximo la capacidad compartida (**multiplexación estadística**).        |
| **Ruta de los Datos**      | Todos los datos siguen la misma ruta fija de principio a fin.                                        | Cada paquete puede tomar rutas distintas según el estado de congestión de la red.                         |
| **Rendimiento**            | **Garantizado y constante** (sin variaciones de retardo o pérdidas por congestión).                  | **Variable.** Puede sufrir retardos de cola o pérdida de paquetes en momentos de alta congestión.         |
| **Ejemplo Típico**         | Red telefónica tradicional (PSTN / RDSI).                                                            | **Internet** (IP), redes Ethernet.                                                                        |
### **Mapeo conceptual importante para la materia**
- **Conmutación de Circuitos: Funciona como una llamada telefónica. Primero "marcas" (estableces el circuito), se reservan los canales (mediante FDM o TDM) y hablas. Nadie más puede usar ese tramo reservado hasta que cuelgues.**
- **Conmutación de Paquetes: Funciona como el correo postal. La información se corta en fragmentos (paquetes), cada uno lleva la dirección de destino en su cabecera y los _routers_ deciden individualmente hacia dónde reenviarlos en cada salto.**

## **8. Analice qué tipo de red es una red de telefonía y qué tipo de red es Internet**

### **Red de Telefonía (Tradicional)**

**Es una red conmutada de circuitos (_Circuit-Switched Network_).**
- **Orientación a conexión: Antes de transmitir voz, requiere una fase explícita de establecimiento de llamada para reservar un camino físico/lógico continuo entre emisor y receptor.**
- **Recursos dedicados: Durante toda la comunicación, se asigna una porción fija e ininterrumpida de ancho de banda (vía FDM o TDM). Nadie más puede utilizar esa capacidad, lo que garantiza baja latencia y velocidad constante sin colas de espera.**
- **Cobro por tiempo/distancia: Históricamente, el costo dependía de la duración de la conexión y la distancia física del circuito reservado.**
### **Internet**

**Es una red conmutada de paquetes (_Packet-Switched Network_).**
- **Sin reserva previa de recursos: La información se fragmenta en pequeñas unidades (_paquetes_) que contienen datos y cabeceras de direccionamiento.**
- **Multiplexación estadística: Múltiples usuarios comparten los mismos enlaces físicos bajo demanda. Si un usuario no envía datos, el ancho de banda queda inmediatamente disponible para otros.**
- **Modelos Best-Effort: Los conmutadores (_routers_) procesan y reenvían cada paquete de manera independiente (almacenamiento y reenvío o _store-and-forward_). Si hay congestión, los paquetes sufren retrasos en colas de espera o pueden ser descartados.**

## **9. Describa brevemente las distintas alternativas que conoce para acceder a Internet en su hogar**

### 1. Conexiones Guiadas (por Cable)

- **FTTH (_Fiber To The Home_ - Fibra hasta el hogar):** El proveedor lleva un hilo de fibra óptica directamente hasta el interior de la vivienda. Ofrece las **mayores velocidades de bajada y subida (simetría)**, bajísima latencia y total inmunidad a interferencias electromagnéticas. Es la tecnología estándar actual en la mayoría de zonas urbanas.
- **HFC (_Hybrid Fiber-Coaxial_ - Híbrido de Fibra y Coaxial):** La red principal del proveedor usa fibra óptica hasta un nodo de la manzana o barrio, y la "última milla" hasta la casa se completa con **cable coaxial** (usado históricamente por la televisión por cable). Permite altas velocidades de bajada, pero la velocidad de subida suele ser menor y es algo más susceptible a la saturación.
- **xDSL (ADSL / VDSL):** Utiliza la infraestructura existente del **par de cobre del teléfono fijo**. La señal disminuye sensiblemente con la distancia a la central telefónica y ofrece velocidades acotadas (asimétricas). Hoy en día se encuentra prácticamente obsoleta o en fase de desmantelamiento en favor de la fibra.
### 2. Conexiones Inalámbricas

- **Redes Móviles (4G / 5G / Inalámbrico Fijo):** Se accede mediante un módem o enrutador con un chip SIM que se conecta a las antenas de telefonía celular más cercanas. La versión **5G residencial** ofrece velocidades comparables al cable, con la ventaja de no requerir instalaciones físicas en la calle.
- **Internet Satelital (GEO y LEO):** Un módem conectado a una antena parabólica en el hogar se comunica con satélites en órbita.
    - _Satelital tradicional (GEO):_ Cubre áreas remotas pero sufre de una latencia muy alta por la distancia.
    - _Satelital de baja órbita (LEO, ej. Starlink):_ Utiliza constelaciones a menor altitud, reduciendo significativamente la latencia y ofreciendo velocidades de banda ancha eficientes en zonas rurales o aisladas.
- **Inalámbrico Terrestre (Radioenlace / WISP):** Proveedores locales colocan una antena receptora en el techo de la casa orientada en línea de visión directa a una torre de transmisión. Se utiliza frecuentemente en zonas periurbanas o rurales donde la infraestructura por cable no llega.

## **10. ¿Qué ventajas tiene una implementación basada en capas o niveles?**

Una arquitectura basada en capas (como el modelo OSI o la pila TCP/IP) ofrece las siguientes ventajas clave para el diseño y funcionamiento de las redes:

- **Abstracción y modularidad:** Cada capa realiza un conjunto específico de funciones y oculta la complejidad interna a las capas superiores e inferiores.
    
- **Mantenibilidad y evolución independiente:** Permite modificar o actualizar la implementación del software/hardware de una capa sin afectar a las demás, siempre que la interfaz entre ellas no cambie (por ejemplo, cambiar de Ethernet a Wi-Fi en la capa de enlace no modifica el funcionamiento del navegador web en la capa de aplicación).
    
- **Interoperabilidad y estandarización:** Facilita que hardware y software de distintos fabricantes se comuniquen entre sí, ya que todos respetan las mismas interfaces y protocolos definidos para cada capa.
    
- **Simplificación del diseño:** Divide el problema complejo de la comunicación global en subproblemas más pequeños y fáciles de diseñar, depurar y enseñar.

## **11. ¿Cómo se llama la PDU de cada una de las siguientes capas: Aplicación, Transporte, Red y Enlace?**

Las Unidades de Datos del Protocolo (**PDU** - _Protocol Data Unit_) representan el bloque de información formateado que se transmite en cada capa específica del modelo de red:
- **Capa de Aplicación:** **Datos** o **Mensaje** (_Data_ / _Message_)
- **Capa de Transporte:** **Segmento** (_Segment_, en el protocolo TCP) o **Datagrama** (_Datagram_, en el protocolo UDP)
- **Capa de Red:** **Paquete** (_Packet_) o **Datagrama IP**
- **Capa de Enlace:** **Trama** (_Frame_)
> **Nota:** En la capa física (por debajo de la de enlace), la PDU pasa a ser simplemente una secuencia de **Bits**.
## **12. ¿Qué es la encapsulación? Si una capa realiza la encapsulación de datos, ¿qué capa del nodo receptor realizará el proceso inverso?**

La **encapsulación** es el proceso mediante el cual una capa emisora toma la PDU (_Protocol Data Unit_) proveniente de la capa superior y le añade información de control propia —por lo general en forma de un **encabezado** (_header_) al inicio y, en algunos casos como la capa de enlace, una **cola** (_trailer_) al final— formando así su propia PDU antes de pasarla a la capa inferior.
A medida que los datos bajan por la pila de protocolos del emisor:
1. La capa de **Aplicación** genera los datos o **Mensaje**.
2. La capa de **Transporte** añade su encabezado (con los puertos origen/destino) formando un **Segmento**.
3. La capa de **Red** agrega su encabezado (con las direcciones IP origen/destino) creando un **Paquete**.
4. La capa de **Enlace** suma su encabezado y cola (con las direcciones MAC origen/destino) obteniendo una **Trama**.
### Proceso inverso en el nodo receptor

El proceso inverso se conoce como **desencapsulación**.
La desencapsulación la realiza **la misma capa homóloga (paritaria)** en el nodo receptor. Es decir:
- La capa que desencapsula la información que fue encapsulada por una capa específica del emisor es **la capa equivalente en el receptor**.
**Por ejemplo:**
- Si la **capa de transporte del emisor** encapsuló un mensaje en un segmento, será la **capa de transporte del receptor** la que retirará ese encabezado para entregar el mensaje original a la capa de aplicación.

## **13. Describa cuáles son las funciones de cada una de las capas del stack TCP/IP o protocolo de Internet.**

El stack de protocolos **TCP/IP** (o arquitectura de Internet) se organiza en cuatro o cinco capas (según el modelo estándar de 4 capas de las RFCs o el modelo de 5 capas frecuentemente usado en la cátedra).
### 1. Capa de Aplicación

- **Función principal:** Ofrecer soporte y servicios de red directos a las aplicaciones del usuario final (navegadores, clientes de correo, etc.).
- **Responsabilidades:** Define los formatos de los mensajes de datos y las reglas con las que interactúan las aplicaciones.
- **Protocolos representativos:** HTTP/HTTPS (web), DNS (resolución de nombres), SMTP/IMAP (correo), FTP (transferencia de archivos).
- **PDU:** Mensaje / Datos.
### 2. Capa de Transporte

- **Función principal:** Proporcionar comunicación lógica de extremo a extremo (_end-to-end_) entre **procesos** que ejecutan en los hosts finales.
- **Responsabilidades:** Multiplexación y desmultiplexación mediante números de **puertos**. Según el protocolo utilizado, puede proveer control de flujo, control de congestión, retransmisión de datos perdidos y entrega ordenada.
- **Protocolos representativos:**
    - **TCP:** Orientado a conexión, confiable y con control de flujo/congestión.
    - **UDP:** No orientado a conexión, no confiable, liviano y sin garantías de entrega.
- **PDU:** Segmento (TCP) o Datagrama (UDP).
### 3. Capa de Red (o Internet)

- **Función principal:** Encaminar y mover paquetes desde el host origen hasta el host destino a través de múltiples redes e intermediarios (_routers_).
- **Responsabilidades:** Direccionamiento lógico global (direcciones IP), determinación de rutas (algoritmos de enrutamiento) y reenvío (_forwarding_) de paquetes en cada salto.
- **Protocolos representativos:** IP (IPv4 / IPv6), ICMP (mensajes de control y diagnóstico como `ping`), ARP.
- **PDU:** Paquete / Datagrama IP.
### 4. Capa de Enlace de Datos

- **Función principal:** Transferir datos entre **nodos adyacentes** que comparten un mismo medio físico de transmisión.
- **Responsabilidades:** Direccionamiento físico mediante direcciones **MAC**, detección/corrección de errores a nivel de enlace, control de acceso al medio compartido (MAC) y delimitación de trama.
- **Protocolos representativos:** Ethernet (802.3), Wi-Fi (802.11), PPP.
- **PDU:** Trama (_Frame_).
### 5. Capa Física

- **Función principal:** Transmitir la secuencia de **bits** individuales a través del medio de transmisión físico.
- **Responsabilidades:** Definir los aspectos mecánicos, eléctricos, ópticos y de señalización (voltajes, frecuencias, modulación, conectores y velocidad de transmisión).
- **Medios físicos:** Cable UTP (par trenzado), fibra óptica, ondas de radio (aire).
- **PDU:** Bits.

## **14. Compare el modelo OSI con la implementación TCP/IP**

El modelo **OSI** (un marco teórico de referencia de 7 capas) y la suite **TCP/IP** (la implementación práctica e histórica de 4/5 capas utilizada en Internet) presentan diferencias y similitudes clave:

| **Criterio**              | **Modelo OSI**                                                                                                 | **Implementación TCP/IP**                                                                             |
| ------------------------- | -------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Enfoque principal**     | Modelo **teórico y conceptual** normativo.                                                                     | Modelo **práctico y funcional** basado en la implementación real de Internet.                         |
| **Número de capas**       | **7 capas** (Aplicación, Presentación, Sesión, Transporte, Red, Enlace, Física).                               | **4 o 5 capas** (Aplicación, Transporte, Red/Internet, Enlace/Acceso a Red, Física).                  |
| **Capas superiores**      | Separa estrictamente la **Aplicación**, **Presentación** (formato/cifrado) y **Sesión** (gestión del diálogo). | Agrupa Presentación y Sesión dentro de la **Capa de Aplicación**.                                     |
| **Nivel de Red**          | Soporta servicios orientados a conexión y no orientados a conexión.                                            | En el nivel de red (IP), solo soporta servicios **no orientados a conexión** (_datagramas_).          |
| **Desarrollo e Historia** | Creado por la ISO de forma académica/teórica antes de probar la implementación de los protocolos.              | Surgió del trabajo práctico (DARPA/IETF) donde los protocolos se programaron e implementaron primero. |
### Similitudes Principales

- **Arquitectura en capas:** Ambos modelos dividen el proceso de comunicación en niveles funcionales y aislados.
- **Mismo propósito central:** Buscan resolver la comunicación entre sistemas finales interconectados mediante protocolos estandarizados.
- **Capas equivalentes:** Las funciones esenciales de las capas de **Transporte** y **Red** (o Internet) son prácticamente idénticas en la especificación teórica de ambos modelos.