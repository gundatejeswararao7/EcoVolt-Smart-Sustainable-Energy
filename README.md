# ⚡ EcoVolt — Secure IoT Smart Energy Meter

> **An IoT-powered smart energy monitoring and billing system designed to track electricity consumption in real time, analyze usage patterns, control electrical loads, and provide meaningful energy insights through a modern web dashboard.**

<p align="center">

<img src="https://img.shields.io/badge/FRONTEND-555555?style=flat-square" />
<img src="https://img.shields.io/badge/REACT-61DAFB?style=flat-square&logo=react&logoColor=white" />
<img src="https://img.shields.io/badge/TAILWIND_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
<img src="https://img.shields.io/badge/VITE-646CFF?style=flat-square&logo=vite&logoColor=white" />
<img src="https://img.shields.io/badge/BACKEND-555555?style=flat-square" />
<img src="https://img.shields.io/badge/NODE.JS-339933?style=flat-square&logo=node.js&logoColor=white" />
<img src="https://img.shields.io/badge/EXPRESS.JS-000000?style=flat-square&logo=express&logoColor=white" />
<img src="https://img.shields.io/badge/MONGODB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
<img src="https://img.shields.io/badge/IOT-555555?style=flat-square" />
<img src="https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white" />
<img src="https://img.shields.io/badge/VOLTAGE_SENSOR-F39C12?style=flat-square" />
<img src="https://img.shields.io/badge/CURRENT_SENSOR-F1C40F?style=flat-square" />
<img src="https://img.shields.io/badge/RELAY_MODULE-E74C3C?style=flat-square" />
<img src="https://img.shields.io/badge/ARDUINO_IDE-00979D?style=flat-square&logo=arduino&logoColor=white" />
<img src="https://img.shields.io/badge/CHART.JS-FF6384?style=flat-square&logo=chart.js&logoColor=white" />
<img src="https://img.shields.io/badge/REST_API-FF6C37?style=flat-square" />
<img src="https://img.shields.io/badge/GIT-F05032?style=flat-square&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GITHUB-181717?style=flat-square&logo=github&logoColor=white" />

</p>

---

## 📌 Overview

**EcoVolt** is a full-stack IoT-based smart energy monitoring platform that combines electrical sensors, an ESP32 microcontroller, backend services, and a modern web dashboard.

The system collects electrical measurements such as **voltage, current, power, and energy consumption** from connected electrical loads. The ESP32 processes sensor readings and communicates with the backend server through a REST API.

Users can monitor their electricity consumption through an interactive React dashboard, analyze usage patterns, estimate electricity costs, and control connected electrical loads through a relay module.

EcoVolt combines:

- ⚡ IoT hardware
- 🔌 Electrical sensors
- 🧠 ESP32 embedded programming
- 🌐 REST API communication
- ⚛️ React web development
- 📊 Data visualization
- 🗄️ MongoDB database management
- 🔐 Authentication and security
- 💰 Energy billing and analytics

---

## 🎯 Project Objectives

The main objectives of EcoVolt are:

- Monitor electricity consumption in real time.
- Measure voltage and current from electrical loads.
- Calculate electrical power and energy usage.
- Store energy-related data for historical analysis.
- Display live readings through a web dashboard.
- Estimate electricity bills based on energy consumption.
- Provide graphical energy consumption analytics.
- Control electrical appliances using a relay module.
- Detect unusually high energy consumption.
- Provide a foundation for future cloud and AI-based energy management.

---

## ✨ Key Features

### ⚡ Real-Time Energy Monitoring

Monitor important electrical parameters including:

- Voltage
- Current
- Power
- Energy consumption
- Connected load status

The ESP32 collects sensor readings and communicates them to the backend for processing and storage.

---

### 📊 Interactive Dashboard

The React dashboard provides a centralized interface for viewing:

- Current energy readings
- Historical consumption
- Power usage
- Energy trends
- Estimated electricity cost
- Device status
- Appliance/relay status

