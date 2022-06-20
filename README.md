# Introducción

MQTT es un protocolo de mensajería reconocido en IoT. Utiliza un modelo de comunicación de publisher/subscriber
y permite distribuir datos de telemetría con un consumo de recursos de red muy bajo.
[test.mosquitto.org](http://test.mosquitto.org/) aloja un broker de MQTT disponible públicamente que utilizaremos para esta prueba.
Los eventos en MQTT se organizan por medio de tópicos. Los tópicos siguen una estructura jerárquica como la de un filesystem.

Apache Kafka es una plataforma distribuida de "Event Streaming", utilizada para diversos fines como Streaming Analytics, data integration, etc.
Utilizaremos Apache Kafka para recibir los eventos originados en MQTT. Una vez que los eventos arriben a Kafka,
será posible derivar diferentes casos de usos.

Apache Nifi es una herramienta para automatizar el flujo de datos entre sistemas. La utilizaremos para distribuir los eventos de MQTT
hacia Kafka, realizando unas transformaciones de por medio.

# Pre-requisitos

- Docker
- Docker Compose

# Entorno

1. Clonar el repositorio
`git clone https://github.com/guidofranco/nifi_mqtt_to_kafka.git`
2. Ir al directorio del proyecto
`cd nifi_mqtt_to_kafa`
3. Iniciar el entorno
`docker-compose up`
4. Abrir la Web UI de Nifi: `https://localhost:8443/nifi/`.

Las credenciales para iniciar sesión se encuentran en el archivo `docker-compose.yml`
6. Subir el template (archivo `.xml`)
