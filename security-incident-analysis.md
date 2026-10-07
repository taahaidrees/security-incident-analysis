# Security Incident Analysis - Brute-Force Web Server Compromise

**Author:** Taaha Idrees  
**Project Type:** Simulated cybersecurity training incident  
**Focus:** Network protocols, incident documentation, brute-force analysis, remediation

## Incident Overview

This project documents a simulated compromise of a recipe website. An attacker gained administrative access through a brute-force attack, modified the website's source code, and caused visitors to download a malicious executable that redirected them to a fake website.

## Section 1 - Network Protocols Identified

DNS (Domain Name System) was identified during the investigation. The browser first sent a DNS request to resolve yummyrecipesforme.com to its IP address. After the malicious redirect was triggered, another DNS request resolved greatrecipesforme.com. HTTP requests were then used to communicate with the web servers.

## Section 2 - Incident Documentation

A former employee gained access to the administrative account for yummyrecipesforme.com through a brute-force attack. The administrative account was still using its default password, and no controls were in place to prevent repeated login attempts. After obtaining access to the admin panel, the attacker modified the website's source code and inserted JavaScript that prompted visitors to download and run an executable file.

Customers reported that after running the file, their browsers were redirected from yummyrecipesforme.com to greatrecipesforme.com and their computers began running more slowly. During the investigation, analysts used a sandbox environment and tcpdump to observe the suspicious behavior. The captured sequence showed DNS resolution for yummyrecipesforme.com, an HTTP request to the site, the malware download, DNS resolution for greatrecipesforme.com, and an HTTP request to the redirected site. A senior analyst inspected the website source code and confirmed that unauthorized JavaScript had been added. Analysis of the downloaded file found a script responsible for redirecting visitors to the malicious website.

## Analyst Investigation Note

Investigation approach: A suspicious website should not be tested on a normal workstation. The website's source code and behavior should be examined in an isolated sandbox environment. In this scenario, source-code inspection was especially relevant because unauthorized JavaScript had been inserted into the compromised site.

## Section 3 - Recommended Remediation

### Two-Factor Authentication (2FA)

Implement two-factor authentication (2FA) for administrative accounts. In this incident, the attacker gained access by successfully guessing the administrative account's default password through repeated login attempts. With 2FA enabled, possession of the password alone would not normally be sufficient to authenticate because an additional verification factor would also be required. This adds another layer of protection if a password is compromised.

## Attack Chain

```text
Default admin password + unrestricted repeated attempts
        |
        v
Brute-force compromise of administrative account
        |
        v
Unauthorized access to website admin panel
        |
        v
Malicious JavaScript added to website source code
        |
        v
Visitors prompted to download and run executable
        |
        v
Browser redirected to malicious website
```

## Skills Demonstrated

- Security incident documentation
- DNS and HTTP traffic analysis
- Brute-force attack analysis
- Web compromise investigation
- Sandbox-based investigation
- tcpdump evidence interpretation
- Authentication security and 2FA

## Portfolio Note

This project is based on a simulated cybersecurity training scenario. The report demonstrates incident-analysis, network-protocol, documentation, and remediation skills rather than production or employment experience.
