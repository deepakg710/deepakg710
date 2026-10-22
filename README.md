<div align="center">
  <p><code>SECURITY ENGINEERING PORTFOLIO</code></p>
  <h1>Deepak G.</h1>
  <p>
    <strong>Aspiring Red Team Operator | Active Directory Security | Network Security & Penetration Testing</strong>
  </p>

  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&pause=1200&color=00D9FF&center=true&vCenter=true&width=650&height=55&lines=Active+Directory+Security;Network+Security+%26+Topology+Analysis;PCAP+Packet+Forensics+%26+Analysis;Security+Tooling+in+Authorized+Labs" alt="Active Directory Security, Network Security, Packet Analysis, Security Tooling" />
  </a>
</div>

---

B.E. Computer Science and Engineering student at **Ballari Institute of Technology & Management (BITM)**, Karnataka, India (Class of 2027). I build defensive and offensive security tools, investigate network protocols, and practice hands-on cybersecurity in authorized lab environments.

- **TryHackMe:** [tryhackme.com/p/deepak710](https://tryhackme.com/p/deepak710)
- **Email:** [deepak710op@gmail.com](mailto:deepak710op@gmail.com)
- **Key Projects:** [NetSec-Analyzer](https://github.com/deepakg710/netsec-analyzer) · [AD-Monitor](https://github.com/deepakg710/AD-Monitor) · [NetTrace](https://github.com/deepakg710/NetTrace)

---

## Featured Projects

### 1. [NetSec-Analyzer](https://github.com/deepakg710/netsec-analyzer) — Cisco Network Security, Attack-Path & Resilience Analysis
Local-first platform that parses Cisco IOS configurations, evaluates security posture, and reconstructs network topology without external dependencies.
- **Topology & Attack Paths:** Automatically reconstructs L2/L3 topology graphs and models deterministic multi-hop attack paths across routing LPM and ACL boundaries.
- **Resilience Engine:** Graph-theoretic detection of Single Points of Failure (SPOFs) via NetworkX articulation points and missing redundant uplinks.
- **Auditing & Remediation:** CIS/NIST compliance scoring with line-numbered evidence, dual Beginner/Pro remediation views, and HTML/PDF report generation.
- **Stack:** Python 3.11+ (FastAPI, NetworkX, ReportLab), React 19, TypeScript, Tailwind CSS v4, `@xyflow/react`.

### 2. [AD-Monitor](https://github.com/deepakg710/AD-Monitor) — Active Directory Defensive Monitoring & Insider Threat Detection
Security monitoring and telemetry platform built for an enterprise Windows Active Directory lab (`lab.local`).
- **Telemetry Ingestion:** Ingests forwarded Windows Security & Defender events (`4624`, `4625`, `4688`, `5145`, `4104`) via native WEF.
- **Lineage & Traps:** Real-time process creation lineage trees, DPAPI-protected browser navigation auditing, and Canary file tripwires.
- **Anomaly Detection:** 19 deterministic detection rules paired with an Isolation Forest User Behavior Analytics (UBA) baseline engine.
- **Stack:** Python, FastAPI, SQLite, React, TypeScript, Tailwind CSS, Argon2id.

### 3. [NetTrace](https://github.com/deepakg710/NetTrace) — Offline PCAP/PCAPNG Packet Analysis & Forensics
Offline network protocol analysis tool for deep packet dissection and flow visualization.
- **Protocol Dissection:** Streaming Scapy parser decoding Frame, Ethernet II, ARP, IPv4/v6, TCP, UDP, ICMP, DNS, and TLS SNI with exact byte offsets.
- **Display Filters:** AST recursive-descent filter engine evaluating 27 protocol fields with boolean logic.
- **Explorer UI:** Wireshark-style 3-pane synchronized packet viewer and interactive endpoint communication topology graph.
- **Stack:** Python (Scapy, FastAPI), React, TypeScript, SQLite.

---

## Technical Skills

- **Security & Domains:** Active Directory Security, Windows Event Forwarding (WEF), Attack-Path Mapping, ACL Audit, MITRE ATT&CK.
- **Networking:** TCP/IP, Routing & Subnetting, OSPF, VLAN Trunking, PCAP Analysis, Wireshark, Scapy, Packet Dissection.
- **Languages & Frameworks:** Python, FastAPI, React 19, TypeScript, Vite, Tailwind CSS, SQL / SQLite, PowerShell, Bash.
- **Tools & Platforms:** Git, NetworkX, ReportLab, Docker, Hyper-V, Linux, Windows Server.

---

## Current Focus

- **Active Directory Lab:** Hypervisor-based Windows Server Domain Controller testing Kerberos authentication mechanics and BloodHound graph analysis.
- **Penetration Testing:** Practicing structured network enumeration, vulnerability validation, and technical documentation via TryHackMe paths.
