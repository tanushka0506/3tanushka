# 3tanushka
# Network Intrusion Detection System (NIDS) Using Snort

## 📜 Project Overview
This repository contains a Network Intrusion Detection System (NIDS) built using Snort. The system monitors network traffic, detects potential threats, and logs alerts based on predefined rules.

## 📂 Project Structure
- `snort.conf`: Snort configuration file.
- `rules/`: Directory containing custom Snort rules.
- `alerts.log`: Log file storing detected alerts.
- `README.md`: Project documentation (this file).

## 🛠️ Installation and Setup
### 📌 **1. Install Snort:**
```bash
sudo apt update
sudo apt install snort -y
```

### 📌 **2. Configure Snort:**
- Edit `snort.conf` to set the network range and logging options.
- Add custom rules to the `rules/local.rules` file.

### 📌 **3. Run Snort:**
```bash
sudo snort -A console -q -c /etc/snort/snort.conf -i eth0
```
- `-A console`: Displays alerts on the console.
- `-q`: Quiet mode.
- `-c`: Specifies the configuration file.
- `-i`: Selects the network interface.

## 📝 Example Rule
Detect HTTP traffic on port 80:
```bash
alert tcp any any -> any 80 (msg:"HTTP traffic detected"; sid:1000001;)
```


