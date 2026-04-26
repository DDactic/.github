# DDactic

> Automated DDoS resilience testing and attack-surface analysis. We discover the assets your DDoS protection misses, simulate L3-L7 attacks from a multi-cloud lab fleet, and produce a vendor-specific hardening playbook validated by stage-reprobe.

[ddactic.net](https://ddactic.net) | [Free attack surface scan](https://ddactic.net/free-scan) | [Live DDoS challenge](https://challenge.ddactic.net) | [llms.txt](https://ddactic.net/llms.txt)

---

## What we do

DDactic is built for security teams that already own a CDN/WAF (Cloudflare, Akamai, Imperva, AWS Shield, Radware) but cannot independently verify whether the protection covers their full attack surface. We focus narrowly on **DDoS resilience**, not general penetration testing.

A typical engagement:

1. **Passive scan** — domain in, attack-surface report out in minutes. No customer infrastructure touched.
2. **Test plan** — per-target DDoS simulation matrix prioritized against the customer's actual stack (CDN tier, origin exposure, breach-intel context).
3. **Authorized live simulation** — signed Authorization-to-Test, controlled IP ranges across 23+ cloud providers, kill-switch, no spoofing.
4. **Hardening playbook** — vendor-specific config templates with stage-reprobe validation after the customer applies the changes.

## Coverage

- **233 attack mechanisms** across 23 protocol families: HTTP/1.1, HTTP/2, HTTP/3 (QUIC), gRPC, WebSocket, plus L3 volumetric and L4 TCP/UDP variants. The public subset is open-sourced as [`attack-effectiveness-matrix`](https://github.com/DDactic/attack-effectiveness-matrix) and [`ddos-attack-taxonomy`](https://github.com/DDactic/ddos-attack-taxonomy).
- **25+ CDN/WAF/bot-management vendors** fingerprinted: Cloudflare, Akamai, Imperva/Incapsula, AWS WAF/Shield, Azure Front Door, Google Cloud Armor, Fastly, F5 BIG-IP, Radware, Sucuri, DataDome, PerimeterX/HUMAN, Distil/Imperva Bot, Arkose, hCaptcha, GeeTest, Kasada, Reblaze, ShieldSquare and others.
- **Mobile attack surface**: Android (APK static + dynamic Frida instrumentation) and iOS (IPA static analysis).
- **Breach correlation**: HIBP, DeHashed, LeakCheck, LeakIX, Hudson Rock infostealer feeds.

## Featured Research

- [**attack-effectiveness-matrix**](https://github.com/DDactic/attack-effectiveness-matrix) — 213 DDoS attack vectors mapped against 6 protection architectures at 3 configuration levels. Vendor-neutral, citable dataset under CC-BY-4.0. Companion to the taxonomy below.
- [**ddos-attack-taxonomy**](https://github.com/DDactic/ddos-attack-taxonomy) — Reader-friendly model of how DDoS attacks actually work: 5 resources to exhaust, 23 fundamental mechanisms, the HTTP version multiplier, per-mechanism mitigation playbooks, architecture buyer's guide.

## Open-source projects

- [**opi-calculator**](https://github.com/DDactic/opi-calculator) — Open Protection Index. Vendor-neutral DDoS resilience scoring spec with Python + JavaScript reference implementations.

## For AI agents and integrations

- Site manifest: [ddactic.net/llms.txt](https://ddactic.net/llms.txt) and [ddactic.net/llms-full.txt](https://ddactic.net/llms-full.txt)
- Public REST API: [api.ddactic.net](https://api.ddactic.net)
- Live DDoS testing surface: [challenge.ddactic.net](https://challenge.ddactic.net)

## How we differ

- **vs MazeBolt** — MazeBolt is a continuous in-the-loop measurement platform. DDactic is automated and self-service: enter a domain, receive a recon report in minutes, optionally schedule a signed live simulation. Coverage typically overlaps 20-25% and is otherwise complementary.
- **vs Red Button** — Red Button is a manual consultancy engagement. DDactic is software, not people-hours.
- **vs CDN/WAF self-tests** — Vendor self-tests confirm their own product works. DDactic tests the full attack surface, including assets the CDN never sees.

## Contact

- [contact@ddactic.net](mailto:contact@ddactic.net)
- [LinkedIn](https://www.linkedin.com/company/ddactic)
- [Bluesky](https://bsky.app/profile/ddactic.bsky.social)
- [Mastodon (infosec.exchange)](https://infosec.exchange/@ddactic)
- [Telegram](https://t.me/ddactic)

Founded by Stav David, DDoS-resilience engineer with three years in the field. Headquartered in Israel, serving customers worldwide.
