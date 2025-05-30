# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

La implementación del Gateway Device Application (GDA) proporciona una capa de abstracción para la gestión de dispositivos IoT conectados. El GDA actúa como un intermediario entre los dispositivos físicos y los servicios en la nube, permitiendo la comunicación bidireccional y el procesamiento de datos. Implementa un sistema robusto de manejo de eventos y estados que permite la gestión eficiente de múltiples dispositivos simultáneamente, con capacidades de monitoreo en tiempo real y gestión de configuración.

How does your implementation work?

La implementación funciona a través de un sistema modular que utiliza patrones de diseño como Observer y Factory para mantener un acoplamiento bajo entre componentes. El sistema se compone de varios módulos principales: un gestor de dispositivos que maneja la conexión y desconexión de dispositivos, un procesador de datos que normaliza y valida la información recibida, y un sistema de eventos que notifica cambios de estado y actualizaciones. La comunicación con la nube se realiza a través de un cliente MQTT que mantiene una conexión persistente y maneja la reconexión automática en caso de fallos.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/santipvz/java-components
Branch: labmodule11

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- DeviceDataManagerTest
- DeviceConnectionManagerTest
- MqttClientConnectorTest
- SystemPerformanceManagerTest
- ConfigUtilTest
- DataUtilTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- DeviceDataManagerIntegrationTest
- MqttClientConnectorIntegrationTest
- SystemPerformanceManagerIntegrationTest
- CloudClientConnectorIntegrationTest

EOF.
