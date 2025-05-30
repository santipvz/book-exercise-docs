# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

La implementación del GDA (Gateway Device Application) proporciona una aplicación servidor MQTT que actúa como puente entre los dispositivos restringidos y el sistema IoT. Esta implementación incluye funcionalidades para gestionar conexiones MQTT, suscribirse a múltiples tópicos relevantes (ActuatorResponse, SensorMsg, SystemPerfMsg) y manejar la comunicación bidireccional con los dispositivos restringidos. El servidor está diseñado para ser robusto y escalable, capaz de manejar múltiples conexiones simultáneas y diferentes niveles de QoS.

How does your implementation work?

La implementación funciona utilizando la biblioteca Paho MQTT para Java, que proporciona una interfaz robusta para la comunicación MQTT. El servidor se configura con parámetros específicos como la URL del broker, el manejo de credenciales (aunque en este caso no se utilizan), y la gestión de suscripciones a tópicos. La implementación maneja la conexión y desconexión del broker de manera segura, y proporciona métodos para suscribirse a tópicos específicos y procesar mensajes entrantes. Las pruebas de rendimiento muestran que el servidor puede manejar eficientemente grandes volúmenes de mensajes, con tiempos de respuesta que varían según el nivel de QoS utilizado.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/santipvz/java-components

Branch: labmodule10

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- MqttClientConnectorTest
- MqttClientPerformanceTest
- ConfigUtilTest
- DataUtilTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- MqttClientConnectorTest
- MqttClientPerformanceTest
- DeviceDataManagerTest
- SensorSimAdapterManagerTest


## GDA MQTT Client Performance Test Results

may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
INFORMACIÓN: Checking if credentials file exists and is loadable...
may 30, 2025 12:56:59 A.M. programmingtheiot.common.ConfigUtil getCredentials
ADVERTENCIA: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
ADVERTENCIA: No credentials are set.
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFORMACIÓN: Using URL for broker conn: tcp://localhost:1883
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
may 30, 2025 12:56:59 A.M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: \n\tTesting Publish: QoS = 0 | msgs = 10000 | payload size = 212 | start = 1.7485595E9 | end = 1.7485595E9 | elapsed = 0.274
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
INFORMACIÓN: Checking if credentials file exists and is loadable...
may 30, 2025 12:56:59 A.M. programmingtheiot.common.ConfigUtil getCredentials
ADVERTENCIA: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
ADVERTENCIA: No credentials are set.
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFORMACIÓN: Using URL for broker conn: tcp://localhost:1883
may 30, 2025 12:56:59 A.M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: \n\tTesting Publish: QoS = 1 | msgs = 10000 | payload size = 212 | start = 1.7485595E9 | end = 1.7485595E9 | elapsed = 0.434
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
INFORMACIÓN: Checking if credentials file exists and is loadable...
may 30, 2025 12:57:00 A.M. programmingtheiot.common.ConfigUtil getCredentials
ADVERTENCIA: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
ADVERTENCIA: No credentials are set.
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFORMACIÓN: Using URL for broker conn: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:57:00 A.M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
may 30, 2025 12:57:00 A.M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest execTestPublish
INFORMACIÓN: \n\tTesting Publish: QoS = 2 | msgs = 10000 | payload size = 212 | start = 1.7485595E9 | end = 1.7485595E9 | elapsed = 0.735
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
INFORMACIÓN: Checking if credentials file exists and is loadable...
may 30, 2025 12:57:01 A.M. programmingtheiot.common.ConfigUtil getCredentials
ADVERTENCIA: Credential file non-existent: ./cred/PiotMqttCred.props. Ignoring.
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector initCredentialConnectionParameters
ADVERTENCIA: No credentials are set.
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector initClientParameters
INFORMACIÓN: Using URL for broker conn: tcp://localhost:1883
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector connectClient
INFORMACIÓN: MQTT client connecting to broker: tcp://localhost:1883
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: MQTT connection successful (is reconnect = false). Broker: tcp://localhost:1883
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/ActuatorResponse
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SensorMsg
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector connectComplete
INFORMACIÓN: Subscribing to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:57:01 A.M. programmingtheiot.gda.connection.MqttClientConnector subscribeToTopic
INFORMACIÓN: Successfully subscribed to topic: PIOT/ConstrainedDevice/SystemPerfMsg
may 30, 2025 12:57:02 A.M. programmingtheiot.gda.connection.MqttClientConnector disconnectClient
INFORMACIÓN: Disconnecting MQTT client from broker: tcp://localhost:1883
may 30, 2025 12:57:02 A.M. programmingtheiot.part03.integration.connection.MqttClientPerformanceTest testConnectAndDisconnect
INFORMACIÓN: Connect and Disconnect [1]: 1302 ms


EOF.