---

### 💰 Electricity Bill Estimation

The system can estimate electricity costs according to configured tariff rates.

```text
Energy Consumption
        ↓
Units Consumed (kWh)
        ↓
Tariff Calculation
        ↓
Estimated Electricity Bill
```

---

### 🔌 Appliance Control

A relay module is integrated with the ESP32 to allow connected electrical loads to be switched ON or OFF.

```text
React Dashboard
       ↓
Node.js API
       ↓
ESP32
       ↓
Relay Module
       ↓
Electrical Load
```

---

### 🚨 High Energy Consumption Alerts

The system can monitor energy usage against configured thresholds.

```text
Energy Reading
      ↓
Compare With Threshold
      ↓
 ┌────┴────┐
 │         │
Normal    High
 │         │
 ▼         ▼
Continue   Alert
Monitoring
```

---

### 📈 Energy Analytics

Historical readings can be analyzed to identify:

- High-consumption periods
- Daily usage patterns
- Energy consumption trends
- Power usage variations
- Potential opportunities for energy savings

---

### 🔐 Secure Application Access

The application is designed with authenticated access so that protected dashboard functionality is available only to authorized users.

Security considerations include:

- User authentication
- Protected routes
- Backend request validation
- Environment variables
- Database access protection
- API security
- IoT device communication security

---

## 🏗️ System Architecture

```text
                 ┌──────────────────────┐
                 │   Electrical Load    │
                 └──────────┬───────────┘
                            │
             ┌──────────────┴──────────────┐
             │                             │
             ▼                             ▼
     ┌───────────────┐             ┌───────────────┐
     │ Voltage Sensor│             │ Current Sensor│
     └───────┬───────┘             └───────┬───────┘
             │                             │
             └──────────────┬──────────────┘
                            ▼
                    ┌──────────────┐
                    │    ESP32     │
                    │              │
                    │ Data Reading │
                    │ Processing   │
                    │ Device Ctrl  │
                    └──────┬───────┘
                           │
                           │ REST API
                           ▼
                  ┌──────────────────┐
                  │   Node.js API    │
                  │    Express.js    │
                  └────────┬─────────┘
                           │
                           ▼
                    ┌──────────────┐
                    │   MongoDB    │
                    │              │
                    │ Energy Data  │
                    │ User Data    │
                    └──────┬───────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │   React Web App  │
                  │                  │
                  │ Dashboard        │
                  │ Analytics        │
                  │ Billing          │
                  │ Device Control   │
                  └──────────────────┘
```

---

## 🔄 Complete Data Flow

```text
Voltage Sensor
       │
       ▼
Current Sensor
       │
       ▼
      ESP32
       │
       │ Collect & Process
       ▼
 REST API Request
       │
       ▼
 Node.js / Express
       │
       ├──────────────► MongoDB
       │                   │
       │                   │ Store readings
       │                   ▼
       │              Historical Data
       │
       ▼
 React Dashboard
       │
       ├──► Live Monitoring
       ├──► Energy Analytics
       ├──► Bill Estimation
       ├──► Consumption Alerts
       └──► Relay Control
```

---

## 🔌 Hardware Components

| Component | Purpose |
| --- | --- |
| **ESP32** | Main IoT microcontroller |
| **Voltage Sensor** | Measures electrical voltage |
| **Current Sensor** | Measures electrical current |
| **Relay Module** | Controls connected electrical loads |
| **Electrical Load** | Device/appliance being monitored |
| **Connecting Wires** | Hardware connections |
| **Power Supply** | Provides required power |

---

## 💻 Software Stack

| Category | Technology |
| --- | --- |
| Microcontroller | ESP32 |
| Embedded Development | Arduino IDE |
| Voltage Measurement | Voltage Sensor |
| Current Measurement | Current Sensor |
| Load Control | Relay Module |
| Frontend | React |
| Styling | Tailwind CSS |
| Backend | Node.js |
| API Framework | Express.js |
| Database | MongoDB |
| Communication | REST API |
| Data Visualization | Chart.js |
| Build Tool | Vite |
| Version Control | Git & GitHub |

