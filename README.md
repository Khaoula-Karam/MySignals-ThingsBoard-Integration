# MySignals ThingsBoard Integration

**Presented for the award of the degree of:**
Master in Big Data and Cloud Computing

**Title:**
_Towards Predictive Analytics Algorithms for Attack Prediction in IoT Platforms_

**Author:**
- Karam Khaoula (karamkhaoula.officiel@gmail.com)

**Supervision and Contribution:**
- Abderrahmane Aqachtoul (abderrahmanaqachtoul@gmail.com)
- Prof. M. Bakhouya, International University of Rabat (Internship Advisor)
- Prof. N. Rafalia, Faculty of Science, Kenitra (Advisor)

## Introduction

### What is MySignals?
[MySignals](https://web.archive.org/web/20170709033035/https://www.cooking-hacks.com/mysignals-hw-v1-ehealth-medical-biometric-iot-platform-arduino-tutorial/) is a comprehensive eHealth platform developed by Libelium. It allows for the monitoring of over 15 different biometric parameters using a variety of medical sensors, including:
- ECG (Electrocardiography)
- SPO2 (Oxygen Saturation in Blood)
- Airflow
- Blood Pressure
- Glucometer
- Temperature
- And many more...

The platform is designed to capture and process health-related data and is compatible with Arduino, making it ideal for developers and researchers interested in creating their own health monitoring systems.

### MySignals Sensors
MySignals sensors enable the real-time collection of various health metrics. These sensors include:
- **ECG Sensor**: For monitoring heart rate and detecting arrhythmias.
- **SPO2 Sensor**: To measure blood oxygen levels.
- **Airflow Sensor**: Useful for respiratory monitoring and conditions like sleep apnea.
- **Blood Pressure Sensor**: For tracking systolic and diastolic blood pressure.
- **Glucometer**: For monitoring blood sugar levels.

The integration with ThingsBoard enables efficient real-time monitoring, data visualization, and alerts for these health parameters. For a complete guide on how to work with MySignals, refer to the PDF guide included in this repository.

### What is ThingsBoard?
[ThingsBoard](https://thingsboard.io/docs/) is an open-source IoT platform that provides device management, data collection, processing, and visualization for IoT solutions. It supports scalable and flexible architectures for IoT and is used for data monitoring and real-time analysis in various industries.

**Key Features of ThingsBoard**:
- **Device Management**: Efficiently manage thousands of devices, their connectivity, and configuration.
- **Data Collection & Processing**: Real-time telemetry data ingestion and processing using complex event processing (CEP).
- **Data Visualization**: Build customizable dashboards to visualize real-time data from connected devices.
- **Rules Engine**: Automate actions and alerting based on incoming data using the powerful rule engine.
- **Scalability**: Designed to support high-throughput data with horizontal scalability.

ThingsBoard provides a reliable platform for building IoT applications, especially when handling multiple sensors and collecting large amounts of telemetry data, like in this project with MySignals. More details about ThingsBoard can be found in their official [documentation](https://thingsboard.io/docs/).

### For More Information
For detailed information on setting up and using MySignals, check out the [MySignals Technical Guide](docs/mysignals_technical_guide_sw.pdf) located in the `/docs` folder.

## Repository Structure

- **/docs**: Contains guides and documentation, including the [MySignals Technical Guide](docs/mysignals_technical_guide_sw.pdf).
- **/code**: Arduino code for real-time sensor data collection from MySignals.
- **/challenges**: Detailed discussion of challenges encountered during development and the solutions applied.
- **/development**: Contains the ThingsBoard environment setup files.

## Project Overview

### Objective
The goal of this project is to develop an IoT-based health monitoring system using MySignals eHealth sensors, Arduino, and ThingsBoard for data collection, visualization, and real-time monitoring.

### Contents

- **mysignals_technical_guide_sw.pdf**: A comprehensive guide to working with the MySignals HW platform, detailing setup instructions, sensor usage, and integration tips.
  
- **MYSIGNALS_Tabs_codes.rar**: Arduino code organized into tabs to support multiple sensors, including ECG, SPO2, airflow, and others, with real-time data acquisition.

- **THINGSBORD_ENV_Setup.rar**: Contains the setup and configuration files for deploying a ThingsBoard environment to capture and visualize data from MySignals sensors.

## Challenges and Solutions

### 1. Simultaneous Data Collection from Multiple Sensors
- **Problem**: We encountered conflicts when attempting to collect data from multiple sensors at the same time. Sensor data was inaccurate due to interference between sensors.
  
- **Solution**: We separated the code for each sensor into different tabs in the Arduino IDE. This allowed us to isolate the processing for each sensor and prevent interference.

### 2. Calibration Techniques
- **Problem**: Data from the sensors, especially ECG and airflow, was inaccurate due to miscalibration.

- **Solution**: We implemented calibration techniques, including repositioning sensors and adjusting reference points to ensure accurate readings.

## Setup Instructions

### Arduino Setup
1. **Download the Code**: Extract the `MYSIGNALS_Tabs_codes.rar` file from the **/code** folder.
2. **Open in Arduino IDE**: Open the `.ino` file in Arduino IDE. Each sensor’s code is separated into tabs to help manage different sensors.
3. **Upload to MySignals**: Ensure all sensors are properly connected and upload the code to the Arduino board.

### ThingsBoard Setup
1. **Environment Setup**: Extract the `THINGSBORD_ENV_Setup.rar` file from the **/development** folder.
2. **Follow the Documentation**: Refer to the included instructions to set up a ThingsBoard environment that communicates with MySignals sensors.
3. **Connect the Sensors**: Use the MySignals sensors to collect real-time data and visualize it using the ThingsBoard dashboard.

## Application Development

We have developed an IoT application using ThingsBoard to monitor the data from MySignals sensors in real-time. The application provides:
- Real-time data visualization for various health parameters such as ECG, SPO2, blood pressure, and airflow.
- Alerts and notifications when health parameters exceed predefined thresholds.

## How to Use the Project

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Khaoula-Karam/MySignals-ThingsBoard-Integration.git
