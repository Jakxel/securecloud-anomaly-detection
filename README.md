# SecureCloud Lite
## Real-Time Cloud Log Anomaly Detection System

---

# 1. Project Overview

SecureCloud Lite is a cloud-based security monitoring system designed to detect anomalous behavior in simulated cloud infrastructure logs using machine learning techniques.

The system analyzes log events in real time, identifies deviations from normal behavioral patterns, and generates alerts when suspicious activities occur.

This project demonstrates the integration of:

- Cloud deployment
- Event-driven processing
- Unsupervised machine learning
- Containerization
- Full-stack development

---

# 2. Problem Statement

Modern cloud environments generate continuous activity logs such as:

- User login events
- Resource creation or deletion
- Permission changes
- API usage events

These logs are typically stored but not actively analyzed in real time. Manual monitoring is inefficient and may fail to detect abnormal patterns early.

The problem addressed by this project is:

> How can anomalous cloud behavior be detected automatically in real time using machine learning?

---

# 3. Project Objectives

## General Objective

Design and implement a cloud-based system capable of detecting anomalous infrastructure behavior using unsupervised learning.

## Specific Objectives

- Simulate realistic cloud infrastructure logs
- Develop a backend service to process log events
- Implement anomaly detection using Isolation Forest
- Store and manage processed data
- Provide a visualization dashboard
- Deploy the system in a cloud environment using Docker

---

# 4. System Scope

This project includes:

- Log simulation (cloud-like events)
- Real-time anomaly detection
- Database storage
- Email alerting system
- Web dashboard visualization
- Cloud deployment on a virtual machine

This project does not include:

- Multi-cloud integration
- Enterprise-grade SIEM functionality
- Complex distributed streaming clusters
- Automated remediation

---

# 5. System Architecture

High-level architecture:

Log Generator → Backend API → ML Model  
Backend → Database  
Backend → Email Alerts  
Frontend Dashboard → Backend API  

## Components

### 1. Log Generator
A Python-based module that simulates cloud events, including:

- Normal user activity
- Anomalous events

### 2. Backend Service
Built with FastAPI, responsible for:

- Receiving and processing logs
- Extracting relevant features
- Running anomaly detection
- Storing results
- Triggering alerts

### 3. Machine Learning Model
Isolation Forest (unsupervised learning):

- Learns normal behavior patterns
- Detects outliers
- Flags anomalous events

### 4. Database
PostgreSQL database for:

- Log storage
- Anomaly records
- Event history

### 5. Frontend Dashboard
React-based interface that displays:

- Total logs processed
- Total anomalies detected
- Timeline of anomalies
- Detailed anomaly table

### 6. Deployment Environment
Dockerized application deployed on a cloud virtual machine.

---

# 6. Anomaly Detection Strategy

The system focuses on detecting two types of anomalies:

## 1. Unusual Login Time

If a user typically logs in between 8 AM and 6 PM, a login at 3 AM may be flagged as anomalous.

## 2. Abnormal Resource Creation Spike

If the system detects an unusual number of resource creation events within a short time window, it is flagged as suspicious.

The Isolation Forest model is trained using baseline "normal" simulated behavior and identifies statistical outliers.

---

# 7. Technology Stack

## Backend
- Python
- FastAPI
- Scikit-learn
- SQLAlchemy

## Frontend
- React
- Axios

## Database
- PostgreSQL

## DevOps & Deployment
- Docker
- Docker Compose
- Cloud VM (AWS EC2 or GCP Compute Engine)

---

# 8. Development Methodology

The project will follow an incremental development approach:

1. Log simulation
2. Backend implementation
3. ML model integration
4. Database integration
5. Frontend development
6. Containerization
7. Cloud deployment
8. Testing and validation

---

# 9. Expected Results

At completion, the system will:

- Process simulated cloud logs in real time
- Detect anomalous events automatically
- Generate email alerts
- Provide a web-based monitoring dashboard
- Run fully containerized in a cloud environment

---

# 10. Evaluation Metrics

The system will be evaluated using:

- Detection accuracy
- False positive rate
- System response time
- Stability under simulated load
- Deployment reproducibility

---

# 11. Limitations

- Uses simulated data instead of production logs
- Limited anomaly types
- Single-node deployment
- No automated remediation system

---

# 12. Future Work

Potential extensions include:

- Integration with real CloudTrail logs
- Advanced anomaly detection models (LSTM)
- Multi-node scalable architecture
- Kubernetes-based deployment
- Automated response actions
- Risk scoring system

---

# 13. Conclusion

SecureCloud Lite provides a realistic, scalable prototype of a cloud-native anomaly detection system. It demonstrates practical application of machine learning in cloud security while maintaining a feasible development scope for a two-member team.

The project balances technical depth with realistic implementation constraints and showcases competencies in backend development, cloud deployment, and applied machine learning.
