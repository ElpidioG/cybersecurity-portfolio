# Incident Report Analysis (NIST Framework)

## Overview
Analysis of a simulated DoS (denial-of-service) incident — an ICMP flood caused by an
unconfigured firewall — structured around the NIST Cybersecurity Framework's five core
functions: Identify, Protect, Detect, Respond, Recover.

## Objective
Given an incident summary, work through each stage of the NIST framework to explain what
happened, what controls were used to contain it, and what should be put in place to detect,
respond to, and recover from similar incidents in the future.

## Tools & Skills Used
- NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, Recover)
- Network security concepts (ICMP floods, DoS attacks, IP spoofing)
- Firewall configuration and rate-limiting
- IDS/IPS and SIEM concepts (e.g. Splunk)
- Incident response and network segmentation planning

## Process
1. **Identify** — Determined the root cause: an unconfigured firewall allowed a malicious actor
   to flood the server with ICMP packets, taking internal network services down for two hours.
2. **Protect** — Outlined the controls put in place after the incident: a firewall rule to
   rate-limit ICMP traffic, source IP address verification to catch spoofed packets, network
   monitoring software, and an IDS/IPS system to filter suspicious traffic; also noted that
   automatic network segmentation on threat detection would strengthen this further.
3. **Detect** — Recommended a SIEM system (e.g. Splunk) for centralized log monitoring, paired
   with IDS for ongoing packet-level traffic inspection.
4. **Respond** — Proposed containing future incidents via network segmentation to stop lateral
   spread, consulting an incident response playbook for known attack patterns, and maintaining
   firewall rules/policies on an ongoing basis rather than only after an incident.
5. **Recover** — Framed recovery around first scoping the extent of the attack (in this case,
   confirming only the internal network was affected) before restarting affected services.

## Findings / Outcome
Mapped a real-world-style DoS incident end-to-end across all five NIST functions, showing that
the original fix (blocking ICMP traffic) addressed the immediate symptom, while the added
controls (rate-limiting, IP verification, IDS/IPS, monitoring) targeted the underlying
misconfiguration — and identified monitoring/detection (SIEM) and segmentation as the two
biggest gaps still worth closing.

## Artifacts
- `Incident_report_analysis.pdf` — full NIST-structured write-up

## Notes
Based on a simulated incident scenario and template from Google Cybersecurity Professional
Certificate coursework, used here to demonstrate applying the NIST Cybersecurity Framework to
a concrete case.
