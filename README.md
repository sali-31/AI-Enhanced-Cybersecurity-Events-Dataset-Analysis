# AI Enhanced Cybersecurity Events Dataset Data Analysis 

## Overview
This project analyzes a cybersecurity events dataset to identify patterns in attack behavior, severity levels, response actions, and potential data exfiltration. The goal is to transform raw log-style data into clear insights using **Python for analysis/cleaning** and **Power BI for interactive dashboards**.

## Project Goals
- Analyze attack activity over time (monthly trends, intensity patterns).
- Compare **Attack Type** vs **Attack Severity** to identify high-risk categories.
- Measure **Data Exfiltration** frequency and rate.
- Evaluate incident outcomes using **Response Action** (Blocked/Contained/Recovered/Eradicated).
- Explore behavior signals like **User Agents**, time-of-day activity, and day-of-week trends.
- Summarize **Threat Intelligence** information and common keywords.

---

## Dataset Summary
Each row represents a cybersecurity event. Common fields used in this analysis include:
- **Timestamp** (when the event occurred)
- **Attack Type** (e.g., Malware, Phishing, DDoS, Ransomware, Insider Threat)
- **Attack Severity** (Low / Medium / High / Critical)
- **Response Action** (Blocked / Contained / Recovered / Eradicated)
- **Data Exfiltrated** (True/False)
- **Source IP / Destination IP**
- **User Agent**
- **Threat Intelligence** category/text

---

## What I Did

### 1) Data Preparation (Python)
- Loaded and explored the dataset (shape, missing values, unique values).
- Converted **Timestamp** to datetime.
- Created time-based columns for reporting:
  - Year, Month Number, Month Name, Day of Week, Hour
- Verified key categorical columns (Attack Type, Severity, Response Action, Exfil flag).
- Produced summary metrics used later in Power BI.

### 2) Modeling & Measures (Power BI)
- Imported the dataset into Power BI.
- Created DAX measures, including:
  - **Total Events**
  - **Exfil Events** and **Exfil Rate**
  - **Critical Events** and **High Events**
  - **Blocked Actions** and **Blocked Rate**
- Built visuals with slicers (Year, Month, Severity, Type) for interactive analysis.

### 3) Dashboards (Power BI)
Designed 3 report pages with consistent styling and layout, similar to a professional dashboard pack.

---

## Dashboards

### Dashboard 1 — Threat Overview
Focus: high-level view of threat volume and risk.
- Total Events, Exfil Events, Exfil Rate
- Critical and High event counts
- Events per Month trend
- Volume & Exfil Rate by Severity (combo chart)
- Attack Intensity heatmap (Month × Year)
- Exfil Rate by Attack Type
- Events by Response Action

### Dashboard 2 — Entity & Behavior Overview
Focus: event behavior and entity signals.
- Unique User Agents
- Top User Agents (bar chart)
- Events by Hour of Day
- Events by Day of Week
- Severity Mix by Attack Type (stacked bars)

### Dashboard 3 — Response & Intelligence
Focus: response outcomes and threat intelligence.
- Blocked Rate and Exfil Rate KPIs
- Threat Intelligence Category distribution
- Response Actions over time
- Exfil Rate by Response Action
- Exfil Events per Month trend
- Top Intelligence Keywords
- Attack Type × Response Action heatmap

---

## Diagrams Included
This repo includes two diagrams for documentation:
- **Schema Diagram**: shows dataset structure and key fields
- **ERD-style Diagram**: shows conceptual relationships (events, attacks, response actions, IPs, threat intel)

---

## Tools & Technologies
- **Python** (pandas, numpy, matplotlib) for cleaning and analysis
- **Power BI Desktop** for modeling, DAX measures, and dashboards
- Exported images/diagrams for documentation

---

## Author
**Sehar Ali**  
