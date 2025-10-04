
# Server Monitoring Guide

## 1. Install Grafana
sudo apt install -y grafana 
sudo systemctl enable grafana-server 
sudo systemctl start grafana-server

## 2. Install Prometheus
sudo apt install prometheus 
sudo systemctl enable prometheus 
sudo systemctl start prometheus

## 3. Grafana Setup
- Log in to Grafana via `http://your-server-ip:3000`
- Add Prometheus as a data source
- Create dashboards for:
  - CPU usage
  - Memory usage
  - Disk space
  - Network traffic

## 4. Alerts Setup
- Configure Grafana alerts for important metrics

## 5. Logs Monitoring
- Use tools like `journalctl` or ELK Stack
journalctl -u grafana-server

