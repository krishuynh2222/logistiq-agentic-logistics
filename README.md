# 🚀 Agentic AI Logistics Optimization System
A real-time, AI-powered logistics decision system that optimizes routes, evaluates risk, and automates dispatch — built with n8n, Google Sheets, and custom optimization logic.

## Why This Project Matters

Most logistics operations still rely on:

- Manual route planning
- Spreadsheet-based tracking
- Delayed decision-making

This system replaces that with:

- Automated route optimization
- Real-time risk evaluation
- AI-assisted decision-making
- End-to-end execution (dispatch + email)

###### ⚡ Designed to mimic how modern logistics companies automate operations with AI + data systems.

## System Workflow
![Workflow](images/n8n_workflow.png)

## 📊 Dashboard (Real Output)
<p align="center"> <img src="images/dashboard.png" width="900"/> </p>

## 📱 Mobile Interface
<p align="center"> <img src="images/mobile.png" width="350"/> </p>

## 📧 Automated Email Dispatch
<p align="center"> <img src="images/mail.png" width="700"/> </p>

## ⚙️ Core Features
#### 📦 1. Data Ingestion
- Reads real shipment data from Google Sheets
- Filters only Pending orders
- Validates required fields (ID, destination, weight)
 
#### 🧮 2. Route Optimization Engine
- Greedy vehicle routing (capacity-aware)
- Groups shipments by proximity
- Calculates:
  - Estimated travel time
  - Fuel efficiency score
  - Route cost
#### 🚦 3. Risk Analysis System
- Traffic-aware routing (dynamic delay factors)
- HOS (Hours of Service) compliance:
  - ≥ 11h → violation
  - ≥ 9h → warning
- Capacity utilization tracking
- Risk scoring model: **risk_score = violation*40 + warning*15 + traffic_spikes*10 + utilization_penalty**
#### 🤖 4. Decision Engine
| Condition                     | Decision  |
| ----------------------------- | --------- |
| Critical risk / HOS violation | ❌ HALT    |
| Medium risk                   | ⚠️ REVIEW |
| Low risk                      | ✅ APPROVE |


#### 🔁 5. Agentic Feedback Loop
- Computes reward signal:
  - Data quality
  - Route efficiency
  - Risk level
  - Decision quality
- Enables future extension into Reinforcement Learning

#### 🎯 Business Impact

This system demonstrates how logistics companies can:

- Reduce manual dispatching effort (~20–30%)
- Improve route efficiency and cost optimization
- Detect operational risks before execution
- Automate reporting and communication
- Enable scalable, AI-assisted decision making

#### 👤 Author

**Kris Huynh**

Computer Science @ NJCU 
