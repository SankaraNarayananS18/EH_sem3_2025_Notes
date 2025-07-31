# EH_sem3_2025_Notes
# 🔍 Network Service Scan Report: scanme.nmap.org

## 1. Introduction

As a **security analyst**, our objective was to assess a publicly accessible host (`scanme.nmap.org`) to identify the **running network services** using Nmap. This domain is officially provided by the Nmap Project for learning and testing purposes (permission granted).

We conducted both **TCP and UDP scans** to understand how different protocols expose services and how the host responds to different scanning techniques.

---

## 2. TCP vs UDP Explanation

| Feature            | TCP (Transmission Control Protocol) | UDP (User Datagram Protocol)        |
|--------------------|--------------------------------------|-------------------------------------|
| Connection         | Connection-oriented                  | Connectionless                      |
| Reliability        | Reliable (ensures delivery)          | Unreliable (no delivery guarantee)  |
| Overhead           | Higher due to 3-way handshake        | Lower (no handshake)                |
| Use Cases          | Web, SSH, FTP, Email                 | DNS, Streaming, VoIP                |
| Packet Order       | Maintains packet order               | Packets may arrive out of order     |
| Speed              | Slower but reliable                  | Faster but prone to packet loss     |

- **TCP** uses a 3-way handshake (`SYN`, `SYN-ACK`, `ACK`) to establish a connection — similar to placing a phone call.
- **UDP** sends datagrams without establishing a session — similar to mailing a letter with no receipt.

---

## 3. Methodology

We used **Nmap (Network Mapper)** to perform the scan.

### 🔧 Tools Used

- **Tool:** Nmap  
- **Target:** `scanme.nmap.org`  
- **Environment:** Kali Linux (or equivalent Linux environment)

## 4. Screenshots

### 🖼️ TCP Scan Screenshot

This screenshot shows the result of running a TCP SYN scan on `scanme.nmap.org`.

![WhatsApp Image 2025-07-31 at 12 36 36_34e71861](https://github.com/user-attachments/assets/f011c17a-7b45-4cc5-938a-0904eea888b7)


---

### 🖼️ UDP Scan Screenshot

This screenshot shows the result of running a UDP scan on `scanme.nmap.org`.

![WhatsApp Image 2025-07-31 at 12 39 44_488460b7](https://github.com/user-attachments/assets/bd95d7a3-f08f-4215-8953-c3496f59c2c9)



### 📜 Commands Used

```bash
# TCP SYN Scan (default)
nmap scanme.nmap.org

# UDP Scan
sudo nmap -sU scanme.nmap.org



