<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/b5b5314d-d0c9-47bd-8d05-aa1b30f3fea8" />

# 🛰️ NetPractice

📌 **Overview**
NetPractice is a core project from the **42 curriculum** designed to teach and test your understanding of **computer networking fundamentals**. Instead of coding, this project uses an **interactive learning platform** where you configure small networks (IP addressing, routing, masks, subnets, gateways) until every machine can reach its target.

Through practical exercises, you’ll build a solid foundation in how data actually flows across networks — knowledge that underpins everything from local LAN setups to the global Internet.

---

## ✨ Features of the Project

* 🌐 Configure **IPv4 addressing** across multiple subnets
* 🛣️ Set up **default gateways** and **routing tables**
* 🎯 Learn to calculate and assign **subnet masks**
* 🧮 Understand **binary/decimal IP conversion**
* 📡 Troubleshoot and fix broken connectivity step by step
* 🔗 Visualize how packets travel across a network
* 🧭 Develop intuition for **OSI vs TCP/IP model layers**

---

## 🧠 Networking Concepts You’ll Learn

### 1. **IP Addressing**

* An IP address identifies a device on a network.
* Written in **dotted decimal notation** (e.g., `192.168.1.10`).
* Consists of:

  * **Network part**: identifies the subnet.
  * **Host part**: identifies the device inside that subnet.

➡️ Example: `192.168.1.10/24`

* `/24` means the first 24 bits are the **network**.
* Network = `192.168.1.0`, Host = `.10`

---

### 2. **Subnet Masks**

* A mask defines how many bits belong to the network.
* Example masks:

  * `/24` → 255.255.255.0 → 254 usable hosts
  * `/30` → 255.255.255.252 → 2 usable hosts (for point-to-point links)

➡️ Subnetting lets you split a large network into smaller, efficient ones.

---

### 3. **Routing & Gateways**

* A **router** connects multiple networks.
* Each machine can only talk directly to devices **on the same subnet**.
* To reach outside, it must send traffic to a **gateway** (usually the router).

➡️ Example:

* PC A: `10.0.1.5/24`, Gateway = `10.0.1.1`
* Destination = `10.0.2.5/24`
* PC A sends to `10.0.1.1` (router), which forwards to `10.0.2.5`.

---

### 4. **Private vs Public IPs**

* **Private ranges**:

  * `10.0.0.0/8`
  * `172.16.0.0/12`
  * `192.168.0.0/16`
* Used for internal networks, not routable on the Internet.
* **Public IPs** are globally unique and reachable over the Internet.

---

### 5. **The OSI & TCP/IP Models**

* **Layers of communication**:

  * Physical → Data Link → Network → Transport → Application
* In NetPractice you mainly focus on the **Network layer** (IP addresses, routes) but you’ll understand how it interacts with:

  * **Transport layer** (TCP/UDP ports)
  * **Data Link layer** (MAC addresses)

---

### 6. **Common Pitfalls You’ll Learn to Fix**

* Wrong subnet mask → devices think they’re in the same network when they’re not.
* No default gateway → can’t reach outside the local subnet.
* Overlapping subnets → routing confusion.
* Misconfigured routes → packets get lost.

---

## 📜 What the Project Covers

* 🧮 **Subnetting math** (binary & CIDR notation)
* 🖧 **Building networks from scratch**
* 🛣️ **Understanding routing logic** (longest prefix match)
* 🧭 **Debugging misconfigurations** (step-by-step testing)

---

## ▶️ How to Use

1. Log into the NetPractice platform provided by 42.
2. Complete levels in order — each introduces a new concept (IP assignment, subnetting, routing, multiple routers, etc.).
3. Verify connectivity by **pinging targets** in the UI.

---

## 🧪 Example Exercise

1. PC1 → IP: `192.168.1.2/24`
2. PC2 → IP: `192.168.1.3/24`
   ✅ Both can ping each other (same subnet).

If PC2 is instead `10.0.0.2/24`:
❌ No direct connection.
➡️ You must add a **router** with:

* Interface1: `192.168.1.1/24`
* Interface2: `10.0.0.1/24`
  Then set gateways on both PCs.

---

## 💡 Tips

* Always check:

  * **IP addresses**
  * **Subnet masks**
  * **Default gateways**
* Convert between **binary & decimal** to see how subnets work.
* Use `/30` subnets for router-to-router links (efficient).
* Think of the **network as a map**: every device must know *how* to reach its destination.

---

## 🛠️ Technical Constraints

* No coding, all configuration is **manual logic**.
* Must fully understand **why** each fix works.
* Solutions should follow **best networking practices**.

---

## 🚀 Why It Matters

By finishing NetPractice, you’ll:

* Build confidence in real-world networking.
* Be able to configure LANs, routers, and troubleshoot IP issues.
* Gain a foundation that helps for future **DevOps, SysAdmin, and Cloud engineering** paths.

