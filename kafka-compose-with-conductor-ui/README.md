# Kafka, Zookeeper, Schema Registry, Conduktor Platform, and Kadeck Web with Docker Compose

This `docker-compose.yml` file sets up a development environment with Kafka, Zookeeper, Schema Registry, Conduktor Platform, and Kadeck Web using Docker Compose.

## Components

The `docker-compose.yml` file includes the following services:

1. **Zookeeper**: A distributed coordination service required by Kafka.
2. **Kafka**: A distributed streaming platform for building real-time data pipelines and streaming applications.
3. **Schema Registry**: A centralized repository for managing and sharing Avro schemas across multiple Kafka producers and consumers.
4. **Conduktor Platform**: A web-based platform to manage, monitor, and control Kafka clusters and Schema Registries.
   [Run Conduktor Platform locally.md](Run%20Conduktor%20Platform%20locally.md)
5. **Kadeck Web**: A web-based Kafka client for managing Kafka topics, partitions, and messages.

## Usage

1. Install Docker and Docker Compose.
2. Clone this repository or copy the `docker-compose.yml` file to your local machine.
3. In the same directory as the `docker-compose.yml` file, create a `jmx-exporter.yml` file with the desired JMX Exporter configuration.
4. Create a `${CONF_NAME:-platform-config}.yaml` file with the desired Conduktor Platform configuration.
5. Set the `LICENSE_KEY` environment variable with your Conduktor Platform license key.
6. Run `docker-compose up -d` to start all the services.

## Ports

The following ports are exposed and mapped to the host machine:

1. **Zookeeper**: 2181 (client port)
2. **Kafka**: 9092 (external listener), 9101 (JMX exporter)
3. **Schema Registry**: 8081 (listener port)
4. **Conduktor Platform**: 8080 (web interface)
5. **Kadeck Web**: 80 (web interface)

## Volumes

The `docker-compose.yml` file defines several named volumes for persisting data:

1. `zookeeper_data`: Stores Zookeeper's data files.
2. `zookeeper_datalog`: Stores Zookeeper's transaction logs.
3. `kafka_data`: Stores Kafka's log files.
4. `conduktor_data`: Stores Conduktor Platform's data files.

## Customization

You can customize the `docker-compose.yml` file by modifying environment variables and volume bindings for each service.

For example, you can change the Kafka broker ID, listeners, and security protocol map by modifying the `KAFKA_BROKER_ID`, `KAFKA_LISTENERS`, and `KAFKA_LISTENER_SECURITY_PROTOCOL_MAP` environment variables.

Additionally, you can modify the `jmx-exporter.yml` and `${CONF_NAME:-platform-config}.yaml` files to change the JMX Exporter and Conduktor Platform configurations, respectively.

## Troubleshooting

If you experience any issues while running the Docker Compose setup, you can use the following commands to debug:

1. `docker-compose logs`: View logs from all services.
2. `docker-compose logs <service_name>`: View logs from a specific service, e.g., `docker-compose logs kafka`.
3. `docker-compose ps`: Check
