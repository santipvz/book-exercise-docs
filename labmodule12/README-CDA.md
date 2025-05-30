# Constrained Device Application (Connected Devices)

## Lab Module 12 - Semester Project - CDA Components

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

La implementación del CDA (Constrained Device Application) proporciona una solución completa para la gestión de dispositivos IoT, incluyendo la recolección de datos de sensores, monitoreo del rendimiento del sistema, y control de actuadores. El sistema está diseñado para funcionar de manera autónoma, procesando datos en tiempo real y tomando decisiones basadas en umbrales predefinidos.

La implementación funciona mediante un sistema de gestión de eventos basado en intervalos de tiempo, donde el SensorAdapterManager y SystemPerformanceManager operan en paralelo cada 5 segundos. El sistema monitorea la temperatura y otros parámetros del sistema, activando actuadores cuando se cruzan umbrales predefinidos (por ejemplo, cuando la temperatura supera los 25°C). La comunicación con el GDA se realiza de forma segura utilizando MQTT con TLS, asegurando la integridad y confidencialidad de los datos transmitidos.

### Code Repository and Branch

URL: https://github.com/santipvz/python-components
Branch: labmodule12

### Unit Tests Executed



### Integration Tests Executed

- SystemTest
- ThresholdActuationTest

EOF.
