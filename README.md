# Raspberry Pi Monitoring
This repo contains an easy to setup monitoring solution for a Raspberry Pi, using Telegraf, InfluxDB and Grafana.

![image](https://github.com/phill4y/pi_monitoring/assets/62095410/c520afb4-722a-44d7-b1e3-7a1e53631e7d)


## Requirements

* Docker
* Docker Compose

## Setup

1. Clone Repository `git clone https://github.com/phill4y/pi_monitoring.git`
2. cd into git repo: `cd pi_monitoring`
3. Create persistent storage directories for Grafana and InfluxDB: `mkdir /opt/influxdb /opt/grafana`
4. Adjust permissions: `sudo chmod 775 /opt/influxdb && sudo chmod /opt/grafana`
5. Start docker compose stack: `docker compose up -d`

## View logs of different services

* docker container logs pi-monitoring-influxdb --follow
* docker container logs pi-monitoring-telegraf --follow
* docker container logs pi-monitoring-grafana --follow

## Dashboard configuration

The default dashboard is described in [dashboard.json](./dashboards/dashboard.json) and based on [10578-raspberry-pi-monitoring](https://grafana.com/grafana/dashboards/10578-raspberry-pi-monitoring/)
