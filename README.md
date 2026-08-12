# AWS EC2 Application server Monitoring using Prometheus and Grafana

## Project Overview

This project demonstrates how to monitor an application running on an AWS EC2 instance using Prometheus, Node Exporter and Grafana.

The application is deployed on one Ubuntu EC2 instance and the monitoring components are deployed on a separate Ubuntu EC2 instance.

## Architecture

Application EC2
    |
    | Node Exporter :9100
    |
    v
Prometheus :9090
    |
    v
Grafana :3000

## Components

- AWS EC2
- Ubuntu
- Python Flask
- Node Exporter
- Prometheus
- Grafana

## Infrastructure

### Application Server

The Application EC2 instance contains:

- Python Flask application
- Node Exporter

Node Exporter exposes system metrics on:

http://<APPLICATION_IP>:9100/metrics

### Monitoring Server

The Monitoring EC2 instance contains:

- Prometheus
- Grafana

Prometheus runs on:

http://<MONITORING_IP>:9090

Grafana runs on:

http://<MONITORING_IP>:3000

## Metrics Monitored

The following metrics are monitored:

- CPU utilization
- Memory utilization
- Disk utilization
- Server availability
- Network metrics
- Node Exporter metrics

## Grafana Dashboard

The Grafana dashboard contains three main panels:

1. CPU Utilization
2. Memory Utilization
3. Disk Utilization

## Prometheus Configuration

Prometheus is configured to scrape:

- Prometheus itself
- Application EC2 Node Exporter

The configuration file is available at:

prometheus/prometheus.yml

## Application

The Flask application source code is available in:

application/app.py

## Installation steps document also added detailly
setup.docx
