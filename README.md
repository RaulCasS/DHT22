#  SENSOR DHT22

## INSTRUCCIONES

### REQUISITOS PREVIOS
Para poder usar este repositorio necesitas entrar a la plataforma [WOKWI](https://wokwi.com/)

### INSTRUCCIONES DE PREPARACION DE ENTORNO
1. Abrir la terminal de programación y colocar la siguiente programación:
   
```
#include "DHTesp.h"


const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(10);  
  ```

2. Instalar la libreria de **DHT sensor library for ESPx**
![](https://github.com/RaulCasS/DHT22/blob/main/Captura%20de%20pantalla%202024-12-11%20230225.png?raw=true)

3. Agregar y hacer la conexión de **DHT22** con la **ESP32** como se muestra en la siguiente imagen:





