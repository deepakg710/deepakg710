# Deepak G.

**Cybersecurity & Systems Engineering · Network Forensics · Defensive Detection & Telemetry**  
B.E. in Computer Science and Engineering — Ballari Institute of Technology & Management (BITM), Karnataka, India (`2023–2027`)

---

## Career Focus

I build **offline-first security analysis and defensive monitoring systems** that turn raw network packets, Windows Active Directory audit events, and endpoint telemetry into explainable, evidence-backed findings.

My engineering work focuses on:
- **Network Forensics & Protocol Dissection:** Streaming `.pcap` / `.pcapng` inspection, recursive-descent display-filter engines, L4 flow state machines, and communication topology reconstruction.
- **Active Directory & Endpoint Detection Engineering:** Windows Event Forwarding (`4624`, `4625`, `4663`, `4688`, `5145`, `1116`), read-only process lineage tracking, privacy-preserving browser telemetry, and multi-sensor timeline correlation.
- **Explainable Diagnostics:** Every alert or topology link is backed by raw frame numbers, Windows event IDs, or explicit heuristic `basis` strings—clearly separating observed facts from inferred relationships.

---

## Featured Projects

### 1. [NetTrace — Offline PCAP/PCAPNG Packet Analysis & Communication Topology Platform](https://github.com/deepakg710/NetTrace)
> **Stack:** Python 3.11 · FastAPI · Scapy · SQLite · React 18 · TypeScript · Tailwind CSS · Vitest & Pytest

An offline packet analysis and network troubleshooting platform comparable to core Wireshark workflows, designed with a beginner-friendly filter builder and interactive communication topology canvas.
- **Recursive-Descent Display-Filter Engine:** Safe tokenizer and AST parser (`ip.addr == 192.168.1.10 && tcp`, `dns || tcp.port == 443`, `tcp.flags.reset == 1`, `!(arp)`) shared across backend SQLite/Python evaluation and frontend live validation.
- **3-Pane Packet Explorer:** Synchronized packet list, expandable protocol layer tree (`Frame`, `Ethernet II`, `IPv4/IPv6`, `TCP/UDP/ICMP`, `DNS/HTTP/TLS`), and interactive hex/ASCII byte viewer.
- **Interactive Communication Topology:** Force-directed and 3-column grouped layouts with isolated-endpoint separation, byte-scaled nodes/edges, protocol breakdown bars, and explicit `inferred=true` + `basis` annotations for L2 gateway/shared-MAC links.
- **Verification:** `12 passed` backend Pytest integration tests + `10 passed` frontend Vitest component tests + deterministic sample PCAP verification (`.\scripts\verify.ps1`).

---

### 2. [AD-Monitor — Active Directory Insider Threat Detection & Multi-Sensor UBA Platform](https://github.com/deepakg710/AD-Monitor)
> **Stack:** Python 3.11+ · FastAPI · SQLite (WAL) · Argon2id · PowerShell · Manifest V3 Extension · React 18 · TypeScript

A multi-source defensive monitoring platform for controlled Active Directory laboratory environments that correlates Windows security auditing, endpoint process snapshots, and domain-level browser activity.
- **Multi-Sensor Investigation Timeline:** Correlates domain navigation $\rightarrow$ file download (`SHA-256`) $\rightarrow$ process execution $\rightarrow$ child process lineage with explicit *"What This Evidence Proves"* and *"What It Does Not Prove"* boundaries.
- **19 Deterministic Detection Rules + Isolation Forest UBA:** Evaluates canary file access, staging & archive creation, script execution, and wrong-password lockouts alongside a pure-Python Isolation Forest model with a 48-window cold-start gate (`Collecting baseline`).
- **Privacy & Security by Design:** Argon2id authentication with mandatory unique 12+ character passphrases on initial setup, DPAPI-encrypted collector tokens, command-line secret redaction, and domain-only browser telemetry.
- **Verification:** `27 passed` automated unit and end-to-end integration tests across database migrations, XML event normalization, detection rules, UBA math, and REST API security (`pytest -v`).

---

## Technical Skills

| Area | Technologies & Tools |
| :--- | :--- |
| **Languages** | Python, TypeScript, JavaScript, SQL, PowerShell, Bash, C/C++ |
| **Security & Networking** | PCAP/PCAPNG Dissection (Scapy, Wireshark), TCP/IP & DNS Diagnostics, Windows Security Auditing (WEF, Sysmon), Argon2id, Windows DPAPI, CSRF/Session Hardening |
| **Backend & Data** | FastAPI, SQLAlchemy, Pydantic v2, SQLite (WAL & Reversible Migrations), REST API Design |
| **Frontend & Visualization** | React 18, Vite, Tailwind CSS, Interactive SVG Network Topology Graphs, Recharts |
| **Testing & Verification** | Pytest, Vitest, React Testing Library, GitHub Actions CI |

---

## Contact

- **GitHub:** [@deepakg710](https://github.com/deepakg710)
- **Email:** [deepak710op@gmail.com](mailto:deepak710op@gmail.com)
