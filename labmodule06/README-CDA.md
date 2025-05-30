# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

La implementación se centra en la comunicación MQTT entre el dispositivo restringido (CDA) y el gateway (GDA). Se ha implementado un cliente MQTT que permite la publicación de datos de sensores y rendimiento del sistema, así como la suscripción a comandos de actuación. El sistema utiliza QoS 0 para mensajes de telemetría y QoS 1 para comandos de actuación, optimizando el rendimiento y la fiabilidad según el tipo de mensaje.


### Code Repository and Branch

URL: https://github.com/santipvz/python-components

Branch: labmodule06

### Unit Tests Executed

- MqttClientConnectorTest
- MqttClientPerformanceTest
- DataUtilTest
- ConfigUtilTest

### Integration Tests Executed

- MqttClientConnectorTest
- MqttClientPerformanceTest
- ConstrainedDeviceAppTest

EOF.
