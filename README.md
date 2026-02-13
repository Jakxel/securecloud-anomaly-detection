# SecureCloud – Cloud Infrastructure Anomaly Detection System

SecureCloud is a cloud-native security platform that detects anomalous behavior in cloud infrastructure in real time.  
It analyzes infrastructure logs, learns normal behavioral patterns, and alerts administrators when suspicious activities occur.

---

## Project Overview

Modern cloud environments generate thousands of events per minute:

- User logins  
- Resource creation/deletion  
- IAM policy changes  
- Network configuration updates  

Traditional systems only store logs. SecureCloud goes further:

- Processes logs in real time  
- Applies machine learning to detect abnormal patterns  
- Generates automated alerts  
- Provides a security monitoring dashboard  

---

## Project Objectives

- Build an event-driven cloud-native architecture
- Implement real-time anomaly detection
- Apply unsupervised machine learning
- Deploy scalable microservices
- Provide observability and alerting mechanisms

---

## 🏗 System Architecture

High-level flow:

Cloud Logs → Event Stream → Processing Service → ML Model  
→ Anomaly Classification → Database → Dashboard + Alerts

### Main Components

1. **Log Source**
   - AWS CloudTrail (or simulated logs)

2. **Event Streaming**
   - Kafka / AWS Kinesis

3. **Processing Service**
   - Python (FastAPI)
   - Runs in Docker container
   - Deployed on Kubernetes

4. **Machine Learning Model**
   - Isolation Forest (unsupervised anomaly detection)

5. **Database**
   - PostgreSQL or DynamoDB

6. **Alert System**
   - Email notifications (SNS)
   - Dashboard alerts

7. **Frontend Dashboard**
   - React
   - Real-time visualization

---

## Anomaly Detection Strategy

SecureCloud uses unsupervised learning to detect:

- Unusual login times
- Sudden privilege escalations
- Abnormal resource creation spikes
- Suspicious geographic access patterns
- Unusual API usage frequency

Initial model: **Isolation Forest**

---

##  Tech Stack

### Backend
- Python
- FastAPI
- Scikit-learn
- Docker

### Cloud & Infrastructure
- AWS (or GCP)
- Kubernetes
- Terraform (optional)

### Streaming
- Kafka or Kinesis

### Database
- PostgreSQL or DynamoDB

### Frontend
- React
- WebSockets

### DevOps
- GitHub Actions
- Prometheus + Grafana (optional)

---

##  Scalability Features

- Event-driven architecture
- Horizontal Pod Autoscaling (HPA)
- Microservices design
- Stateless processing services

---

##  Security Considerations

- IAM role-based access control
- Encrypted communication (TLS)
- Secure API endpoints
- Principle of least privilege

---
    
##  Future Improvements

- Multi-cloud support
- Deep learning-based detection
- Risk scoring system
- Automated remediation
- Zero-trust integration

---


## 📜 License

MIT License
