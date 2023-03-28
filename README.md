![60062294.png](assets/conductorlogo.png?t=1680038974486)

# sources https://docs.conduktor.io/platform/installation/get-started/docker-compose/

## docker-compose-lib

Use Docker Compose to start:

* Single node Kafka cluster
* Schema Registry
* The latest version of Conduktor Platform

* [X]  [kafka-compose-with-conductor-ui](kafka-compose-with-conductor-ui)

If you do not want to use the auto-run script, you can find more information about starting the platform locally via Docker Compose in the example repository:

[https://github.com/conduktor/conduktor-platform/tree/main/example-local](https://github.com/conduktor/conduktor-platform/tree/main/example-local)

## Access Conduktor[](https://docs.conduktor.io/platform/installation/get-started/docker-compose/#access-conduktor "Direct link to Access Conduktor")

After a few minutes, **Conduktor will be available at [http://localhost:8080](http://localhost:8080/)**

## Customizing the Docker Compose[](https://docs.conduktor.io/platform/installation/get-started/docker-compose/#customizing-the-docker-compose "Direct link to Customizing the Docker Compose")

Conduktor depends on a configuration file `platform-config.yaml`. This is used to setup your oganizations environment. The file is used to declare:

* Organization name
* External database (optional)
* User authentication (Basic or SSO)

In the above example, a default `platform-config.yaml` is used to start the platform. However, if you would like to see more examples for connecting to your own infrastructure, see the [Configuration Page](https://docs.conduktor.io/platform/configuration/introduction/).
