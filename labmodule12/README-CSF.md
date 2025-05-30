# Cloud Service Functions (Connected Devices)

## Lab Module 12 - Semester Project - CSF Components

Be sure to implement all the PIOT-CSF-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Nuestra implementación utiliza Ubidots como el componente Cloud Service Functions (CSF). Ubidots actúa como el punto centralizado para la ingesta y visualización de datos de telemetría enviados por el Gateway Device (GDA), así como para la gestión y envío de comandos de actuación hacia el GDA, que a su vez los reenvía al Constrained Device (CDA). Esto permite la monitorización remota de sensores y el rendimiento del sistema desde el CDA y el GDA, así como el control remoto de actuadores conectados al CDA a través de la plataforma Ubidots.

How does your implementation work?

La comunicación entre el GDA y el CSF (Ubidots) se realiza utilizando el protocolo MQTT a través del puerto seguro 8883 con TLS para asegurar la confidencialidad e integridad de los datos. El GDA publica los datos de telemetría (sensores ambientales y rendimiento del sistema del CDA, además del rendimiento del sistema del propio GDA) en los tópicos específicos de Ubidots (`/v1.6/devices/{clientID}`). Ubidots está configurado para procesar estos mensajes JSON y crear variables correspondientes en el dashboard del dispositivo. Además, el GDA se suscribe a tópicos de comandos de actuación en Ubidots para recibir instrucciones remotas, que luego procesa y reenvía al CDA también a través de MQTT/TLS.


#### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/santipvz/python-components
Branch: default

#### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- SystemTest


EOF.
