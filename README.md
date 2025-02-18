# Project: Integrating CODESYS with Node-RED, InfluxDB, and Grafana via MQTT

## Description

This project demonstrates how to integrate the CODESYS development environment with Node-RED, InfluxDB, and Grafana using the MQTT protocol. The objective is to transmit data from CODESYS to Node-RED, where it is processed and stored in an InfluxDB database, and subsequently visualized using Grafana.

## Requirements

- **CODESYS**: A development environment for PLCs.
- **Node-RED**: A flow-based development tool for visual programming. [Official Documentation](https://nodered.org/docs/)
- **InfluxDB**: A time-series database.
- **Grafana**: A data visualization platform. [Official Documentation](https://grafana.com/docs/)
- **MQTT Broker**: e.g., Mosquitto.

## Installation and Configuration

### 1. CODESYS

- **MQTT Configuration**: Set up the MQTT client in CODESYS to publish data to a specified topic.
- **Sample Code**: Available in the current repository.

### 2. Node-RED

- **Installation**: Follow the [official getting started guide](https://nodered.org/docs/getting-started/).
- **Importing Flows**: Import the flow from the `flows.json` file available in the repository [MQTT-INFLUXDB-CODESYS-GRAFANA](https://github.com/controlbytePL/MQTT-INFLUXDB-CODESYS-GRAFANA).
- **MQTT Configuration**: Configure the MQTT node to subscribe to the topic used by CODESYS.
- **Data Processing**: Add nodes to parse JSON data and store it in InfluxDB.

### 3. InfluxDB

- **Installation**: Download and install InfluxDB from the [official site](https://docs.influxdata.com/influxdb/v1.8/introduction/install/).
- **Configuration**: Create a database where Node-RED will store the data.

### 4. Grafana

- **Installation**: Follow the [official installation guide](https://grafana.com/docs/grafana/latest/installation/).
- **Adding Data Source**: Configure Grafana to use the InfluxDB database.
- **Importing Dashboard**: Import the dashboard from the [grafanamqtt](https://github.com/controlbytePL/grafanamqtt) repository.

## Running on Windows

1. **Node-RED**: Open the command prompt and run `node-red` to start the environment.
2. **Mosquitto Broker**: Start the Mosquitto service.
3. **InfluxDB**: Start the InfluxDB service.

## Notes

- Ensure all services are running and properly configured before starting.
- Adjust configurations as needed, especially IP addresses, ports, and MQTT topics.

## Repository Links

- [MQTT-INFLUXDB-CODESYS-GRAFANA](https://github.com/controlbytePL/MQTT-INFLUXDB-CODESYS-GRAFANA)
- [grafanamqtt](https://github.com/controlbytePL/grafanamqtt)

## License

This project is licensed under the MIT License. 
