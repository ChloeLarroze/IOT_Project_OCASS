# IoT Project: Air Quality Monitoring and Ventilation Control in Confined Metro Stations

## Overview

This project aims to develop a Proof of Concept (PoC) for an IoT system designed to monitor and analyze environmental parameters in real-time within confined metro stations. The system integrates various sensors to measure indicators such as fine particles, CO₂ levels, humidity, and temperature. Data is transmitted via LoRa (Long Range) wireless communication, enabling long-range, low-energy data transmission. The system also includes an intelligent ventilation control mechanism to improve air quality based on the collected data.

## Objectives

- **Sensor Integration:** Select, calibrate, and ensure accurate measurement of environmental parameters.
- **Wireless Communication (LoRa):** Configure data transmission in underground environments.
- **Ventilation:** Adapt air renewal based on measured pollution levels.
- **Data Utilization:** Visualize and adjust the system in real-time using Datacake.

## System Components

The IoT system consists of several interconnected components:

- **Sensor Block:** Includes environmental sensors (fine particles, CO₂, humidity, temperature).
- **Microcontroller Block:** Manages data acquisition and communication with other modules.
- **Wireless Transmission Block:** Ensures LoRa communication for data transmission to a gateway.
- **Server/Cloud Block:** Stores and visualizes collected data via the Datacake platform.
- **Ventilation Block:** Controls a fan to improve air circulation based on air quality data.

## Key Features

### Real-Time Air Quality Monitoring

The system continuously monitors air quality parameters, allowing for the detection of pollution spikes and timely intervention. This is crucial in dynamic environments like metro stations, where air quality can fluctuate significantly throughout the day.

### Intelligent Ventilation Control

The system includes a fan that can be controlled automatically or manually based on air quality data. When the Air Quality Index (AQI) exceeds a predefined threshold, the fan activates and adjusts its speed proportionally to the pollution level.

### LoRa Communication

LoRa technology is used for long-range, low-power data transmission, making it ideal for underground environments. The system communicates with a LoRa gateway, which relays data to the Datacake platform for visualization and control.

### Datacake Interface

The Datacake platform provides a user-friendly interface for real-time data visualization and remote control of the system. Operators can monitor air quality parameters and adjust fan settings remotely.

## System Design

### Hardware

- **Microcontroller:** STM32-based OCASS platform.
- **Sensors:** Bosch BME680 for air quality, temperature, humidity, and pressure.
- **LoRa Module:** RFM95W-868S2 for wireless communication.
- **Fan:** 12V turbine fan controlled via PWM.

### Software

- **LoRaWAN Communication:** Utilizes the Cayenne Low Power Payload (LPP) format for data transmission.
- **Datacake Integration:** Data is visualized and controlled via the Datacake platform.
- **Automatic Fan Control:** The fan speed is adjusted based on AQI levels, with options for manual override.

## Testing and Results

### Prototype

A prototype was developed to simulate a confined metro station environment. The system was tested by injecting CO₂ into the enclosed space and monitoring the air quality. The fan was activated when the AQI exceeded the threshold, demonstrating the system's ability to improve air quality.

### Results

- **Data Accuracy:** The system provided consistent and accurate air quality measurements.
- **Fan Control:** The fan successfully activated and adjusted its speed based on AQI levels.
- **Remote Control:** Operators were able to control the fan and adjust settings remotely via Datacake.

## Limitations and Future Improvements

### Energy Consumption

The current system does not optimize for energy efficiency. Future iterations could implement low-power modes and reduce data transmission frequency to conserve energy.

### LoRa Network Quality

While LoRa is suitable for long-range communication, network stability can be affected by environmental factors. Improvements could include dynamic adjustment of the Spreading Factor (SF) and automatic reconnection mechanisms.

### Enhanced Ventilation Control

Future enhancements could integrate additional parameters, such as passenger density, to optimize fan operation. Integration with mobility apps like BonjourRATP could also provide real-time alerts to passengers about air quality.

## Conclusion

This project demonstrates the potential of IoT technology to address real-world environmental challenges, such as air quality in confined metro stations. The system successfully integrates sensor data, wireless communication, and intelligent ventilation control to improve air quality. While the prototype is a proof of concept, it lays the groundwork for future developments and large-scale deployment.

## References

- OpenData RATP, "Explore RATP data". Available: [https://data.ratp.fr/explore/?sort=modified](https://data.ratp.fr/explore/?sort=modified)
- France Télévisions, "Enquête France TV : Pollution dans le métro parisien". Available: [https://www.francetvinfo.fr/monde/environnement/crise-climatique/pollution-air/enquete-france-tv-pollution-dans-le-metro-parisien-decouvrez-les-mesures-inedites-de-la-qualite-de-l-air-dans-votre-station_5815343.html](https://www.francetvinfo.fr/monde/environnement/crise-climatique/pollution-air/enquete-france-tv-pollution-dans-le-metro-parisien-decouvrez-les-mesures-inedites-de-la-qualite-de-l-air-dans-votre-station_5815343.html)
- Airparif, "Stations de métro et de RER". Available: [https://www.airparif.fr/stations-de-metro-et-de-rer](https://www.airparif.fr/stations-de-metro-et-de-rer)
- Île-de-France Mobilités, "Qualité de l'air dans le réseau de transport francilien". Available: [https://data.iledefrance-mobilites.fr/explore/dataset/qualite-de-lair-dans-le-reseau-de-transport-francilien/information/](https://data.iledefrance-mobilites.fr/explore/dataset/qualite-de-lair-dans-le-reseau-de-transport-francilien/information/)
- Le Monde, "Pollution de l'air dans le métro : une étude alerte sur le niveau de particules fines". Available: [https://www.lemonde.fr/planete/article/2023/05/23/pollution-de-l-air-dans-le-metro-une-etude-alerte-sur-le-niveau-de-particules-fines_6174442_3244.html](https://www.lemonde.fr/planete/article/2023/05/23/pollution-de-l-air-dans-le-metro-une-etude-alerte-sur-le-niveau-de-particules-fines_6174442_3244.html)

## Annexes

For detailed information on the CayenneLPP frame types, automatic motor control algorithms, and downlink encoders, refer to the full project report.

This README provides an overview of the IoT project for air quality monitoring and ventilation control in confined metro stations. For more detailed information, please refer to the full project report.
