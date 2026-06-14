# Environmental Stress Analytics Platform

A full-stack environmental monitoring pipeline integrating Arduino sensors with Python-based data workflows, from hardware sensing to decision-ready visualisation.

> **Status:** In progress — currently building and testing the sensor circuit.

---

## Overview

This project captures real-time environmental data using Arduino-connected sensors, processes and stores it using Python and MySQL, and visualises trends through Power BI dashboards. The goal is to surface actionable environmental insights for non-technical stakeholders.

---

## Sensors

| Sensor | Measures |
|---|---|
| Water Level Sensor | Water presence and depth |
| Light Sensor (LDR) | Ambient light intensity |
| Ultrasonic Distance Sensor (HC-SR04) | Object proximity / distance |
| Sound Sensor | Ambient noise levels |

---

## Planned Architecture

```
Arduino (sensors)
    ↓  Serial (USB)
Python / PySerial
    ↓  Data cleaning & transformation (Pandas)
MySQL Database
    ↓  Downstream analysis
Power BI Dashboard
```

---

## Tech Stack

| Layer | Tools |
|---|---|
| Hardware | Arduino, sensors/actuators |
| Serial Communication | PySerial |
| Data Processing | Python, Pandas, NumPy |
| Database | MySQL |
| Visualisation | Power BI |
| Prototyping | Tinkercad |

---

## Project Structure

```
environmental-stress-analytics/
├── arduino/
│   └── sensors.ino          # Arduino sketch for sensor data collection
├── python/
│   ├── serial_reader.py     # Reads serial data from Arduino via PySerial
│   ├── transform.py         # Cleans and transforms raw sensor data (Pandas)
│   └── db_writer.py         # Writes processed data to MySQL
├── sql/
│   └── schema.sql           # Database schema
├── dashboards/
│   └── environmental.pbix   # Power BI dashboard file
├── requirements.txt
└── .gitignore
```

---

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/Khalisah-Kazi/<repo-name>.git
cd <repo-name>
```

### 2. Install Python dependencies
```bash
pip install -r requirements.txt
```

### 3. Upload the Arduino sketch
Open `arduino/sensors.ino` in the Arduino IDE and upload to your board.

### 4. Configure the database
Run the schema file to set up your MySQL database:
```sql
source sql/schema.sql;
```

### 5. Run the pipeline
```bash
python python/serial_reader.py
```

---

## Requirements

```
pyserial
pandas
numpy
mysql-connector-python
```

---

## Author

**Khalisah Kazi**  
BSc Information Technology, Middlesex University Dubai  
[LinkedIn](www.linkedin.com/in/khalisah-kazi-93b933325) · [GitHub]((https://github.com/kazi15khalisah))
