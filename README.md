# 🔌 Router-to-Router Connection Guide (Cisco Packet Tracer)

This guide walks you through the process of connecting two Cisco routers using Cisco Packet Tracer, configuring IP addresses on their interfaces, and verifying connectivity using CLI and screenshots.

---

## 📂 Folder Structure

Router-to-Router-Connection-Guide/ ├── README.md ├── configs/ │   ├── Router0.txt │   └── Router1.txt ├── screenshots/ │   

---

## 🧰 Requirements

- Cisco Packet Tracer (version 7.2 or later)
- Basic understanding of router interfaces and IP configuration
- Two Cisco 2911 routers in simulation
- Copper cross-over cable for router-to-router connection

---

## 📡 Network Topology

[Router0] <--- crossover cable ---> [Router1] GigabitEthernet 0/0: 10.0.0.1/8                  GigabitEthernet 0/0: 10.0.0.2/8

---

## ⚙ Configuration Steps

### 🔧 Router0

#### Using CLI:

```bash
enable
configure terminal
hostname Router0
interface gigabitEthernet 0/0
ip address 10.0.0.1 255.0.0.0
no shutdown
exit
exit
write memory
```

> This config is saved in: configs/Router0.txt




---

##🔧 Router1

Using CLI:

```bash
enable
configure terminal
hostname Router1
interface gigabitEthernet 0/0
ip address 10.0.0.2 255.0.0.0
no shutdown
exit
exit
write memory
```
> This config is saved in: configs/Router1.txt




---

🧪 Testing Connectivity

After configuring both routers, test the connection with a ping command:

ping 10.0.0.1    # From Router0
ping 10.0.0.2    # From Router1

If the ping is successful, the routers are correctly connected and communicating.

See the screenshots in the screenshots/ folder for visual verification.


---
🧰 Troubleshooting Tips

Issue	Possible Cause	Solution

No ping response	Interfaces are down	Ensure no shutdown is used
Wrong IP address	Misconfigured IP	Re-check the CLI commands
IP conflict	Same IP on both routers	Assign unique IPs



---

📘 Author

Created by VikashChoudhary-04

Cyber Security Enthusiast


---

📝 License

This project is licensed under the MIT License.

---

## Download Packet Tracer File

You can download the complete simulation and open it in Cisco Packet Tracer:

[configuration.pkt](./configuration.pkt)
