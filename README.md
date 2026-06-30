## Evidence & Screenshots

### 1. Docker Hardening Configuration


![Docker Daemon Hardened](screenshots/
docker-daemon-hardened.png)


*CIS Docker Benchmark controls: icc=false, no-new-privileges=true, userland-proxy=false*

### 2. DVWA SQL Injection Attack


![SQL Injection Attack](screenshots/dvwa-sql-injection-attack.png)


*Successful exploitation of SQL injection vulnerability: ' OR '1'='1 bypasses authentication*

### 3. TCPDump Traffic Capture


![Traffic Capture Running](screenshots/tcpdump-traffic-capture.png)


*Real-time packet capture on isolated Docker network*

### 4. Wireshark HTTP Payload Analysis


![Wireshark Payload](screenshots/wireshark-http-payload.png)


*HTTP POST request containing SQL injection payload captured in pcap file*

### 5. Network Isolation Test (Ping Failure)


![Ping Blocked](screenshots/ping-isolation-test.png)


*Monitor container cannot reach DVWA due to ICC (Inter-Container Communication) disabled*

### 6. Capture File Verification


![Pcap File](screenshots/lab-capture.png)


*Lab_capture.pcap successfully created on Kali host via docker cp*

### 7. Docker Network Inspection


![Network Details](screenshots/docker-network-inspect.png)


*Both containers connected to security-lab_security_lab_net with correct IPs*

## How to Reproduce This Lab

### Prerequisites
- Kali Linux with Docker installed
- 8GB RAM minimum
- 10GB free disk space

### Quick Start
```bash
git clone https://github.com/yourusername/docker-security-lab
cd docker-security-lab
docker-compose up -d
firefox http://127.0.0.1:8080
