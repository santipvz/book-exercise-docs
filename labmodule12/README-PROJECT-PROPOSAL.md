# Lab Module 12 - Semester Project Proposal

## Description

Describe your idea in 1 paragraph (at least 2 or 3 sentences).

Este proyecto propone el desarrollo de un sistema IoT que integre un dispositivo restringido (CDA), un Gateway Device (GDA) y un servicio en la nube (CSF) para la monitorización de condiciones ambientales y el rendimiento del sistema, así como el control remoto de actuadores. El objetivo es establecer una comunicación segura y fiable entre los componentes utilizando protocolos estándar de IoT, permitiendo la recolección de datos en tiempo real y la ejecución de acciones remotas.

## What - The Problem 

What problem are you trying to solve and why does it matter? Write 1 to 2 paragraphs in response.

El proyecto aborda el desafío de construir una solución de IoT de extremo a extremo que sea capaz de recopilar datos de entornos con recursos limitados (CDA), agregarlos y procesarlos en un punto intermedio (GDA), y enviarlos a una plataforma en la nube para análisis, visualización y control remoto. La relevancia de este problema radica en la creciente necesidad de sistemas que permitan la toma de decisiones basada en datos en tiempo real y la automatización de procesos en diversos dominios, desde la agricultura inteligente hasta la monitorización de infraestructuras críticas.

La implementación de una arquitectura distribuida con componentes en el borde (edge) y en la nube es fundamental para procesar grandes volúmenes de datos, reducir la latencia en las respuestas y operar en entornos con conectividad intermitente. Este proyecto busca sentar las bases para este tipo de soluciones.

## Why - Who Cares? 

Why do you care about this particular problem? Write 1 to 2 paragraphs in response.

La posibilidad de conectar dispositivos físicos al mundo digital y obtener información valiosa de ellos es un campo fascinante con un potencial transformador. Me interesa este problema porque la implementación de sistemas IoT eficientes y seguros es clave para unlocking nuevas capacidades en una amplia gama de aplicaciones, desde la mejora de la eficiencia energética en hogares y ciudades inteligentes hasta la optimización de la producción industrial y la habilitación de la telemedicina. Contribuir al desarrollo de las habilidades necesarias para construir estos sistemas es relevante para mi crecimiento profesional y me permite participar en la configuración del futuro digital.

## How - Expected Technical Approach

How do you plan to tackle this problem technically?

Include a high-level design diagram depicting your planned technical approach - it does not need to be final, but it must include the CDA, GDA, and cloud services you plan to use, as well as the protocol(s) you will use for communicating between the devices and the cloud.

[Insertar diagrama de alto nivel aquí - Describir verbalmente o insertar una imagen]

El enfoque técnico se basa en una arquitectura de tres capas: Dispositivo Restringido (CDA), Gateway Device (GDA) y Cloud Service Functions (CSF - Ubidots). El CDA, implementado en Python, recolectará datos de sensores simulados (temperatura, humedad, presión) y rendimiento del sistema, y se comunicará con el GDA usando MQTT/TLS. El GDA, también en Python, actuará como agregador, procesando los datos del CDA, recolectando su propio rendimiento del sistema y publicando toda la telemetría en Ubidots a través de MQTT/TLS. Ubidots se utilizará para la visualización de datos y el envío de comandos de actuación al GDA, que los reenviará al CDA para controlar un actuador simulado. La seguridad se garantizará mediante el uso de TLS en todas las comunicaciones MQTT.

Write 1 to 2 paragraphs describing your diagram.

[Descripción del diagrama, similar a la de README-PROJECT-FINAL.md, pero enfocada en la propuesta inicial]

El diagrama propuesto ilustra la interconexión de los tres componentes principales. El CDA, en el nivel más bajo, interactúa con sensores y actuadores locales. Se conecta al GDA mediante un enlace seguro MQTT/TLS. El GDA, en el nivel intermedio, recibe datos del CDA, procesa su propia información de rendimiento y mantiene una conexión segura MQTT/TLS con la plataforma en la nube (Ubidots). La flechas indican el flujo de datos de telemetría desde el CDA hacia el GDA y luego hacia la nube, y el flujo de comandos de actuación desde la nube hacia el GDA y finalmente hacia el CDA. Esta arquitectura modular permite escalar la solución y gestionar los recursos de manera eficiente.

## Results - Expected Outcomes 

If your project is successful, what outcome do you expect (e.g. what will happen if everything works)? Write 1 to 2 paragraphs describing your expected outcomes.

Se espera que, al finalizar el proyecto, el sistema sea capaz de operar de forma autónoma, recolectando datos de telemetría del CDA y GDA, enviándolos a Ubidots para su visualización en tiempo real, y respondiendo a comandos de actuación iniciados desde la plataforma en la nube. Se anticipa que los datos de sensores ambientales y rendimiento del sistema se mostrarán correctamente en el dashboard de Ubidots, y que será posible controlar un actuador en el CDA de forma remota a través de la interfaz de Ubidots. Además, se espera que la comunicación entre todos los componentes sea segura gracias a la implementación de TLS.

Se medirá el éxito por la estabilidad de la conexión, la correcta transmisión y visualización de todos los datos de telemetría esperados (incluyendo CPU, memoria y disco), la capacidad de activar y desactivar el actuador remoto, y la ausencia de errores críticos durante periodos prolongados de ejecución. Aunque se espera que la implementación satisfaga los requisitos principales, se reconocen los posibles desafíos técnicos y se abordarán durante el proceso de desarrollo.


EOF.
