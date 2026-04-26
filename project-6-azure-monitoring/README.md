# 📊 Project 6 – Azure Monitoring and Logging

## 📌 Overview

This project demonstrates how Azure engineers monitor cloud infrastructure using Azure Monitor and Log Analytics.

---

## 🎯 Goal

To understand how cloud systems are monitored using metrics and logs.

---

## 🛠️ Technologies Used

* Azure Monitor
* Log Analytics Workspace
* Virtual Machines
* KQL (Kusto Query Language)

---

## ⚙️ What I Built

* Created a Log Analytics Workspace
* Connected a Virtual Machine to monitoring
* Enabled diagnostics logging
* Queried logs using KQL
* Viewed real-time metrics

---

## 📊 Metrics vs Logs

| Type    | Description                                            |
| ------- | ------------------------------------------------------ |
| Metrics | Real-time performance data (CPU, memory, network)      |
| Logs    | Detailed records used for troubleshooting and analysis |

---

## 🔍 Sample Queries

```kusto
Heartbeat
| take 10
```

```kusto
Perf
| where CounterName == "% Processor Time"
| take 10
```

---

## 📸 Screenshots

Screenshots are included in the `/screenshots` folder.

---

## 🧠 What I Learned

* How Azure Monitor collects metrics and logs
* Difference between metrics and logs
* How to query logs using KQL
* Importance of monitoring in cloud environments

---

## 🚧 Challenges Faced

* Understanding how to connect VM to Log Analytics
* Learning KQL queries

---

## ✅ Outcome

Successfully monitored a VM and analysed logs using Azure tools.

---

## 🔄 Next Steps

* Create alert rules (e.g. CPU > 80%)
* Automate monitoring responses
* Integrate with security tools
