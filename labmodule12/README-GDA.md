# GDA - Gateway Device Application

## Overview
La aplicación Gateway Device (GDA) ha sido implementada como un componente central que actúa como intermediario entre los dispositivos restringidos (CDA) y los servicios en la nube. La implementación incluye todas las funcionalidades requeridas para la gestión de datos, comunicación y procesamiento de eventos.

## Requirements
- Java 11 o superior
- Maven 3.6 o superior
- Conexión a Internet para servicios en la nube
- Puerto 56830 disponible para CoAP
- Puerto 1883 disponible para MQTT

## Design
La arquitectura del GDA se ha implementado siguiendo un diseño modular y extensible:

1. **Conexiones**:
   - CoAP Server: Implementado en `CoapServerGateway.java` para comunicación con CDA
   - MQTT Client: Implementado en `MqttClientConnector.java` para comunicación con la nube
   - Configuración de puertos y seguridad en `PiotConfig.props`

2. **Gestión de Datos**:
   - `DeviceDataManager`: Centraliza el procesamiento de datos
   - `SystemPerformanceManager`: Monitorea el rendimiento del sistema
   - `DataUtil`: Utilidades para el manejo de datos

3. **Procesamiento de Eventos**:
   - Análisis de datos de sensores
   - Generación de eventos de actuación
   - Manejo de comandos de la nube

## Implementation
La implementación incluye:

1. **Conexiones Seguras**:
   - CoAP: Puerto 56830 con autenticación y encriptación deshabilitadas para pruebas
   - MQTT: Conexión segura al broker local en puerto 1883

2. **Procesamiento de Datos**:
   - Almacenamiento local de datos de sensores
   - Monitoreo de rendimiento del sistema
   - Análisis de datos para generación de eventos

3. **Integración con Servicios**:
   - Conexión con Ubidots para almacenamiento en la nube
   - Manejo de eventos y comandos de la nube
   - Gestión de respuestas de actuadores

## Testing
Se han implementado pruebas integrales en `GatewayDeviceAppTest.java` que verifican:

1. **Conexiones**:
   - Inicialización correcta del servidor CoAP
   - Conexión exitosa al broker MQTT
   - Manejo de recursos CoAP

2. **Procesamiento de Datos**:
   - Recepción y procesamiento de datos de sensores
   - Manejo de comandos de actuadores
   - Almacenamiento local de datos

3. **Eventos**:
   - Generación de eventos basados en datos
   - Manejo de comandos de la nube
   - Respuestas a actuadores

## Configuration
La configuración se maneja a través de `PiotConfig.props`:

1. **CoAP**:
   - Puerto: 56830
   - Autenticación: Deshabilitada
   - Encriptación: Deshabilitada

2. **MQTT**:
   - Broker: localhost:1883
   - Credenciales: Cargadas desde `UbidotsCloudCred.props`

3. **Almacenamiento**:
   - Persistencia local habilitada
   - Envío a la nube configurado

## Usage
Para ejecutar el GDA:

1. **Compilación**:
   ```bash
   mvn clean install
   ```

2. **Ejecución**:
   ```bash
   mvn exec:java -Dexec.mainClass="programmingtheiot.gda.app.GatewayDeviceApp"
   ```

3. **Pruebas**:
   ```bash
   mvn test -Dtest=GatewayDeviceAppTest
   ```

## Notes
- El GDA está diseñado para ser escalable y mantener un alto rendimiento
- La implementación actual está optimizada para pruebas y desarrollo
- Se recomienda habilitar la seguridad en producción

EOF.
