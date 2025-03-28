# 📌 Apache Kafka - Mensajería Asíncrona para Microservicios

Apache Kafka es un servicio de mensajería asíncrona diseñado para microservicios, proporcionando un bus de mensajes escalable, distribuido y altamente resiliente.

---

## 🚀 Implementación Básica de Apache Kafka

### 🛠️ 1. Crear el archivo `Dockerfile`
Para implementar los contenedores, primero es necesario crear el archivo `Dockerfile`.

### ▶️ 2. Levantar los contenedores
Ejecuta el siguiente comando para iniciar los contenedores:

```sh
 docker-compose up -d
```

### 📌 3. Crear un Topic
#### 🔹 3.1 Ingresar al contenedor de Kafka
Ejecuta el siguiente comando:

```sh
docker exec -it kafka bash
```

#### 🔹 3.2 Crear un topic
Dentro del contenedor, ejecuta:

```sh
kafka-topics --bootstrap-server kafka:9092 --create --topic primer-topic
```

### ✉️ 4. Enviar Mensajes con Producer
#### 🔹 4.1 Crear un mensaje
Ejecuta el siguiente comando para enviar un mensaje al topic:

```sh
kafka-console-producer --bootstrap-server kafka:9092 --topic primer-topic
```

### 📥 5. Consumir Mensajes con Consumer
#### 🔹 5.1 Leer mensajes desde el Consumer
Ejecuta el siguiente comando para recibir los mensajes desde el topic:

```sh
kafka-console-consumer --bootstrap-server kafka:9092 --topic primer-topic --from-beginning
```

---