---

## 📂 Project Structure

```text
EcoVolt-Smart-Sustainable-Energy/
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── assets/
│   │   └── App.jsx
│   │
│   ├── package.json
│   └── ...
│
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── middleware/
│   ├── config/
│   ├── index.js
│   ├── package.json
│   └── ...
│
├── hardware/
│   ├── esp32/
│   └── ...
│
├── README.md
├── .gitignore
└── ...
```

> The exact folders may vary depending on the current implementation of the project.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/saivamshidanthoju/EcoVolt-Smart-Sustainable-Energy.git
```

Navigate into the project:

```bash
cd EcoVolt-Smart-Sustainable-Energy
```

---

## 🖥️ Frontend Setup

Navigate to the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The React application will be available through the local Vite development server.

---

## ⚙️ Backend Setup

Open a new terminal and navigate to the backend:

```bash
cd backend
```

Install dependencies:

```bash
npm install
```

Start the backend server:

```bash
node index.js
```

---

## 🗄️ MongoDB Configuration

Make sure MongoDB is available before starting the backend.

Create an environment file named `.env` with contents similar to:

```env
MONGODB_URI=your_mongodb_connection_string
PORT=5000
JWT_SECRET=your_secret_key
```

> ⚠️ **Never commit `.env` files or database credentials to GitHub.**

Add the following to `.gitignore`:

```text
.env
node_modules/
```

---

## 🔧 ESP32 Setup

The ESP32 firmware can be developed and uploaded using Arduino IDE.

General workflow:

```text
Install Arduino IDE
        ↓
Install ESP32 Board Support
        ↓
Connect ESP32
        ↓
Configure Sensors
        ↓
Configure Wi-Fi
        ↓
Configure API Endpoint
        ↓
Upload Firmware
        ↓
Start Sending Energy Data
```

The ESP32 collects sensor readings and communicates with the backend API.

---

## 🔗 API Communication

The system follows a client-server architecture.

```text
ESP32
  │
  │ HTTP Request
  ▼
Express.js API
  │
  ├── Validate Data
  ├── Process Reading
  └── Store Data
          │
          ▼
       MongoDB
```

The React frontend retrieves the required information from the backend through REST API endpoints.

---

## 📊 Dashboard Workflow

```text
                  User Login
                      ↓
                  Authentication
                      ↓
                  Dashboard
                      ↓
┌───────────────┬───────────────┬───────────────┐
│               │               │
▼               ▼               ▼
Live Data     Analytics       Billing
│               │               │
▼               ▼               ▼
Voltage       Charts          Units
Current       Trends          Tariff
Power         History         Cost
Energy
    │
    └──────────────┬──────────────┘
                   ▼
             Device Control
                   │
                   ▼
             Relay ON / OFF
```

---

## 🔐 Security Considerations

Security is an important part of the EcoVolt architecture.

The project considers:

- User authentication
- Protected application routes
- Backend request validation
- Secure API communication
- Environment variables for sensitive configuration
- Database access protection
- Separation of frontend and backend responsibilities
- IoT device communication security

For production deployment, additional protections should be implemented, including:

- HTTPS
- IoT device authentication
- API authentication
- Rate limiting
- Input sanitization
- Strong device identity management
- Secure firmware updates
- Role-based access control

---

## 📈 Energy Monitoring Workflow

```text
Sensor Measurement
       ↓
Voltage + Current
       ↓
Power Calculation
       ↓
Energy Calculation
       ↓
ESP32
       ↓
Backend API
       ↓
MongoDB
       ↓
Dashboard
       ↓
