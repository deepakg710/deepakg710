<div align="center">
  <p><code>SECURITY ENGINEERING PORTFOLIO</code></p>
  <h1>Deepak G.</h1>
  <p><strong>Aspiring Red Team Operator</strong><br />
  Active Directory Security · Network Forensics · Windows Security</p>

  <a href="https://github.com/deepakg710">
    <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&size=20&pause=1000&color=00D9FF&center=true&vCenter=true&width=500&lines=Active+Directory+Security;Network+Forensics+%26+Packet+Analysis;Building+Security+Tools+in+Authorized+Labs" alt="Typing SVG: Active Directory Security | Network Forensics & Packet Analysis | Building Security Tools in Authorized Labs" />
  </a>
</div>

---

**Aspiring Red Team Operator | Active Directory Security | Network Penetration Testing**

B.E. Computer Science and Engineering student at **Ballari Institute of Technology & Management (BITM)**, Karnataka, India (graduating in 2027). I build security-focused software and practice cybersecurity in authorized lab environments. My current focus is Active Directory security, Windows auditing, network enumeration, packet-level traffic analysis, and understanding how security events can be correlated during investigations.

- **GitHub:** [github.com/deepakg710](https://github.com/deepakg710)
- **TryHackMe:** [tryhackme.com/p/deepak710](https://tryhackme.com/p/deepak710)
- **Projects:** [AD-Monitor](https://github.com/deepakg710/AD-Monitor) · [NetTrace](https://github.com/deepakg710/NetTrace)
- **Email:** [deepak710op@gmail.com](mailto:deepak710op@gmail.com)

---

## Featured Projects

### 1. [AD-Monitor](https://github.com/deepakg710/AD-Monitor) — Defensive Security Monitoring & Insider-Threat Detection

A defensive security monitoring and investigation platform built for a controlled Windows Active Directory laboratory environment (`lab.local`). Building this system provided hands-on visibility into how Windows Security Event IDs, process creation trees, and behavioral baselines record endpoint and domain activity during an investigation.

- **Telemetry Ingestion & Normalization:**
  - Ingests forwarded Windows Security and Defender XML events via native Windows Event Forwarding (WEF).
  - Normalizes Event IDs `4624`, `4625` (logon / failed logon), `4656`, `4663` (file access / permission denied), `4688`, `4689` (process creation / termination), `5145` (network share object access), `1116` (Defender malware detection), and `4104` (PowerShell script block logging) with Windows Domain SID (`S-1-5-21-...`) and source workstation attribution.
- **Endpoint & Browser Collection:**
  - **Read-Only Process Telemetry:** Lightweight PowerShell agent collecting process snapshots, parent-child lineage trees, CPU deltas, Authenticode signature verification, SHA-256 binary hashes, and regex-based command-line credential/token redaction.
  - **Privacy-Preserving Browser Telemetry:** Chromium Manifest V3 extension and Windows DPAPI-protected Native Messaging host recording domain-only navigation (stripping full paths, query strings, and credentials) and download SHA-256 lifecycle revisions.
- **Correlation & Anomaly Detection:**
  - **Investigation Timeline:** Correlates disparate multi-sensor events (`domain visit → file download → process execution → child process`) with explicit *"What This Evidence Proves"* and *"What It Does Not Prove"* boundaries.
  - **Detection Engines:** 19 deterministic rules (canary file access, staging and archiving, encoded PowerShell, repeated failed logon counters) and a pure-Python Isolation Forest User Behavior Analytics (UBA) model with a 48-window baseline collection gate (`Collecting baseline`).
- **Security Controls & Verification:**
  - Argon2id password hashing, mandatory unique 12+ character administrator passphrase on initial setup, default-password blocklist, HTTP-only session cookies, and CSRF token protection.
  - **Test Suite:** `27 passed` automated unit and integration tests across database migrations, event normalization, detection rules, UBA calculations, and API security (`python -m pytest -v`).
- **Planned (Not Yet Implemented):**
  - Microsoft Sysmon `Event ID 3` network connection ingestion, automated Sigma rule YAML import/export utility, and cross-workstation lateral movement graph visualization.

---

### 2. [NetTrace](https://github.com/deepakg710/NetTrace) — Offline PCAP/PCAPNG Analysis & Network Investigation Tool

An offline packet-capture analysis and network-troubleshooting application built with FastAPI, Scapy, SQLite, React, and TypeScript to inspect protocol headers, filter packet streams, and reconstruct observed endpoint communications.

- **Streaming Packet Dissection:**
  - Streaming Scapy `PcapReader` parser with magic-byte validation (`\xd4\xc3\xb2\xa1`, `\xa1\xb2\xc3\xd4`, `\x0a\x0d\x0d\x0a`).
  - Decodes Frame, Ethernet II, ARP, IPv4/IPv6, TCP, UDP, ICMP, DNS, HTTP, and TLS SNI metadata with exact byte offsets (`byte_start`, `byte_end`) and synchronized hex/ASCII view.
- **Display-Filter Engine:**
  - Safe tokenizer and recursive-descent AST parser (zero `eval` or `exec`) supporting 27 L2–L7 fields (`ip.addr`, `ip.src`, `ip.dst`, `tcp.port`, `udp.port`, `tcp.flags.syn`, `tcp.flags.reset`, `frame.number`, `frame.len`, `dns.qry.name`, `dns.rcode`, etc.) with logical `&&`, `||`, `!`, and parentheses across backend and frontend.
  - *Documented Limitation:* Implements a focused subset of display-filter syntax rather than full Wireshark dissector parity.
- **Three-Pane Packet Explorer & Communication Topology:**
  - Wireshark-style synchronized packet table, expandable protocol layer tree, and hex/ASCII byte viewer with byte offset highlighting.
  - Interactive force-directed and grouped communication topology graph separating observed L3/L4 flows from inferred L2 links (`inferred=true` with explicit `basis` strings).
- **Diagnostics, Reporting & Verification:**
  - Heuristic detection for TCP SYN port scans, host sweeps, connection resets (`RST`), incomplete handshakes, and DNS `NXDOMAIN`/`SERVFAIL`/unanswered queries.
  - Standalone HTML, ReportLab PDF, structured JSON, and filtered CSV exports.
  - **Test Suite:** `12 passed` backend `pytest` tests + `10 passed` frontend `vitest` tests (`.\scripts\verify.ps1`).
- **Planned / Scope Boundaries:**
  - Offline `.pcap`/`.pcapng` analysis only (live network interface packet sniffing is out of scope by design). CIDR subnet filter notation (`192.168.1.0/24`) and TCP stream payload reassembly are planned.

---

### 3. Active Directory Red Team Lab — Planned

> **Status:** Planned project (not yet built or executed).

The goal of this upcoming project is to construct an isolated Windows domain laboratory environment containing a Windows Server Domain Controller and client workstations, then document structured, authorized security-testing exercises from initial enumeration through defensive remediation. All exercises will be conducted strictly within self-owned, isolated virtual machines.

- **Planned Learning Objectives:**
  - Domain and user enumeration
  - Controlled misconfiguration discovery
  - Authorized attack-path testing
  - Privilege-boundary analysis
  - Evidence collection and reproducibility
  - Defensive remediation and validation
- **Planned Deliverables:**
  - Lab architecture diagram
  - Setup and configuration guide
  - Sanitized commands and outputs
  - Evidence-backed findings report
  - Risk and impact explanations
  - Remediation and validation steps
  - Screenshots of actual lab results

---

## Skills & Technical Areas

- **Networking:** TCP/IP fundamentals, three-way handshakes, connection reset (`RST`) and retransmission behavior, ARP, DNS resolution and failure codes (`A`, `NXDOMAIN`, `SERVFAIL`), HTTP/TLS metadata, subnetting, and routing fundamentals.
- **Windows & Active Directory:** Windows Security Auditing, Windows Event Forwarding (WEF), domain SIDs, process creation lineage, Windows DPAPI, and Active Directory security & attack-path concepts *(developing)*.
- **Security Monitoring & Investigation:** Multi-source event correlation, deterministic detection rule design, behavioral baselines, alert triage, evidence collection, and investigation workflows.
- **Network Analysis:** PCAP/PCAPNG analysis, Scapy, display-filter construction, protocol inspection, L4 flow state analysis, and endpoint communication mapping.
- **Operating Systems:** Windows 10/11, Windows Server lab administration, and Linux command-line workflows *(developing)*.
- **Development Tools & Technologies:** Python, FastAPI, SQLAlchemy, Pydantic, SQLite (WAL mode & reversible migrations), React, TypeScript, Vite, Tailwind CSS, Argon2id, pytest, Vitest, Git, and GitHub Actions.

---

## Current Learning Roadmap

- **Active Directory Lab Construction:** Provisioning an isolated hypervisor environment with a Windows Server 2022 Domain Controller and Windows 10/11 client VMs to practice domain configuration, security auditing, and Group Policy management.
- **Active Directory Attack-Path Analysis:** Studying Kerberos mechanics (AS-REQ/AS-REP pre-authentication, TGS requests, ticket granting), Service Principal Name (SPN) discovery, BloodHound/SharpHound graph analysis concepts, and defensive detection signatures.
- **Network Penetration Testing Discipline:** Practicing structured network enumeration, port/service identification, protocol-level vulnerability validation, and sanitized technical reporting.
- **Authorized Hands-On Practice:** Progressing through foundational TryHackMe learning paths (*Pre-Security*, *Jr Penetration Tester*, *Offensive Pentesting*) to reinforce hands-on offensive methodology and methodology verification in strictly authorized environments.
