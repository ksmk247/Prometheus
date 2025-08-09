# Server Monitoring and Alerting using Prometheus & Grafana

```markdown
# Server Monitoring and Alerting using Prometheus & Grafana

## 📌 Overview
This project implements a **server monitoring and alerting system** using **Prometheus** and **Grafana**.  
It collects metrics from the server, stores them in Prometheus, visualizes them in Grafana, and triggers alerts when metrics cross defined thresholds.

---

## 🛠 Tech Stack
- **Prometheus** – Time-series database for metrics storage.
- **Grafana** – Visualization and dashboarding.
- **Node Exporter** – For collecting server metrics.
- **Alertmanager** – For managing alerts.
- **Linux Server** – Target system for monitoring.

---

## 🚀 Features
- Real-time server metrics collection.
- Custom Grafana dashboards.
- Alert configuration for critical events.
- Email/Slack notification integration via Alertmanager.

---

## 📂 Project Structure
```

server-monitoring/
│
├── prometheus.yml           # Prometheus configuration file
├── alertmanager.yml         # Alertmanager configuration file
├── dashboards/              # Grafana dashboards JSON files
└── docs/                    # Setup guides & documentation

````

---

## ⚙️ Setup Instructions

### 1️⃣ Install Prometheus
```bash
wget https://github.com/prometheus/prometheus/releases/latest/download/prometheus.tar.gz
tar -xvf prometheus.tar.gz
cd prometheus
./prometheus --config.file=prometheus.yml
````

### 2️⃣ Install Node Exporter

```bash
wget https://github.com/prometheus/node_exporter/releases/latest/download/node_exporter.tar.gz
tar -xvf node_exporter.tar.gz
cd node_exporter
./node_exporter
```

### 3️⃣ Install Grafana

```bash
sudo apt-get install -y apt-transport-https software-properties-common
sudo apt-get install -y grafana
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```

### 4️⃣ Configure Dashboards & Alerts

* Import `dashboards/` JSON files into Grafana.
* Edit `alertmanager.yml` to set up email/Slack alerts.
* Restart services after configuration changes.

---

## 📊 Example Dashboard

![Grafana Dashboard Example](docs/grafana-dashboard.png)

---

## 🔔 Alerting Example

* **CPU Usage > 80%** → Send email to admin.
* **Disk Usage > 90%** → Send Slack notification.

---

## 📝 License

This project is licensed under the MIT License.

---

## 🤝 Contributing

1. Fork this repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature-name
   ```
3. Commit changes and push.
4. Open a Pull Request.

---

## 🚀 Outcome

By completing this project, we achieved:

- **Real-Time Server Monitoring** – Successfully set up Prometheus to collect and store server metrics, ensuring visibility into CPU, memory, disk, and network usage.
- **Custom Dashboards** – Built interactive and visually appealing Grafana dashboards for quick performance insights.
- **Automated Alerts** – Configured alert rules in Prometheus Alertmanager to notify via email/Slack when system thresholds were breached.
- **Scalable & Modular Setup** – Designed the monitoring system to easily accommodate additional servers and services.
- **Improved Incident Response** – Reduced downtime by enabling proactive detection and faster troubleshooting of performance issues.
- **Open-Source Tooling** – Leveraged Prometheus, Grafana, and Alertmanager for a cost-effective monitoring solution without vendor lock-in.

This setup provides **continuous observability**, **early warning alerts**, and **better decision-making** for infrastructure performance and capacity planning.

