# Indoor and Outdoor Weather Monitoring using STM32 and Node-RED

## Project Overview
This project monitors indoor environmental conditions using a BME280 sensor connected to an STM32 NUCLEO-F401RE board and compares them with external weather data obtained through an API. Node-RED processes both sets of data and provides recommendations on whether the window should be kept open or closed, along with two additional suggestions based on humidity levels.

## Components Used
- STM32 NUCLEO-F401RE
- BME280 Temperature, Pressure and Humidity Sensor
- ESP8266 Wi-Fi Module
- Computer running Node-RED

## Software and Technologies
- Embedded C
- STM32CubeMX / Keil MDK
- MQTT Protocol
- Node-RED Dashboard
- OpenWeather API
- JavaScript (Function Nodes)

## Working Flow
1. BME280 measures indoor temperature, pressure and humidity.
2. STM32 reads sensor data through I2C.
3. ESP8266 connects to Wi-Fi and publishes sensor readings to an MQTT broker.
4. Node-RED receives indoor sensor data through an MQTT input node.
5. An HTTP request retrieves external weather information using the OpenWeather API.
6. Function nodes compare indoor sensor readings with outside weather conditions.
7. Based on the comparison, the system recommends whether to keep the window open or closed and provides two additional humidity-based suggestions.
8. Results are displayed on the Node-RED dashboard.

## MQTT Configuration
- Broker: `broker.emqx.io`
- Port: `1883`
- Topic: `stm32/diya`
- QoS: `0`

## Node-RED Dashboard
The dashboard displays:
- Indoor temperature gauge
- Indoor humidity gauge
- External weather information
- Location and weather description
- Window open/close recommendation
- Two additional humidity-based suggestions

## Expected Output
The system compares indoor sensor readings with external weather conditions and provides recommendations to help maintain suitable indoor environmental conditions through window ventilation and humidity management.

## Conclusion
This project integrates embedded systems, IoT communication, external weather APIs and Node-RED visualization to develop a smart indoor environmental monitoring and recommendation system.