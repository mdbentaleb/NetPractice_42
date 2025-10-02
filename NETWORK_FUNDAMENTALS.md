
# 🌐 Computer Network Fundamentals

---

## 📌 What is a Network?

A **computer network** is a collection of interconnected devices — such as **computers, servers, routers, and switches** — that communicate with each other to **share data and resources**.

---

## 🖧 Types of Computer Networks

### 📍 By Geographic Scope

1. **PAN (Personal Area Network)**

   * Very small area (~10–15 meters).
   * Used for connecting personal devices like smartphones, laptops, headphones.
   * Example: Bluetooth connection between phone and wireless earbuds.

2. **HAN (Home Area Network)**

   * Connects devices inside a **home**.
   * Example: Wi-Fi router connecting PCs, smart TVs, phones, IoT devices.

3. **LAN (Local Area Network)**

   * Connects devices in a **limited area** (office, campus, building).
   * Example: Company office network sharing printers and files.

4. **CAN (Campus Area Network)**

   * Connects **multiple LANs** in a campus (university, corporate).
   * Example: University connecting faculty buildings together.

5. **MAN (Metropolitan Area Network)**

   * Covers a **city or large campus**.
   * Larger than LAN, smaller than WAN.
   * Example: City-wide Wi-Fi or interconnecting multiple offices.

6. **WAN (Wide Area Network)**

   * Covers **large geographic areas** (country, continent).
   * The **Internet** is the biggest WAN.

7. **GAN (Global Area Network)**

   * Spans multiple countries, connecting multiple WANs.
   * Example: International corporation’s private global network.

---

### ⚙️ Specialized Networks

1. **SAN (Storage Area Network)** – high-performance storage sharing in data centers.
2. **EPN (Enterprise Private Network)** – secure networks managed by large organizations.
3. **VPN (Virtual Private Network)** – encrypted tunnel over public Internet.

---

## 🔗 Network Topologies

1. **Bus Topology** – all devices share a single cable (cheap, but collisions happen).
2. **Star Topology** – all devices connect to a central switch/hub (easy to manage).
3. **Ring Topology** – devices connected in a circle, data flows one way.
4. **Mesh Topology** – every device connected to every other device (high redundancy).
5. **Hybrid Topology** – combination of two or more (e.g., star + bus).

---

## 📡 Network Devices

* **Router** – connects networks, forwards packets using routing tables.
* **Switch** – connects devices inside a LAN, forwards frames using MAC addresses.
* **Hub** – basic device, broadcasts to all ports (inefficient).
* **Modem** – converts analog ↔ digital signals for Internet access.
* **Access Point** – provides Wi-Fi to extend wired LAN.
* **Firewall** – filters traffic based on rules.
* **IDS/IPS** – detect or block suspicious network activity.

---

## 📜 Network Protocols

1. **TCP/IP** – foundation of the Internet (transmission + addressing).
2. **HTTP/HTTPS** – web browsing, HTTPS adds encryption.
3. **FTP** – file transfer.
4. **SMTP/POP3/IMAP** – sending & receiving emails.
5. **DNS** – translates domain names → IP addresses.
6. **DHCP** – automatically assigns IP addresses to devices.
7. **SNMP** – monitoring and managing devices.

---

## 🧮 Example: IP Addressing & Subnet Masks

Suppose we have:

```
PC1
IP Address: 104.95.23.12
Subnet Mask: 255.255.255.0 (/24)
```

* Network address = **104.95.23.0**
* Broadcast address = **104.95.23.255**
* Valid host range = **104.95.23.1 → 104.95.23.254**

Now add:

```
PC2
IP Address: 104.95.23.50
Subnet Mask: 255.255.255.0 (/24)
```

✅ Both PCs are in the same network → they can communicate **directly**.

---

If instead PC2 is:

```
PC2
IP Address: 104.95.24.10
Subnet Mask: 255.255.255.0 (/24)
```

❌ They are on **different networks** (`104.95.23.0/24` vs `104.95.24.0/24`).
➡️ You need a **router** (with interfaces in both networks) and set **gateways** for the PCs.

---

## 🛣️ Gateway Example

* **Router**:

  * Interface1: `104.95.23.1/24`
  * Interface2: `104.95.24.1/24`

* **PC1 Gateway** = `104.95.23.1`

* **PC2 Gateway** = `104.95.24.1`

✅ Now PC1 ↔ PC2 communication works via router.

---

## 🎯 Why Learn This?

* You’ll understand the **logic behind IP networks**, routing, and communication.
* These fundamentals are the **backbone of DevOps, Cloud, SysAdmin, Cybersecurity, and Infrastructure engineering**.
* NetPractice at 42 teaches you **by solving real network problems**, not just reading theory.

---
