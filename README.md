# Wireshark TLS Traffic Analysis

## Project Overview
This project analyzes network traffic using Wireshark to understand TLS handshakes, encrypted communication, TCP behavior, and network troubleshooting indicators.

## Objectives
- Capture and inspect live network traffic.
- Analyze TLS handshake messages.
- Identify Client Hello and Server Hello exchanges.
- Examine Server Name Indication (SNI).
- Understand encrypted application data.
- Review protocol hierarchy, endpoints, and TCP conversations.
- Identify retransmissions, duplicate ACKs, and connection resets.

## Tools Used
- Wireshark
- Windows 11
- Display filters and packet analysis

## Analysis Performed

### 1. TLS Handshake Analysis
Inspected TLS handshake messages, including:
- Client Hello
- Server Hello
- Certificate
- Change Cipher Spec
- Encrypted Application Data

### 2. TLS Protocol Inspection
Observed TLS 1.2 and TLS 1.3 traffic in the capture.

The Client Hello included the SNI hostname `api.jobright.ai`. The Server Hello advertised TLS 1.3 support and selected the TLS_AES_256_GCM_SHA384 cipher suite.

### 3. Encrypted Traffic
Inspected encrypted application data exchanged between client and server. Application payloads were not readable without the necessary session secrets.

### 4. TCP Stream Analysis
Used TCP stream filtering and conversation statistics to inspect:
- Source and destination ports
- Connection establishment
- Data exchange
- Connection termination

### 5. Protocol Hierarchy and Endpoints
Reviewed protocol distribution and endpoint statistics.

The capture contained 2,060 packets, including 684 TLS packets in the protocol hierarchy view.

### 6. Expert Information
Reviewed Wireshark diagnostic indicators, including:
- DNS retransmissions
- Missing DNS responses
- TCP duplicate acknowledgments
- Partial acknowledgments
- Connection resets
- QUIC decryption warnings

These indicators are troubleshooting observations and do not independently establish malicious activity.

## Key Learning Outcomes
- Understanding TLS handshake communication.
- Recognizing TLS versions and cipher suites.
- Understanding SNI and encrypted application traffic.
- Using Wireshark display filters.
- Analyzing TCP streams and network endpoints.
- Interpreting network troubleshooting indicators.

## Repository Structure
```text
Wireshark-TLS-Traffic-Analysis/
├── README.md
├── captures/
│   └── tls-handshake-analysis.pcapng
└── screenshots/
    └── [Wireshark analysis screenshots]
```

## Disclaimer
This project was conducted for educational purposes using network traffic captured on my own system. IP addresses, hostnames, and other network details are included only to explain the observed traffic.