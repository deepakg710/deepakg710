# Deepak G.

**Aspiring Red Team Operator | Active Directory Security | Network Penetration Testing**

B.E. in Computer Science and Engineering student at **Ballari Institute of Technology & Management (BITM)**, Karnataka, India (graduating in 2027).

I build security-focused software and practice cybersecurity in authorized lab environments. My current focus is developing practical skills in **Active Directory security**, **Windows internals and auditing**, **network enumeration**, **packet-level traffic analysis**, and **attack-path methodology**—using hands-on engineering to understand both how attacks operate on the wire/endpoint and what telemetry they leave behind.

- **GitHub:** [github.com/deepakg710](https://github.com/deepakg710)
- **TryHackMe:** [tryhackme.com/p/deepak710](https://tryhackme.com/p/deepak710)
- **Projects:** [AD-Monitor](https://github.com/deepakg710/AD-Monitor) · [NetTrace](https://github.com/deepakg710/NetTrace)
- **Email:** [deepak710op@gmail.com](mailto:deepak710op@gmail.com)

---

## Projects

### 1. [AD-Monitor](https://github.com/deepakg710/AD-Monitor) — Defensive Security Monitoring & Insider-Threat Detection
A defensive security-monitoring and investigation platform built for a controlled Windows Active Directory lab environment (`lab.local`). Building this project provided direct visibility into how Windows Security Event IDs, process creation trees, and behavioral baselines record endpoint and domain activity.

- **Implemented & Verified Capabilities:**
  - **Windows Event Forwarding (WEF) Ingestion:** Normalizes forwarded Windows Security and Defender XML events (`4624`, `4625`, `4656`, `4663`, `4688`, `4689`, `5145`, `1116`, `4104`) with domain SID and host attribution.
  - **Read-Only Endpoint Process Telemetry:** PowerShell collector capturing process snapshots, parent-child lineage, CPU deltas, Authenticode status, SHA-256 hashes, and regex command-line token redaction.
  - **Privacy-Preserving Browser Telemetry:** Chromium Manifest V3 extension and DPAPI-protected Native Messaging host recording top-level domain navigations (stripping paths, queries, and credentials) and download SHA-256 lifecycle revisions.
  - **Event Correlation & Detection:** Investigation Timeline linking domain visits, file downloads, and process execution; 19 deterministic detection rules (canary access, staging/archiving, encoded PowerShell, repeated failed logons); and a CPU-based Isolation Forest UBA model with a 48-window cold-start gate (`Collecting baseline`).
  - **Authentication & Security Controls:** Argon2id password hashing, mandatory unique 12+ character administrator passphrase on initial setup, default-password blocklist, HTTP-only session cookies, and CSRF validation.
  - **Verification:** `27 passed` automated `pytest` unit and integration tests (`tests/`).
- **Planned (Not Yet Implemented):**
  - Sysmon `Event ID 3` network connection ingestion, Sigma rule YAML import/export, and cross-workstation lateral movement graph visualization.

---

### 2. [NetTrace](https://github.com/deepakg710/NetTrace) — Offline PCAP/PCAPNG Analysis & Network Investigation Tool
An offline packet-capture analysis and network-troubleshooting application built with FastAPI, Scapy, SQLite, React, and TypeScript to inspect protocol headers, filter packet streams, and map observed endpoint communications.

- **Implemented & Verified Capabilities:**
  - **Packet & Protocol Dissection:** Streaming Scapy `PcapReader` parser validating magic bytes and extracting Frame, Ethernet II, ARP, IPv4/IPv6, TCP, UDP, ICMP, DNS, HTTP, and TLS SNI metadata with byte offsets and hex dumps.
  - **Display-Filter Engine:** Safe tokenizer and recursive-descent AST parser (no `eval`/`exec`) supporting 27 L2–L7 fields (`ip.addr`, `ip.src`, `ip.dst`, `tcp.port`, `udp.port`, `tcp.flags.syn`, `tcp.flags.reset`, `frame.number`, `frame.len`, `dns.qry.name`, logical `&&`, `||`, `!`, and parentheses) across backend and frontend. *(Implements a focused subset of display-filter syntax rather than full Wireshark dissector parity.)*
  - **3-Pane Packet Explorer & Communication Topology:** Synchronized packet list, expandable protocol layer tree, and hex/ASCII byte viewer; force-directed and grouped communication topology graph separating observed L3/L4 flows from inferred L2 relationships (`inferred=true` with documented `basis`).
  - **Traffic Diagnostics & Reporting:** Heuristic detection for TCP SYN port scans, host sweeps, connection resets (`RST`), incomplete handshakes, and DNS `NXDOMAIN`/`SERVFAIL`/unanswered queries, with HTML, ReportLab PDF, JSON, and CSV exports.
  - **Verification:** `12 passed` backend `pytest` tests and `10 passed` frontend `vitest` tests (`.\scripts\verify.ps1`).
- **Planned / Scope Boundaries:**
  - Offline `.pcap`/`.pcapng` analysis only (live interface packet sniffing is out of scope by design). CIDR subnet filter notation (`192.168.1.0/24`) and TCP stream payload reassembly are planned.

---

## Skills & Technical Areas

- **Networking:** TCP/IP fundamentals, three-way handshakes, RST/retransmission behavior, ARP, DNS resolution (`A`, `NXDOMAIN`, `SERVFAIL`), HTTP/TLS metadata, and subnetting.
- **Windows and Active Directory:** Windows Security Auditing (`4624`, `4625`, `4656`, `4663`, `4688`, `4689`, `5145`), Windows Event Forwarding (WEF), domain SIDs, process creation lineage, Windows DPAPI, and Active Directory enumeration & attack-path concepts *(developing)*.
- **Security monitoring and investigation:** Multi-source event correlation, deterministic detection rule design, failed-logon & port-scan heuristics, evidence boundary documentation, and case triage workflows.
- **Network analysis:** Offline `.pcap`/`.pcapng` dissection with Scapy and Wireshark, display-filter construction, L4 flow state analysis, and endpoint communication mapping.
- **Operating systems:** Windows 10/11, Windows Server (Active Directory lab administration), and Linux command-line workflows *(developing)*.
- **Development tools and technologies:** FastAPI, SQLAlchemy, Pydantic, SQLite (WAL mode & reversible migrations), React, TypeScript, Vite, Tailwind CSS, Argon2id authentication, Pytest, Vitest, Git, and GitHub Actions.
