# Docker Telemetry - Prometheus - Grafana Stack for NX-OS 

========

A monitoring solution for NX-OS switches with [Prometheus](https://prometheus.io/), [Grafana](http://grafana.org/), [NodeExporter](https://github.com/prometheus/node_exporter).

### Prerequisites

Docker Engine >= 1.13
Docker Compose >= 1.11

### Installation

Docker compose is required to run this.

Clone this repository on your Docker host, cd into directory and run compose up:

```sh
$ cd telemetry-prometheus-grafana
$ docker-compose up -d
```

### Diagram:

![](https://github.com/hahasheminejad/telemetry-prometheus-grafana/raw/master/Telemetry-Prometheus-image.jpg)

Containers:

* Prometheus (metrics database) `http://<host-ip>:9090`
* Prometheus-Pushgateway (push acceptor for ephemeral and batch jobs) `http://<host-ip>:9091`
* Grafana (visualize metrics) `http://<host-ip>:3000`
* NodeExporter (host metrics collector)
* Docker Telemetry Receiver `http://<host-ip>:50001`
