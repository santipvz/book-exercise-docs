# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

Se utiliza un generador que simula lecturas de temperatura, humedad y presión, empaquetándolas en objetos de telemetría para analizar el comportamiento del dispositivo. Además, se implementó un disparador que, al superar ciertos umbrales, registra un comando de actuador simulado.

### Code Repository and Branch

URL: https://github.com/santipvz/python-components/tree/labmodule03

Branch: labmodule03

### Unit Tests Executed

- ActuatorDataTest

- SensorDataTest

- SystemPerformanceDataTest

- HumiditySensorSimTaskTest

- PressureSensorSimTaskTest

- TemperatureSensorSimTaskTest

- HumidifierActuatorSimTaskTest

- HvacActuatorSimTaskTest

### Integration Tests Executed

- SensorAdapterManagerTest

- ActuatorAdapterManagerTest

- ConstrainedDeviceAppTest

EOF.
