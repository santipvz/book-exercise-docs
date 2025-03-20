# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues.

### Description

Se ha creado un módulo denominado SystemPerformanceManager, encargado de programar y ejecutar tareas periódicas para recolectar métricas esenciales como la utilización de la CPU y de la memoria.

La clase base BaseSystemUtilTask proporciona la funcionalidad común para todas las tareas de monitorización, mientras que las clases especializadas SystemCpuUtilTask y SystemMemUtilTask se encargan de recoger, respectivamente, las métricas de CPU y memoria.

### Code Repository and Branch

URL: https://github.com/santipvz/java-components

Branch: Branch: (Pongo la default porque se me olvidó crear una branch especifica para esto.)


### Unit Tests Executed

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest


### Integration Tests Executed

- GatewayDeviceAppTest
- SystemPerformanceManagerTest


EOF.
