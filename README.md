📘 Networking Basics for HLD/LLD & Interviews
1. 🌐 OSI Model (7 Layers)

The OSI (Open Systems Interconnection) model standardizes communication into 7 layers:

Physical Layer

Deals with hardware (cables, NIC, hubs).

Bits are transmitted as signals.

Data Link Layer

Responsible for MAC addressing and error detection.

Examples: Ethernet, Wi-Fi.

Network Layer

Handles routing, addressing (IP), packet forwarding.

Example protocols: IPv4, IPv6, ICMP.

Transport Layer

Ensures reliable delivery, segmentation, flow control.

Example protocols: TCP, UDP.

Session Layer

Manages sessions (start, maintain, terminate communication).

Example: NetBIOS, RPC.

Presentation Layer

Data translation, compression, encryption.

Example: SSL/TLS, JPEG, MPEG.

Application Layer

End-user services (email, file transfer, web).

Examples: HTTP, SMTP, IMAP, FTP, DNS.

👉 Interview Tip: Often asked: “Which layer does protocol X belong to?”

2. 🚦 TCP vs UDP

Transport Layer protocols (Layer 4).

TCP (Transmission Control Protocol)

Connection-oriented.

Reliable (acknowledgements, retransmissions).

Flow & congestion control.

Used for: HTTP/HTTPS, FTP, SSH, Email (SMTP, IMAP, POP3).

UDP (User Datagram Protocol)

Connectionless.

Faster but unreliable (no guarantee of delivery).

Lightweight, minimal overhead.

Used for: DNS, VoIP, Video Streaming, Online Gaming.

👉 Interview Question: “Why use UDP over TCP?”
Answer: Speed & low latency, where occasional loss is acceptable (e.g., video/audio calls).

3. 📧 Email Protocols

SMTP (Simple Mail Transfer Protocol)

Used to send emails.

Works with TCP (port 25/587).

IMAP (Internet Message Access Protocol)

Used to read emails from the server.

Keeps mail on server (syncs across devices).

TCP port 143 (or 993 for secure IMAPS).

POP3 (Post Office Protocol v3)

Downloads mail from server → deletes from server (older approach).

TCP port 110 (or 995 for secure POP3S).

👉 Comparison:

SMTP = Sending

IMAP = Reading + Sync

POP3 = Reading (one device, not synced)

4. ⚡ Other Key Networking Concepts

IP Addressing (IPv4/IPv6) – Uniquely identifies devices.

DNS (Domain Name System) – Resolves names (google.com → IP).

HTTP/HTTPS – Web communication. HTTPS adds encryption via TLS.

Firewalls & Load Balancers – Core components in HLD diagrams.

NAT (Network Address Translation) – Maps private → public IP.

Latency, Bandwidth, Throughput – Common performance metrics.

5. 🧩 Networking in HLD & LLD

When asked in HLD/LLD interviews, focus on:

How clients talk to servers (Protocols & Ports).

Security (TLS, Firewalls, VPNs).

Reliability (TCP vs UDP choice, retries).

Scalability (Load Balancers, CDNs, Caching).

Data flow (e.g., “User enters URL → DNS → TCP Handshake → HTTP Request”).


/////////////////////////////////////////////////
📂 FTP and Networking Protocols
1. 🔹 What is FTP?

FTP (File Transfer Protocol) is one of the oldest protocols used to transfer files between client and server over a network.

Works on Application Layer (Layer 7 of OSI).

Uses TCP ports 21 (command) and 20 (data transfer).

Examples: Uploading/downloading files from a server.

2. 🔐 Is FTP Secure?

Plain FTP is not secure – it sends username, password, and data in plain text.

Anyone sniffing the network (via Wireshark, tcpdump, etc.) can capture credentials and files.

Secure Alternatives:

FTPS (FTP Secure / FTP-SSL)

Adds SSL/TLS encryption to FTP.

Works on same ports but with encryption.

SFTP (SSH File Transfer Protocol)

Not FTP at all → It’s built on SSH (port 22).

Provides secure authentication & encryption.

Commonly used in enterprises.

👉 Interview Tip: If asked “Is FTP secure?” → Answer: No, plain FTP is insecure. Use FTPS or SFTP for secure file transfer.

3. 📡 How Many Networking Protocols Are There?

There are hundreds of protocols, but for Networking + HLD/LLD interviews, focus on the core ones:

🔸 Application Layer Protocols

HTTP / HTTPS – Web communication.

FTP / FTPS / SFTP – File transfer.

SMTP, IMAP, POP3 – Email.

DNS – Domain name resolution.

DHCP – Dynamic IP assignment.

SNMP – Network monitoring.

🔸 Transport Layer Protocols

TCP – Reliable, connection-based.

UDP – Fast, connectionless.

🔸 Network Layer Protocols

IP (IPv4, IPv6) – Addressing & routing.

ICMP – Error reporting, ping.

ARP – Maps IP → MAC address.

🔸 Security Protocols

SSL/TLS – Encryption for HTTPS, FTPS, IMAPs, etc.

IPSec – VPNs, secure tunneling.

SSH – Secure shell, also basis for SFTP.

4. 🧩 Quick Recap

FTP → Old, insecure → prefer SFTP or FTPS.

Protocols → Too many, but interviews care about:

HTTP/HTTPS, TCP/UDP, DNS, DHCP, FTP/SFTP, SMTP/IMAP, IP, ICMP, ARP.

Always map protocols to OSI layers in your answers.




