# ProYield — Automated Production Test & Yield Analysis System

## 📌 Project Overview
This project implements an automated production test analysis system designed to simulate, validate, and analyze electronic device test results in a manufacturing-like environment.

The system emulates production test workflows commonly used in semiconductor and electronics manufacturing, applying specification limits, classifying failures, calculating yield, and generating automated engineering reports and statistical visualizations.

The project is intentionally focused on **test engineering, automation, and data-driven decision-making**, reflecting real-world practices used in companies such as **Texas Instruments, Intel, and Micron**.

---

## 🎯 Project Objectives
- Simulate production test measurements for electronic devices (DUTs)
- Apply lower and upper specification limits (LSL / USL)
- Automatically classify devices as PASS or FAIL
- Identify dominant failure modes
- Calculate production yield and quality metrics
- Generate engineering-grade statistical visualizations
- Demonstrate structured, scalable, and maintainable Python design

---

## 🏭 Industrial Context
In high-volume semiconductor manufacturing, every device must pass a sequence of electrical and timing tests before shipment. These tests ensure compliance with strict specifications and are critical for maintaining product quality and manufacturing efficiency.

This project models a simplified version of such environments:
- Each simulated sample represents a **Device Under Test (DUT)**
- Multiple electrical and timing parameters are evaluated
- Any out-of-spec condition results in device rejection
- Yield loss contributors are automatically identified

---

## 🔧 System Architecture
The system follows a standard industrial test data pipeline:
Production Test Simulation
↓
Specification Validation (LSL / USL)
↓
Pass / Fail Classification
↓
Failure Mode Identification
↓
Yield Calculation
↓
Statistical Analysis & Visualization

---

## 🧪 Simulated Test Parameters
The system simulates representative production test measurements:

| Parameter        | Description                        | Specification Limits |
|------------------|------------------------------------|----------------------|
| Output Voltage   | Regulated output voltage stability | 4.8 V – 5.2 V        |
| Current Draw     | Device current consumption          | 90 mA – 120 mA       |
| Rise Time        | Signal timing performance           | 8 ns – 12 ns         |

Statistical variation and noise are intentionally introduced to emulate realistic manufacturing conditions.

---

## ⚠️ Pass / Fail and Failure Mode Logic
Each DUT is evaluated against its specification limits:
- A device **FAILS** if any single parameter violates its limits
- Failure modes are recorded per device (voltage, current, rise_time)
- Devices passing all tests are classified as **PASS**

This logic reflects real production test decision criteria.

---

## 📊 Yield and Quality Metrics
The system automatically computes:
- Total units tested
- Passed units
- Failed units
- Overall production yield
- Failure distribution by test parameter

These metrics are essential for monitoring process health and identifying yield loss drivers.

---

## 📈 Statistical Distribution Analysis (Visual Results)
> <img width="586" height="479" alt="image" src="https://github.com/user-attachments/assets/8d37cfa0-a329-45be-bb0e-fe28d9c681f8" />
> <img width="569" height="472" alt="image" src="https://github.com/user-attachments/assets/955832b8-1a4c-40b0-8a57-0dc24b912d85" />
> <img width="586" height="458" alt="image" src="https://github.com/user-attachments/assets/5035965a-bbbe-4747-bb05-2348f3b9da9d" />



This section is intended to include statistical distributions of each test parameter with specification limits overlaid, enabling rapid visual assessment of process centering, spread, and dominant failure mechanisms.

---

## 📁 Project Structure

ProYield/
│
├── analysis/
│ └── production_test_analysis.py
│
├── data/
│ └── test_results.csv
│
├── images/
│ ├── voltage_histogram.png
│ ├── current_histogram.png
│ └── rise_time_histogram.png
│
├── requirements.txt
└── README.md

---

## ▶️ How to Run the Project
1. Install dependencies:
```bash ```
``` pip install -r requirements.txt ```
2.- Execute the analysis:
python analysis/production_test_analysis.py

3.- Outputs:

CSV file containing test results and classifications

Yield summary printed to console

Automatically generated statistical plots

🧠 Engineering Skills Demonstrated

Production test engineering concepts

Specification-driven validation (LSL / USL)

Yield and failure mode analysis

Automated quality reporting

Industrial data visualization

Clean, modular, and maintainable Python architecture

🚀 Future Enhancements

Integration with real production or ATE data

Statistical Process Control (SPC) metrics

Database-backed test result storage

Real-time yield dashboards

Hardware-in-the-loop validation




