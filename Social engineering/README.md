# Parking Lot USB Exercise

## Overview
Simulated incident-response and social-engineering risk analysis of a USB drive found in a
hospital parking lot, belonging to an employee and containing a mix of personal and
work-related files.

## Objective
Assess what kind of information exposure a found, unencrypted USB drive represents, reason
through how an attacker could exploit that information, and identify controls that would
mitigate this class of physical / social-engineering risk.

## Tools & Skills Used
- Attacker-mindset / threat modeling reasoning
- PII identification and data classification
- Risk analysis (technical, operational, and managerial controls)
- Social engineering awareness

## Process
1. Reviewed the contents of the drive, noting that personal files (family plans, a colleague's
   wedding details) were mixed with work files (shift schedules, budget information).
2. Reasoned through how an attacker could weaponize this mix of information — e.g. using shift
   schedules and personal details to craft a targeted social engineering attack, or using budget
   data for competitive or financial harm.
3. Considered the technical risk of the drive itself: an unscanned USB could carry a trojan or
   ransomware payload capable of compromising a connected machine or creating a backdoor.
4. Identified controls to reduce this risk going forward, spanning technical (device scanning,
   USB port restrictions), operational (no mixing personal/work data on portable media), and
   managerial (security awareness training) categories.

## Findings / Outcome
Concluded that mixing personal and professional data on a single portable device meaningfully
increases an organization's attack surface — a single lost device can double as both a malware
vector and a ready-made profile for targeted social engineering or blackmail.

## Artifacts
- `Parking_lot_USB_exercise.pdf` — full write-up

## Notes
Based on a simulated scenario from Google Cybersecurity Professional Certificate coursework.
Names and the organization referenced are fictional.
