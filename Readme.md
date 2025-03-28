# APACHE KAFKA

Apache Kafka es un servicio de mensajeria asincrono para microservicios que proporciona un bus de mensajes escalable, distribuido y altamente resiliente.

### Implementacion basica de apache kafka 

1- Crear el archivo dockerfile para poder implementar los contenedores.

2- Luego ejecutar el siguiente comando para levantar los contenedores.

 docker-compose up -d

3- Crear topic

3.1 Ingresamos al contenedor con el siguiente comando.

 docker exec -it kafka bash 

3.2 Creamos el topic.

kafka-topics --bootstrap-server kafka:9092 --create --topic primer-topic

4- Producer 

4.1 Creamos el primer mensaje con el siguiente comando.

kafka-console-producer --bootstrap-server kafka:9092 --topic primer-topic

5- Consumer

5.1 Consumimos el mensaje desde el consumer.

kafka-console-consumer --bootstrap-server kafka:9092 --topic primer-topic --from-beginning

