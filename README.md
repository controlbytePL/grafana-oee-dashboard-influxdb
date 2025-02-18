# Grafana Dashboard for MQTT Codesys OEE Data

## Description
This project provides a Grafana dashboard titled **"MQTT Codesys OEE Data"**, designed to visualize key performance indicators (KPIs) of industrial machines. The dashboard connects to an **InfluxDB** database to retrieve and display essential metrics gathered via **MQTT** from a Codesys PLC.

## Key Features
- **OEE (Overall Equipment Effectiveness):** Displays the overall efficiency of the equipment.
- **Quality:** Monitors the percentage of high-quality produced items.
- **Availability:** Tracks machine uptime and availability.
- **Performance:** Measures production speed relative to targets.
- **Machine State:** Indicates real-time machine status (Running/Stopped).
- **Product Weight:** Displays variations in product weight over time.

## Data Source
- **Database:** InfluxDB (Time-series database)
- **Data Input:** Collected from a Codesys PLC using MQTT and stored in InfluxDB.
- **Query Language:** InfluxQL

## Prerequisites
- **Grafana 11.5.1 or later**
- **InfluxDB (v1.8 or later)**
- **MQTT Broker (e.g., Mosquitto)**
- **Codesys PLC configured to publish OEE metrics via MQTT**

## Installation and Setup
1. **Import the Dashboard:** In Grafana, navigate to `Create > Import` and upload the provided JSON file.
2. **Configure the Data Source:** Ensure InfluxDB is set up as a data source with the appropriate database and credentials.
3. **MQTT Data Pipeline:** Verify that MQTT messages from Codesys are correctly logged into InfluxDB.

## Dashboard Panels
- **OEE Gauge:** Real-time OEE percentage with color-coded thresholds.
- **Quality Gauge:** Displays the mean quality value from `oee_data`.
- **Availability Gauge:** Visualizes machine availability.
- **Performance Gauge:** Shows production performance.
- **Machine State Timeline:** Displays a state timeline (Running/Stopped) with color-coded statuses.
- **Product Weight Chart:** Displays historical trends of product weight.

## Usage Notes
- The dashboard updates automatically every minute.
- Threshold colors are configured based on standard KPIs.
- Data grouping uses the `time($__interval)` setting from Grafana.

## Example
![Dashboard Preview](https://kursy.controlbyte.pl/wp-content/uploads/2025/02/2025-02-18_07h05_43-8k9t8y8.png)

## License
This project is licensed under the MIT License.

