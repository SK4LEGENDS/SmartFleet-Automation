# 🚗 UiPath Agent Project — Vehicle & Driver Availability Workflow

This repository contains my **first UiPath Agent Development Project**, designed to automate and optimize the process of matching **available drivers and vehicles** for logistics planning based on **route data, weather, and traffic conditions**.

---

## 🧠 Project Overview

The **Vehicle & Driver Availability Workflow** is an AI-integrated automation built using **UiPath Integration Service**.  
It combines **RPA precision** with **AI-driven decision-making** to analyze transportation routes and recommend the best possible plan for logistics dispatch.

### 💡 Key Features
- ✅ Intelligent vehicle & driver matching  
- 🌦️ Weather and traffic analysis for route risk assessment  
- 📊 Smart recommendations with plan and precautions  
- 🧩 Modular workflows for scalability  
- 🔄 AI evaluation pipeline for output scoring  

---

## ⚙️ System Components

| Component | Description |
|------------|--------------|
| **Driver Availability Workflow** | Filters and ranks available drivers based on experience, proximity, and workload. |
| **Vehicle Availability Workflow** | Selects the most suitable vehicles based on type, fuel, capacity, and availability. |
| **Main Agent Workflows** | Central logic that combines route, weather, and resource data to recommend optimal dispatch plans. |
| **Database Tables** | Local database files for storing vehicle and driver details. |
| **Evaluation Sets** | JSON datasets used to test workflow accuracy and AI evaluation performance. |

---

## 🧩 Workflow Architecture

Below are the core UiPath workflows used in the project:

### 🧍 Driver Filtration Workflow
![Driver Filtration Workflow](Driver_Filtration_Workflow.jpg)

### 🚘 Vehicle Filtration Workflow
![Vehicle Filtration Workflow](Vehicle_Filtration_Workflow.jpg)

### 🤖 Main Agents
**Agent 1:**  
![Agent 1](Agent_1.png)

**Agent 2:**  
![Agent 2](Agent_2.png)

---

## 🗂️ Database Structure

### 👨‍✈️ Driver Database
![Driver DB](Driver_DB.png)

**Schema Overview**
| Field | Description |
|--------|--------------|
| Driver ID | Unique identifier for each driver |
| Name | Full name |
| Experience | Years of driving experience |
| Proximity | Distance from current pickup location |
| Phone | Contact number |
| Remarks | Notes on driver. |

### 🚛 Vehicle Database
![Vehicle DB](Vehicle_DB.png)

**Schema Overview**
| Field | Description |
|--------|--------------|
| Vehicle ID | Unique identifier for each vehicle |
| Vehicle Number | Registration number |
| Brand | Manufacturer |
| Model | Vehicle model |
| Type | Truck, Lorry, Van, etc. |
| Fuel | Petrol/Diesel/Electric |
| Capacity | Load capacity |
| Remarks | maintenance note |

---

## 📈 Evaluation Framework

The project uses **AI-based semantic evaluation** to score output JSONs against expected results.  
The evaluator prompt compares contextual accuracy — not exact string matches — allowing flexible and intelligent output scoring.

Example evaluation fields include:
- Route summary accuracy  
- Weather and traffic context  
- Correct mapping of driver/vehicle lists  
- Logical recommendation plans    

---

## 🧾 Example Output Structure

```json
{
  "content": {
    "routeSummary": {
      "origin": "",
      "destination": "",
      "distance": 0,
      "duration": 0
    },
    "trafficAndWeather": {
      "trafficConditions": "",
      "weatherForecast": "",
      "risks": [""]
    },
    "availableDrivers": [
      {
        "name": "",
        "id": "",
        "experience": "",
        "hometownProximity": "",
        "phoneNumber": "",
        "remarks": ""
      }
    ],
    "availableVehicles": [
      {
        "VehicleID": "",
        "VehicleNumber": "",
        "Brand": "",
        "Model": "",
        "Type": "",
        "Fuel": "",
        "Capacity": "",
        "Remark": ""
      }
    ],
    "finalRecommendation": {
      "plan": "",
      "precautions": [""]
    }
  }
}
