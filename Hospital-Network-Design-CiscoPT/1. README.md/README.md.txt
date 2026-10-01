# Hospital Network Design (Cisco Packet Tracer)

## 📌 Project Overview
This project designs a hospital network connecting five departments:
- Laboratory
- Pharmacy
- Emergency
- Administration
- IT

Each department has its own subnet, DHCP server, and reliable communication setup. Administration hosts Web, Email, and DNS servers. Routing is configured using OSPF.

---

## 🖼️ Topology Diagram
![Hospital Network Topology](Docs/topology_diagram.png)

---

## 📊 Subnetting Plan
- Assigned block: 172.31.50.0/24
- Divided into 5 equal subnets:
  - Lab: 172.31.50.0/27
  - Pharmacy: 172.31.50.32/27
  - Emergency: 172.31.50.64/27
  - Administration: 172.31.50.96/27
  - IT: 172.31.50.128/27

Inter-router links use /30 subnets.

---

## ⚙️ Routing Protocol
- **OSPF** selected for scalability and efficient routing updates.  
- Justification: OSPF supports hierarchical design and is better for future expansion compared to RIP.

---

## 🔧 Features Implemented
- DHCP for automatic IP assignment  
- DNS for name resolution  
- Email & Web servers in Administration  
- OSPF dynamic routing  
- Structured subnetting with clear host ranges  

---

## 🚀 How to Run
1. Open `hospital_network.pkt` in Cisco Packet Tracer (version 8.x recommended).  
2. Verify DHCP assignment in each department.  
3. Test inter-department communication using `ping`.  
4. Access Web and Email servers from client PCs.  

---

## ⚠️ Limitation & Solution
- **Limitation:** Single point of failure at core router.  
- **Solution:** Add redundancy using HSRP or additional backup router.  

---

## 👨‍💻 Author
- Md. Habibul Islam, Southeast University, CSE Department, Bangladesh
