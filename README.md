# 🚀 LANCast  
### SDN-Based Offline LAN Screen Broadcasting System

---

## 📌 Overview

**LANCast** is a Software-Defined Networking (SDN) based one-to-many screen broadcasting system designed for offline Local Area Networks (LAN).

It enables a single broadcaster to stream their screen in real time to multiple receivers without requiring internet access.

The system integrates:
- Java for screen capture and streaming
- UDP Multicast for one-to-many communication
- Ryu SDN Controller for traffic optimization
- OpenFlow-enabled switches (Mininet for simulation)

---

## 🎯 Problem Statement

Traditional LAN streaming methods create multiple unicast streams, leading to:

- Network congestion  
- High bandwidth consumption  
- Increased latency  
- Packet loss under load  

An optimized solution is required to efficiently manage LAN broadcast traffic.

---

## 💡 Proposed Solution

LANCast leverages SDN to intelligently manage multicast traffic:

1. The broadcaster sends video frames using UDP multicast.
2. Receivers join the multicast group.
3. The SDN controller dynamically installs flow rules.
4. Switches forward packets efficiently without duplication.
5. Traffic prioritization ensures smooth real-time streaming.

---

## 🏗️ System Architecture

```
Broadcaster (Java App)
        |
        | UDP Multicast
        v
OpenFlow Switch  <---->  SDN Controller (Ryu)
        |
        v
Multiple Receivers (Java App)
```

---

## ⚙️ Technologies Used

- Java (Screen Capture & Networking)
- UDP Multicast
- Ryu SDN Controller (Python)
- OpenFlow Protocol
- Mininet (Network Simulation)
- Wireshark (Traffic Analysis)

---

## 🔄 How It Works

- Screen is captured and encoded by the broadcaster.
- Frames are transmitted via UDP multicast.
- Receivers subscribe to the multicast group.
- The SDN controller:
  - Detects multicast traffic
  - Installs optimized forwarding rules
  - Manages bandwidth efficiently
  - Reduces congestion and latency

---

## 🧪 Testing Environment

- Mininet simulated topology
- 1 Broadcaster
- 3+ Receivers
- 1 OpenFlow Switch
- 1 Ryu Controller

---

## 📊 Key Features

- Offline operation (No Internet Required)
- One-to-many streaming
- Efficient bandwidth utilization
- Centralized SDN control
- Scalable architecture
- Real-time screen broadcasting

---

## 🚀 Future Enhancements

- Adaptive bitrate streaming
- H.264/H.265 compression
- Authentication & access control
- Web-based monitoring dashboard
- Deployment on real OpenFlow hardware

---

## 👨‍💻 Team Structure

- Streaming Module Development
- SDN Controller Implementation
- Network Simulation & Testing
- Documentation & Deployment

---

## 📌 Use Cases

- Smart Classrooms
- College Laboratories
- Seminar Halls
- Campus Broadcasting
- Corporate Training Rooms

---

## 📚 Learning Outcomes

This project demonstrates:

- Practical SDN implementation
- OpenFlow-based traffic management
- Multicast networking concepts
- Real-time multimedia streaming
- Network optimization techniques

---

## 📜 License

This project is developed for academic and research purposes.
