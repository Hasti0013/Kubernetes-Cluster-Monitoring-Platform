
# Kubernetes Cluster Monitoring Platform

A cloud-native Kubernetes observability system designed to enhance cluster visibility, workload monitoring, and resource tracking across nodes using metrics-server architecture, custom scraping logic, and Kubernetes-native deployment patterns.

---

## 🚀 Overview

This project implements a Kubernetes-based monitoring platform that collects, processes, and exposes cluster-level metrics for nodes and workloads. It extends standard metrics-server concepts by improving observability, modularizing metric collection components, and enabling scalable deployment using Helm charts.

The system is designed to simulate real-world production monitoring pipelines used in cloud environments for infrastructure visibility and performance tracking.

---

## 🧠 Key Objectives

- Improve cluster-wide visibility into node and pod resource usage  
- Enable structured and scalable metrics collection architecture  
- Support Kubernetes-native deployment and observability workflows  
- Simulate production-grade monitoring pipeline design  

---

## ⚙️ Architecture

The system follows a layered monitoring architecture:

- **Node Layer:** Kubernetes nodes expose resource metrics via kubelet interfaces  
- **Scraper Layer:** Metrics are collected and processed through a scraping mechanism  
- **Metrics Server Layer:** Aggregates and serves cluster-wide metrics via APIs  
- **Storage Layer:** Maintains structured metric data for querying and analysis  

---

## 🧩 Core Components

### 1. Metrics Server
Handles aggregation and exposure of cluster metrics through Kubernetes APIs.

### 2. Scraper Module
Collects metrics from nodes and kubelets and standardizes data formats.

### 3. API Layer
Exposes cluster health and resource utilization data for external tools.

### 4. Storage Layer
Manages internal storage and retrieval of collected metrics.

### 5. Helm Charts
Provides Kubernetes-native deployment configuration for scalable rollout.

---

## 🛠 Tech Stack

- Kubernetes
- Go (core metrics-server components)
- Helm
- Docker
- Linux
- Kubernetes APIs
- Observability concepts (Prometheus-style architecture)

---

## 📊 Key Features

- Cluster-wide CPU, memory, and node-level metrics collection  
- Modular scraper-based architecture for scalability  
- Kubernetes-native deployment using Helm charts  
- High-level observability pipeline design  
- Support for multi-node monitoring environments  

---

## 🎯 Engineering Highlights

- Designed scalable architecture inspired by production Kubernetes monitoring systems  
- Structured modular components for metrics collection and aggregation  
- Improved system observability through enhanced scraping and API layering  
- Implemented deployment automation using Helm for Kubernetes environments  

---

## 📈 Impact

- Improved visibility into cluster and workload performance  
- Enabled structured monitoring of distributed Kubernetes nodes  
- Reduced complexity in tracking resource utilization across systems  

---

## 📁 Repository Structure

- `/pkg` → Core metrics server logic (API, scraper, storage, utilities)  
- `/cmd` → Application entry point  
- `/charts` → Helm deployment configurations  
- `/manifests` → Kubernetes YAML configurations  
- `/test` → Integration and e2e tests  
- `/docs` → Supporting documentation (if added)  

---

## 🚀 How to Run (if applicable)

```bash
# Build components
make build

# Deploy using Helm
helm install metrics-server ./charts/metrics-server

# Apply Kubernetes manifests
kubectl apply -f manifests/
