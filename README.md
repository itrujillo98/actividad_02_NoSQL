# actividad_02_NoSQL

Escenario: El escenario es un sistema de base de datos que gestiona los datos de un evento deportivo, donde se deben almacenar grandes volúmenes de información, como los resultados de partidos, detalles de jugadores, estadísticas, etc. Este sistema necesita escalar adecuadamente debido al volumen de datos y a la necesidad de alto rendimiento.

Requerimientos no funcionales:
Escalabilidad: El sistema debe poder manejar grandes volúmenes de datos generados por el evento deportivo.
Rendimiento: Se debe optimizar el tiempo de respuesta de las consultas, especialmente aquellas que se realizan sobre grandes cantidades de datos.
Disponibilidad: El sistema debe estar disponible y funcionando sin caídas, incluso cuando se incrementa el volumen de datos.
Integridad de los datos: Debe garantizarse que los datos estén correctos y sin duplicados, incluso después de particionar la base de datos.
Particionamiento necesario: El particionamiento horizontal (sharding) es necesario para distribuir los datos a través de varios servidores, permitiendo que el sistema escale horizontalmente.

Definir la estrategia de particionamiento:
En MongoDB, puedes particionar la base de datos utilizando un campo de shard key. Esto puede ser un campo que distribuye bien los datos y las consultas entre los fragmentos.
Ejemplo de shard key: Si estamos manejando un evento deportivo, una buena opción podría ser evento_id, ya que los datos de diferentes eventos no se solapan y permiten distribuir los datos eficientemente.
Otra opción podría ser usar campos como fecha o jugador_id si las consultas más frecuentes están relacionadas con eventos específicos o jugadores.
