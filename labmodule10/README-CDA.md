# Constrained Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

La implementación del CDA (Constrained Device Application) proporciona una aplicación cliente MQTT que permite la comunicación con el broker MQTT. Esta implementación incluye funcionalidades para conectarse y desconectarse del broker, así como para publicar mensajes con diferentes niveles de QoS (Quality of Service). El cliente está diseñado para ser eficiente y manejar grandes volúmenes de mensajes, como se demuestra en las pruebas de rendimiento realizadas.

How does your implementation work?

La implementación funciona utilizando la biblioteca Paho MQTT para Python, que proporciona una interfaz robusta para la comunicación MQTT. El cliente se configura con parámetros específicos como el ID del cliente, el host del broker, el puerto y el tiempo de keep-alive. La implementación maneja la conexión y desconexión del broker de manera segura, y proporciona métodos para publicar mensajes con diferentes niveles de QoS (0, 1 y 2). Las pruebas de rendimiento muestran que el cliente puede manejar eficientemente grandes volúmenes de mensajes, con tiempos de respuesta que varían según el nivel de QoS utilizado.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/santipvz/python-components

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

## CDA MQTT Client Performance Test Results
2025-05-26 21:22:36,277:ConfigUtil:INFO:Loading config: /home/santi/Escritorio/PIC/python-components/config/PiotConfig.props
2025-05-26 21:22:36,277:ConfigUtil:DEBUG:Config: ['Mqtt.GatewayService', 'Coap.GatewayService', 'ConstrainedDevice']
2025-05-26 21:22:36,277:ConfigUtil:INFO:Created instance of ConfigUtil: <programmingtheiot.common.ConfigUtil.ConfigUtil object at 0x7a7eab7448c0>
2025-05-26 21:22:36,277:MqttClientConnector:INFO:       MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-05-26 21:22:36,277:MqttClientConnector:INFO:       MQTT Broker Host: localhost
2025-05-26 21:22:36,277:MqttClientConnector:INFO:       MQTT Broker Port: 1883
2025-05-26 21:22:36,277:MqttClientConnector:INFO:       MQTT Keep Alive:  60
2025-05-26 21:22:36,277:MqttClientConnector:INFO:MQTT client connecting to broker at host: localhost
2025-05-26 21:22:36,278:MqttClientConnector:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x7a7eac492570>
2025-05-26 21:22:36,278:MqttClientConnector:INFO:Disconnecting MQTT client from broker: localhost
2025-05-26 21:22:37,279:MqttClientConnector:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x7a7eac492570>
2025-05-26 21:22:37,280:MqttClientPerformanceTest:INFO:Connect and Disconnect: 1002.570106 ms
.2025-05-26 21:22:37,280:MqttClientConnector:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-05-26 21:22:37,280:MqttClientConnector:INFO:       MQTT Broker Host: localhost
2025-05-26 21:22:37,280:MqttClientConnector:INFO:       MQTT Broker Port: 1883
2025-05-26 21:22:37,280:MqttClientConnector:INFO:       MQTT Keep Alive:  60
2025-05-26 21:22:37,280:MqttClientConnector:INFO:MQTT client connecting to broker at host: localhost
2025-05-26 21:22:37,280:MqttClientConnector:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x7a7eac490920>
2025-05-26 21:22:37,280:DataUtil:INFO:Created DataUtil instance.
2025-05-26 21:22:37,623:MqttClientConnector:INFO:Disconnecting MQTT client from broker: localhost
2025-05-26 21:22:38,624:MqttClientConnector:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x7a7eac490920>
2025-05-26 21:22:38,624:MqttClientPerformanceTest:INFO:
        Testing Publish: QoS = 0 | msgs = 10000 | payload size = 264 | start = 1748287357281012.5 | end = 1748287357623213.2 | elapsed = 0.342200646
2025-05-26 21:22:38,624:MqttClientPerformanceTest:INFO:Publish message - QoS 0 [10000]: 342.200646 ms
.2025-05-26 21:22:38,624:MqttClientConnector:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-05-26 21:22:38,624:MqttClientConnector:INFO:       MQTT Broker Host: localhost
2025-05-26 21:22:38,624:MqttClientConnector:INFO:       MQTT Broker Port: 1883
2025-05-26 21:22:38,624:MqttClientConnector:INFO:       MQTT Keep Alive:  60
2025-05-26 21:22:38,624:MqttClientConnector:INFO:MQTT client connecting to broker at host: localhost
2025-05-26 21:22:38,624:DataUtil:INFO:Created DataUtil instance.
2025-05-26 21:22:38,625:MqttClientConnector:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x7a7eac16d2b0>
2025-05-26 21:22:39,347:MqttClientConnector:INFO:Disconnecting MQTT client from broker: localhost
2025-05-26 21:22:40,348:MqttClientConnector:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x7a7eac16d2b0>
2025-05-26 21:22:40,348:MqttClientPerformanceTest:INFO:
        Testing Publish: QoS = 1 | msgs = 10000 | payload size = 264 | start = 1748287358625038.2 | end = 1748287359347544.8 | elapsed = 0.722506396
2025-05-26 21:22:40,348:MqttClientPerformanceTest:INFO:Publish message - QoS 1 [10000]: 722.506396 ms
.2025-05-26 21:22:40,348:MqttClientConnector:INFO:      MQTT Client ID:   CDAMqttClientPerformanceTest001
2025-05-26 21:22:40,348:MqttClientConnector:INFO:       MQTT Broker Host: localhost
2025-05-26 21:22:40,348:MqttClientConnector:INFO:       MQTT Broker Port: 1883
2025-05-26 21:22:40,348:MqttClientConnector:INFO:       MQTT Keep Alive:  60
2025-05-26 21:22:40,348:MqttClientConnector:INFO:MQTT client connecting to broker at host: localhost
2025-05-26 21:22:40,349:DataUtil:INFO:Created DataUtil instance.
2025-05-26 21:22:40,349:MqttClientConnector:INFO:MQTT client connected to broker: <paho.mqtt.client.Client object at 0x7a7eab7471a0>
2025-05-26 21:22:41,591:MqttClientConnector:INFO:Disconnecting MQTT client from broker: localhost
2025-05-26 21:22:42,592:MqttClientConnector:INFO:MQTT client disconnected from broker: <paho.mqtt.client.Client object at 0x7a7eab7471a0>
2025-05-26 21:22:42,592:MqttClientPerformanceTest:INFO:
        Testing Publish: QoS = 2 | msgs = 10000 | payload size = 264 | start = 1748287360349182.2 | end = 1748287361591382.0 | elapsed = 1.2421999579999998
2025-05-26 21:22:42,592:MqttClientPerformanceTest:INFO:Publish message - QoS 2 [10000]: 1242.199958 ms
.
----------------------------------------------------------------------
Ran 4 tests in 6.316s

OK

EOF.
