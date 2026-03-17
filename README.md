# DevOps Monitoring Stack

# DevOps Monitoring Stack

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Prometheus](https://img.shields.io/badge/monitoring-prometheus-orange)
![Grafana](https://img.shields.io/badge/visualization-grafana-F46800)
![Node Exporter](https://img.shields.io/badge/exporter-node--exporter-green)

This project demonstrates a basic infrastructure monitoring stack using **Prometheus**, **Grafana**, and **Node Exporter**.

## Table of Contents

- Architecture
- Technologies
- Monitoring Screenshots
- Repository Structure
- Purpose

The stack collects system metrics from Linux servers, stores them in Prometheus, and visualizes them using Grafana dashboards.

---

## Architecture

Linux servers expose system metrics through **Node Exporter**.  
**Prometheus** periodically scrapes these metrics and stores them as time-series data.  
**Grafana** connects to Prometheus and visualizes the metrics through dashboards.


![Monitoring Architecture](architecture/monitoring-architecture.png)

---

## Technologies

- Prometheus
- Grafana
- Node Exporter
- Linux

---

## Monitoring Screenshots

### Grafana Dashboard

Example Grafana dashboard showing system metrics such as CPU usage, memory usage, and disk utilization.

![Grafana Dashboard](screenshots/grafana-dashboard.png)

---

### Prometheus Targets

Prometheus successfully scraping metrics from Node Exporter instances running on monitored servers.

![Prometheus Targets](screenshots/prometheus-targets.png)

---

## Repository Structure

devops-monitoring-stack
│
├── architecture
│ └── monitoring-architecture.png
│
├── prometheus
│ └── prometheus.yml
│
├── grafana
│ └── node-exporter-dashboard.json
│
├── screenshots
│ ├── grafana-dashboard.png
│ └── prometheus-targets.png
│
└── README.md

## Purpose

This repository demonstrates a simple **monitoring and observability setup for Linux infrastructure** using open-source tools commonly used in DevOps environments.