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

  




