Author

Roll No.	  Name	      GitHub username
24ESKCS066	Aryan Jain	er-aryan-jain


# 🌍 AirQualityPrediction

> An end-to-end Machine Learning and DevOps project for predicting **Air Quality Index (AQI)** and **AQI categories** from air-pollutant measurements.

[![CI](https://github.com/skit-devops-2026/devops-24ESKCS066/actions/workflows/ci.yml/badge.svg)](https://github.com/skit-devops-2026/devops-24ESKCS066/actions/workflows/ci.yml)

---

## 📌 Overview

**AirQualityPrediction** is an end-to-end Machine Learning application designed to predict the **Air Quality Index (AQI)** using pollutant concentration data.

The project uses air-quality data collected from the **Central Pollution Control Board (CPCB)** through the Government of India's Open Government Data Platform.

The system combines:

- Data collection
- Data preprocessing
- Machine Learning
- AQI regression
- AQI classification
- FastAPI REST API
- Web-based frontend
- Automated testing
- GitHub Actions CI
- Jenkins CI pipeline
- Git/GitHub version control

The final application allows users to provide pollutant measurements and receive:

1. A predicted numerical AQI value
2. The corresponding AQI category

---

# 🎯 Objectives

The main objectives of the project are:

- Collect air-quality data from a reliable government source.
- Clean and preprocess real-world air-quality data.
- Develop Machine Learning models for AQI prediction.
- Predict both numerical AQI and AQI category.
- Expose the ML models through a REST API.
- Provide a user-friendly web interface.
- Implement automated software testing.
- Implement Continuous Integration using GitHub Actions.
- Implement a Jenkins-based CI pipeline.
- Follow a structured Git and GitHub workflow.

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────────┐
                    │   CPCB / data.gov.in    │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │    Data Collection      │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │ Data Cleaning &         │
                    │ Preprocessing            │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │ Feature Preparation     │
                    └────────────┬────────────┘
                                 │
                                 ▼
              ┌────────────────────────────────────┐
              │       Machine Learning Layer       │
              │                                    │
              │  Random Forest Regressor           │
              │  Random Forest Classifier          │
              └────────────────┬───────────────────┘
                               │
                               ▼
                    ┌─────────────────────────┐
                    │    Saved ML Models      │
                    │       .joblib           │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │     FastAPI Backend     │
                    │                         │
                    │    POST /predict-aqi    │
                    └────────────┬────────────┘
                                 │
                    ┌────────────┴────────────┐
                    │                         │
                    ▼                         ▼
          ┌──────────────────┐      ┌──────────────────┐
          │ Frontend         │      │ Swagger API      │
          │ Dashboard        │      │ Documentation    │
          └──────────────────┘      └──────────────────┘


                     DEVOPS PIPELINE
                            │
              ┌─────────────┴─────────────┐
              │                           │
              ▼                           ▼
       ┌──────────────┐           ┌──────────────┐
       │ GitHub        │           │ Jenkins      │
       │ Actions       │           │ Pipeline     │
       └──────┬───────┘           └──────┬───────┘
              │                          │
              ▼                          ▼
        Automated Tests             Test + Verify
