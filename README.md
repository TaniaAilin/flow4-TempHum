# flow5-NodeRed-ClimaAPI
Este repositorio contiene el flow de NodeRed para obtener la informacion climatica por API desde openweathermap.org

# Introducción
En este flow podrá observarse un conjunto de gráficas en Dasboard, las cuales tienen como proposito reportar la información climática recibida manualmente por MQTT, la información recibida automáticamente por API y la información de varius usuarios compartida por MQTT en un broker publico

# Material Necesario
Para realizar este flow necesitas lo siguiente

Ubuntu 20.04
NodeJS
NPM
NodeRed
Nodos Dashboard
Mosquitto
Material de referencia
En los siguientes enlaces puedes encontrar cursos en la plataforma de edu.codigoiot.com que te permitirán realiar las configuraciones necesarias

Instalación de Virutal Box y Ubuntu 20.04
Instalación de NodeRed
Introducción a NodeRed
Introducción a Mosquitto
Servicios
Para que este ejercicio funcione, necesitas los siguientes servicios

HiveMQ. Es un broker publico y no se necesita cuenta
OpenWeatherMap. Servicio meteorológico gratuito. Se requiere cuenta, pero no se requiere ningun pago.
Instrucciones
Requisitos previos
Para que este flow funcione, debes cumplir con los siguientes requisitos previos

Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2
Instalar los nodos node-red-dashboard. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.
Instalación de Broker local Mosquitto MQTT.
Cuenta en OpenWeatherMap.org. Este es el servidor del cual se obtendrán los datos del clima por API
API Key valida. Deberás generar una API Key con tu cuenta de openweathermaps.org
Instrucciones de preparación del entorno
Para ejecutar este flow, es necesario lo siguiente:

Arrancar NodeRed con el comando node-red
Importar el flow del repositorio.
Coloca tu API Key personal en la API Call del nodo HTTP Request.
Actualiza la IP del broker público.
Hacer clic en el boton Deploy.
Instrucciones de operación
Para observar el resutlado de este flow, abre un navegador y dirígete a localhost:1880/ui.
Para activar las gráficas de clima manual, debes enviar por MQTT un mensaje que contenga un JSON con las variables ID, temp y hum.
  Notas
La sección manual de este flow se suscribe al tema codigoIoT/fow5/mqtt en un broker local.
El mensaje mqtt usado para probar este flow es mosquitto_pub -h localhost -t codigoIoT/Mor/mqtt/flow5 -m '{"ID":"Tania Ailin","temp":19,"hum":95}''
Para que la gráfica historica muestre información, deben enviarse al menos 2 puntos.
Para actualizar la IP del broker publico, se recomienda el siguiente comando nslookup broker.hivemq.com. Puedes usar el broker publico de tu elección.
Para que multiples graficas sean mostradas en la sección de Histórico Público, es necesario que multiples usuarios se encuentren publicando a la vez.
# Resultados
A continuación puedes ver los nodos del flow. 

A continuación puede ver el tablero resultante. 

# Evidencias
https://youtu.be/aDlTqSABwro
# Créditos
Desarrollado por Tania Ailin

https://www.facebook.com/tania.ailin.1
https://github.com/TaniaAilin/
