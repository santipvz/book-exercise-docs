# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

Se ha desarrollado un módulo denominado SystemPerformanceManager, responsable de la programación y ejecución periódica de tareas que recogen métricas esenciales como la utilización de la CPU y de la memoria.

La clase base BaseSystemUtilTask provee la funcionalidad común necesaria para que las tareas especializadas, SystemCpuUtilTask y SystemMemUtilTask, puedan heredar y extender su comportamiento.

### Code Repository and Branch

URL: https://github.com/santipvz/python-components/tree/labmodule02

Branch: labmodule02

### Unit Tests Executed

- ConfigUtilTest

- SystemCpuUtilTaskTest

- SystemMemUtilTaskTest

### Integration Tests Executed

- ConstrainedDeviceAppTest

- SystemPerformanceManagerTest

EOF.
