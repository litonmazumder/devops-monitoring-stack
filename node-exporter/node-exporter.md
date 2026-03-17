# Install Node Exporter to servers

## Overview

To monitor application and database servers with Prometheus, exporters are installed on target servers. Exporters expose metrics that Prometheus can scrape.

Downloads latest file from the internet to your server
```
wget https://github.com/prometheus/node_exporter/releases/latest/download/node_exporter-1.10.2.linux-amd64.tar.gz
```
Extracts the compressed archive
```
tar xvf node_exporter-1.10.2.linux-amd64.tar.gz
```
change directory
```
cd node_exporter-1.10.2.linux-amd64
```
Copy the binary executable to a system path
```
sudo cp node_exporter /usr/local/bin/
```
Run node exporter
```
node_exporter
```
Open the metrics endpoint:
```
http://192.168.x.x:9100/metrics
```
Create the service file
```
sudo nano /etc/systemd/system/node_exporter.service
```
```
[Unit]
Description=Node Exporter
After=network.target

[Service]
ExecStart=/usr/local/bin/node_exporter
Restart=always
User=nobody

[Install]
WantedBy=multi-user.target
```
sudo systemctl enable node_exporter
```
sudo systemctl daemon-reload
```
Start the exporter
```
sudo systemctl start node_exporter
```
Enable auto-start(This makes it start after every reboot)
```
sudo systemctl enable node_exporter
```
Check status
```
systemctl status node_exporter
```

