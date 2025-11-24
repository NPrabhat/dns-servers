# HaGeZi DNS: Free, Non-Commercial EU Public DNS Servers

HaGeZi DNS offers free, non-commercial public DNS resolvers designed and operated by a private individual for the European community. It provides robust DNS-based blocking of ads, trackers, scam, phishing, fake, and malware domains - helping users achieve greater privacy and security online with zero cost.

## Features

- EU-only hosting (Hetzner: Falkenstein, Nuremberg, Helsinki) and jurisdiction, with full GDPR and ENISA recommendations.
- Entirely open-source stack: Technitium DNS with Unbound as upstream and a local root zone copy on Debian 13.
- Blocking level: Balanced (Ad, Tracking, Scam, Phishing, Malware)
- Blocklists: HaGeZi Multi Pro & HaGeZi Threat Intelligence Feeds
- No additional censorship, only security and privacy-oriented filtering.

## Security & Privacy

- No recursion via third-party resolvers.
- Strict DNSSEC validation to prevent tampering.
- QNAME minimization is enforced for better privacy.
- DNS leak/rebind protection
- No EDNS Client Subnet, user location is not exposed to upstreams.
- Rate limiting for response and clients.
- Only encrypted transport: DNS-over-HTTPS (DoH/DoH3), DNS-over-TLS (DoT) and DNS-over-QUIC (DoQ)
- No conventional DNS over port 53 to protect against DNS-based DDoS, amplification, spoofing, and cache poisoning.
- Firewall: restricted to ports strictly necessary for operation.
- OS & DNS software are regularly updated for latest security.
- No logging or storage of individual queries per client.
- No sharing of any data with third parties. If you don't log anything sharable, you can't share anything.

## Logging and Data Handling

- Hourly DNS statistics (processed and block domain rankings, per-client query counts) stored only in RAM, never written to disk and auto-deleted each hour or on service/server restart.<br>(Query counts per client are solely for rate limiting, no linkage to resolved/blocked domains or other details)
- Error logging: Only domains failing to resolve (due to DNSSEC, server, timeout, etc. - resulting in SERVFAIL) are logged for up to 7 days for troubleshooting. No client IP addresses are included.

## Getting Help

- Open a GitHub Issue or contact [support@hagezi.org](mailto:support@hagezi.org) for support and questions.

## Server Locations & Access

| Location           | Protocols     | Endpoint/URL                          | Apple<br>Config        | Good<br>EU Latency    |
|--------------------|---------------|-------------------------------------|-----------------------|-------------------------|
| Germany, Falkenstein| DoH/DoH3      | `https://root.hagezi.org/dns-query`   | [Link](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/root-hagezi-org.mobileconfig) [QR](/mobileconfig/root-hagezi-org.mobileconfig.png)    | DE, PL, CZ, AT, NL, DK, FR, LU, BE |
|                    | DoT/QUIC      | `root.hagezi.org`                     |                       |                         |
| Finland, Helsinki   | DoH/DoH3      | `https://juuri.hagezi.org/dns-query`  | [Link](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/juuri-hagezi-org.mobileconfig) [QR](/mobileconfig/juuri-hagezi-org.mobileconfig.png)    | FI, EE, SE, LV, LT, PL, DK |
|                    | DoT/QUIC      | `juuri.hagezi.org`                    |                       |                         |

## Disclaimer / Privacy Policy (EU Compliance)

HaGeZi DNS is a non-commercial, publicly accessible DNS resolver service operated privately for the public benefit in the EU.

- All servers are operated from data centers in the EU and fall under EU data protection laws, including EU General Data Protection Regulation (GDPR). User DNS traffic never leaves EU jurisdiction, and only encrypted protocols are offered to maximize privacy.
- No personal data (such as user names, IP resolution logs, or query specifics linked to individuals) is collected, persisted, or shared with any third party. For operational integrity, temporary and anonymized query statistics are maintained for a maximum of one hour exclusively in memory, not on permanent storage. IP addresses are only ever processed for technical features such as query rate limiting and are not bindable to resolution data.
- Error logs contain only metadata about DNS failures (domain, timestamp, error type, no client data).
- No client data is ever sold or shared. All technical and policy guidelines align with the best practices of leading EU projects.
- Service and server security are proactively maintained; software is kept up-to-date.
- This is a best-effort, volunteer-provided service with no warranty, availability, or liability for interruptions or malfunctions. It is intended for private, lawful use only. Misuse, automated abuse, or attempts to circumvent restrictions may result in access being blocked.
- This service is not affiliated with any commercial provider, government body, or the DNS4EU consortium.
- Use of the service constitutes acceptance of these terms.

For privacy matters or to request information on data processing, contact [privacy@hagezi.org](mailto:privacy@hagezi.org).

Service operator: HaGezi - [mail@hagezi.org](mailto:mail@hagezi.org), maintained by a private individual in accordance with Article 4 and 13/14 GDPR for non-commercial volunteer projects within the EU.

---
