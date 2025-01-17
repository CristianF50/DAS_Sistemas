## ¿Qué lenguaje de programación utiliza el equipo de Netflix?
Se utiliza Python.

## ¿Qué sucedía con la base de datos de Oracle del monolito de Netflix?
El servicio de base de datos de Oracle en IBM no es economico, por lo que optaron por usar AWS ya que esta era mas economica en comparación.

## ¿Cuál fue una de las principales desventajas que el equipo de Netflix tuvo con la arquitectura monolítica?
Las grandes dificultades de escalar una aplicación monolitica, ya que la información del usuario aumentaba rápidamente, y era dificil almacenarla en su sistema de base de datos en aquel entonces, lo cual causaba muchos problemas y decidieron migrar a una arquitectura de microservicios.

## ¿A qué autor cita el ponente cuando da el concepto de un microservicio?
Martin Fowler.

## ¿Cuáles son las 3 principales ventajas que el ponente cita sobre los microservicios?
Eso sería agilidad. La capacidad de iterar en una pequeña pieza de funcionalidad enfocada rápidamente y ver resultados.

## ¿Qué analogía se utiliza para comparar los microservicios con la vida real?
Se utiliza la analogia como órganos en un sistema de órganos y estos sistemas que luego se unen para formar los organismos en general.

## Describe al menos 3 diferentes tipos de servicios que Netflix tenía en su arquitectura en aquel entonces
Las Recomendaciones este iba dentro del Producto, este servicio se encargaba del algoritmo con el que mostraban recomendaciones a los usuarios, Routing, y obviamente el servicio de la Base de Datos, que iba dentro de Persistencia.

## ¿Cuáles son las áreas primarias que se proponen para los retos y soluciones de utilizar microservicios?
Se proponen utilizar en aplicaciones en donde se ve un crecimiento muy rápido, donde de tener una arquitectura monolitica no de abasto para este crecimiento, y asi poder escalar fácilmente la aplicación.
    
## ¿Qué es el falló en cascada?
Cuando uno de los servicios falla, este puede provocar que algun otro falle y asi sucesivamente con todos los servicios.

## ¿Qué es Hystrix?
Hystrix es una biblioteca que controla la interacción entre microservicios para proporcionar latencia y tolerancia a fallas.

## ¿Qué analogía utiliza el ponente para comparar las librerias de cliente con la vida real?
Como una infección parasitaria.

## ¿De qué manera el equipo de Netflix manejo el problema de la persistencia en microservicios?
Empezando a pensar sobre las construccciones correctas y con el CAP Theorem, establece que es posible optimizar para cualquiera de las siguientes 2: consistencia, disponibilidad y tolerancia de partición de red, pero no los tres al mismo tiempo.

## ¿Cuál fue la estrategia de Netflix después de que sufrieron la caída del 24 de Diciembre del 2012?
Su estrategia fue aislar regiones, para que las interrupciones en los EE.UU. O Europa no se afecten entre sí.

## ¿Cuáles son los 3 escenarios/casos que se plantean para la parte de escalamiento?
Varios grupos pueden trabajar en conjunto, aumenta la productividad del equipo de DevOps, y es encaja perfectamente para aplicaciones grandes.

## ¿De qué manera se describe un "stateless service" en el video?
Es algo parecido a una base de datos, no se almacenan cantidades masivas de informacion, se tienen los metadatos más accesados en cache, asi que su naturaleza es no volatil, o de configuracion de información.

## ¿Qué es Chaos Monkey?
Es una estrategia que se utiliza a la hora de desplegar una actualizacion, si esta tiene un error sea posible regresar a la version estable de manera rapida

## ¿Qué es un microservicio híbrido?
Lo describe como "Es fácil de tomar EVCache asegurado", 30 millones de peticiones por segundo, 2 trillones de peticiones por día globalmente, miles de millones de objetos, 10 mil instancias de memcached, milisegundos de latencia por peticion.

## ¿Cómo solucionó el equipo de Netflix el problema con el anti-patrón de carga excesiva?
Usando una tecnología llamad "EVCache" el cual es esencialmente un wrapper alrededor de memcache D, multiples copias son escritas a multiples nodos, asi que cada vez que una escritura pasa no solo se escribe en multiples nodos, sino que los escribe en varias zonas de accesibilidad.

## ¿Qué tecnologías nuevas integró el equipo de Netflix cuando comenzó a manejar contenedores?
Node.js y Docker.

## ¿Cuáles fueron algunos de los principales costos de varianza del equipo de Netflix?
Hacer las operaciones automaticamente.

## ¿Qué es Spinnaker?
Es un administrador de aplicaciones, el cual permite hacer cambios de software con una velocidad alta y confidencia.

## ¿Cómo manejo Netflix el problema de las arquitecturas híbridas?
La solución fue eliminar completamente las unidades centrales de su arquitectura, por lo que los nodos comparten los mismos privilegios y responsabilidades de un cliente y un servidor.

## ¿Qué es "chaos engineering" o "ingeniería del caos"?
Es la disciplina de experimentar en un software en producción para asi crear confidencia en la capabilidad del sistema para soportar condiciones inesperadas y turbulentas.