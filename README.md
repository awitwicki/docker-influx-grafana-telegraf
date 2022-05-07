# docker-influx-grafana-telegraf
Monitoring service for easy server metrics logging

## Quick Start

```
sudo chown -R 472:472 /data/grafana/
docker-compose up --build
```

## Grafana

Open <http://localhost:3000>

```
Username: admin
Password: admin
```

You can find server metrics dashboard in `dashboards` -> `manage` -> `general` list

# Advanced level

## Mapped Ports

```
Host		Container		Service

3000		3000			grafana
8086		8086			influxdb

8092		8092/udp		telegraf
8094		8094			telegraf
8125		8125/udp		telegraf
```

## InfluxDB

```
URL: http://localhost:8086
Port: 8086
```

### InfluxDB Shell (CLI)

1. Establish a ssh connection with the container
2. Launch `influx` to open InfluxDB Shell (CLI)
