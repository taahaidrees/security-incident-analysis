# 🚨 Security Incident Analysis - Brute-Force Web Server Compromise

A simulated cybersecurity incident report documenting a brute-force compromise of a web server, malicious website modification, network-protocol evidence, and a recommended authentication control.

## Overview

An attacker gained access to a website's administrative account by repeatedly attempting known default passwords. After obtaining access, the attacker modified the site's source code, caused visitors to download a malicious executable, and redirected affected users to a malicious website.

## Investigation Highlights

- Identified DNS activity used to resolve the legitimate and malicious domain names.
- Connected HTTP requests with the observed web activity.
- Analyzed the brute-force attack path and the role of a default administrative password.
- Documented the malicious JavaScript and executable-driven redirect described in the incident evidence.
- Applied a sandbox-based investigation approach.
- Recommended two-factor authentication (2FA) for administrative accounts.

## Attack Chain

`Default password` → `Brute-force access` → `Admin panel compromise` → `Malicious JavaScript` → `Executable download` → `Malicious redirect`

## Files

- `security-incident-analysis.md` - Full incident analysis
- `security-incident-analysis.pdf` - Portfolio-ready incident report

## Skills Demonstrated

Incident Response • DNS • HTTP • tcpdump • Network Analysis • Brute-Force Analysis • Web Security • 2FA • Security Documentation

## Project Context

This project uses a simulated cybersecurity training scenario. It demonstrates practical incident-analysis and documentation skills and is not presented as production or employment experience.