Analytics + Billing
```

---

## 🧮 Energy Calculation

The system can use electrical measurements to calculate power and energy consumption.

**Electrical Power**

```text
Power (W) = Voltage (V) × Current (A)
```

**Energy Consumption**

```text
Energy (kWh) = Power (W) × Time (hours) / 1000
```

**Estimated Cost**

```text
Estimated Cost = Energy Consumption (kWh) × Tariff Rate
```

> Actual calculations may vary depending on sensor hardware, sampling method, power factor, tariff structure, and implementation.

---

## 🎓 Skills Demonstrated

**IoT**
- ESP32
- Sensor integration
- Electrical parameter monitoring
- Relay-based device control
- IoT-to-server communication

**Frontend Development**
- React
- Tailwind CSS
- Responsive UI
- Dashboard development
- Data visualization
- API integration

**Backend Development**
- Node.js
- Express.js
- REST API development
- Authentication
- Request validation
- Server-side processing

**Database**
- MongoDB
- Data modeling
- Storing sensor readings
- Historical energy analysis

**Development & Collaboration**
- Git
- GitHub
- Branch-based development
- Pull Requests
- Code reviews
- Team collaboration

---

## 🌱 Benefits of the System

EcoVolt can help users:

- Understand their electricity consumption.
- Monitor electrical parameters remotely.
- Identify high-energy-consuming periods.
- Estimate electricity expenses.
- Control connected electrical loads.
- Analyze historical energy usage.
- Make more informed energy-saving decisions.

---

## 🔮 Future Enhancements

**☁️ Cloud Integration**
- AWS IoT Core
- AWS Lambda
- Amazon DynamoDB
- Firebase

**📡 Advanced IoT Communication**
- MQTT
- WebSockets
- Secure device-to-cloud communication
- Real-time device synchronization

**🤖 Artificial Intelligence**
- Energy consumption prediction
- Anomaly detection
- Appliance usage classification
- Personalized energy-saving recommendations
- Intelligent load optimization

**🚨 Advanced Security**
- Device authentication
- End-to-end encryption
- Role-based access control
- Intrusion/anomaly detection
- Secure firmware updates
- Device certificates

**📱 Mobile Application**
- Live energy monitoring
- Push notifications
- Remote appliance control
- Bill tracking
- Energy analytics

**⚡ Smart Energy Management**
- Automatic appliance scheduling
- Load optimization
- Peak-hour alerts
- Power anomaly detection
- Multiple ESP32 devices
- Multi-home energy monitoring
- Smart energy recommendations

---

## 👥 Team Collaboration

This project is developed collaboratively using Git and GitHub.

Recommended workflow:

```text
                    ┌──────────┐
                    │   main   │
                    └────┬─────┘
                         │
             ┌───────────┼───────────┐
             │           │           │
             ▼           ▼           ▼
        Backend       Frontend    Hardware
         Branch        Branch       Branch
             │           │           │
             └───────────┼───────────┘
                         │
                         ▼
                   Pull Requests
                         │
                         ▼
                       main
```

Each team member can work on a separate branch, submit changes through Pull Requests, review the code, and merge approved changes into the main branch.

---

## 📊 Project Status

🚧 **Academic / Mini Project**

EcoVolt is being developed as an IoT-based smart energy monitoring and management solution.

The system can be further extended with cloud deployment, advanced analytics, AI-powered recommendations, mobile applications, and production-level security.

---

## 🛡️ Safety Notice

> ⚠️ **Electrical safety is critical.**
>
> Working with mains electricity can cause serious injury, fire, or death. Sensor and relay wiring should only be performed using appropriate isolation, protection, rated components, and safe electrical practices. Do not work on energized mains circuits without proper qualifications and safety procedures.

---

## 📜 License

This project is developed for **educational and academic purposes**.

---

## 📫 Contact

**GitHub**

**Gunda Tejeswara Rao**

https://github.com/gundatejeswararao7

---

## ⭐ Support

If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub.

---

<div align="center">

### ⚡ Built with IoT + ESP32 + React + Node.js + MongoDB

**EcoVolt — Monitor. Analyze. Optimize. Save Energy. 🌱**

</div>
