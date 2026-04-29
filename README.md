# 🚀 Task 2: Cloud Monitoring and Alerts using AWS CloudWatch

---

## 📌 Objective

To monitor a cloud-based EC2 instance using AWS CloudWatch and configure alerts that notify when system resource usage exceeds a defined threshold.

---

## ☁️ Cloud Platform Used

* **Cloud Provider:** Amazon Web Services (AWS)
* **Monitoring Service:** AWS CloudWatch
* **Resource:** EC2 Instance (Free Tier)

---

## 🛠️ Tools & Services

* AWS EC2
* AWS CloudWatch
* CloudWatch Alarms
* Amazon SNS (Email Notification)

---

## ⚙️ Implementation Steps

### 1️⃣ EC2 Instance Setup

An EC2 instance was launched and used as the monitored resource.

📷 Screenshot:
![EC2 Instance](images/ec2-instance.png)

---

### 2️⃣ Instance Details

Instance configuration including Public IP, Instance Type, and Security settings.

📷 Screenshot:
![Instance Details](images/instance-details.png)

---

### 3️⃣ Simulating High CPU Usage

CPU load was generated using the command:

```bash
yes > /dev/null &
```

This continuously consumes CPU resources.

📷 Screenshot:
![CPU Load](images/cpu-load.png)

---

### 4️⃣ Creating CloudWatch Alarm

A CloudWatch alarm was created with:

* **Metric:** CPUUtilization
* **Threshold:** Greater than 10%
* **Period:** 5 minutes
* **Action:** SNS Email Notification

📷 Screenshot:
![Alarm Created](images/alarm-created.png)

---

### 5️⃣ Alarm State Change

The alarm state changed from **OK → In Alarm**, confirming that CPU usage crossed the threshold.

📷 Screenshot:
![Alarm State](images/alarm-state.png)

---

### 6️⃣ CloudWatch Overview

CloudWatch dashboard showing active alarm and warning indication.

📷 Screenshot:
![Overview](images/cloudwatch-overview.png)

---

### 7️⃣ Recent Alarms Visualization

Graph showing CPU utilization spike in recent alarms.

📷 Screenshot:
![Recent Alarms](images/recent-alarms.png)

---

### 8️⃣ Metrics Graph

Detailed CPU utilization metrics graph.

📷 Screenshot:
![Metrics](images/metrics.png)

---

### 9️⃣ Dashboard Visualization

Custom CloudWatch dashboard displaying CPU utilization graph.

📷 Screenshot:
![Dashboard](images/dashboard.png)

---

### 🔟 Email Notification

Email alert received when CPU usage exceeded threshold.

📷 Screenshot:
![Email Alert](images/email-alert.png)

---

## 📊 Results

* EC2 instance successfully monitored using AWS CloudWatch
* High CPU utilization detected
* Alarm triggered correctly
* Email notification received
* Dashboard graphs clearly showed CPU spike

---

## ✅ Conclusion

This task demonstrated how AWS CloudWatch can be used for real-time monitoring and alerting.
By configuring alarms and notifications, system performance issues can be detected early, improving reliability and system management.

---
