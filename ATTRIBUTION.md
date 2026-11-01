# Discovery and Research Attribution

This release deliberately separates **authorship of this report** from **discovery of the underlying vulnerabilities**.

## PHP2Shell / CVE attribution

According to the PHP Foundation's post-incident account dated 21 October 2026:

- In 2024, PHP's external security work involved OSTIF and Quarkslab, and PHP developers identified early signs of the out-of-memory problem that later became central to CVE-2026-109618.
- Calif began an audit of PHP on 30 July 2026 through the Patch the Planet program.
- On 11 August 2026, **Ryan A. at Calif** reported unconditional remote code execution with the same root cause as the previously identified OOM problem.
- **OpenAI** independently reported the same root cause and later reported further attack vectors on 18 September 2026. The PHP Foundation specifically thanked **OpenAI Codex Security, especially Amy Burnett**.
- **Wiz** reported further attack vectors on 24 August 2026.
- The PHP Foundation also acknowledged Trail of Bits for later auditing work.

These organizations and researchers retain credit for their discoveries and responsible-disclosure work. Md Riyadh Hasan does not claim to have discovered PHP2Shell, CVE-2026-109618, or CVE-2026-109619.

## Original contribution of this report

The author claims authorship only of the report's original synthesis and presentation, including:

- the integrated technical/organizational incident analysis;
- the evidence ladder and hypothesis framing;
- analysis of PHP-dependent internet-business risk;
- the defensive honeypot research proposal;
- the report's original figures and visual synthesis; and
- the **Hasan PHP Dependency Resilience Framework (PDRF)**.

## Primary attribution source

The PHP Foundation, "Today's PHP Security Release, and How We're Strengthening PHP Security," 21 October 2026.

Official PHP security advisory and release archive, 21 October 2026.

Official source: https://thephp.foundation/blog/2026/10/21/todays-php-security-release-and-how-were-strengthening-php-security/

Verified against the Foundation post on 1 November 2026. The 2024 OOM signs were found by a Foundation-contracted PHP core developer while fixing a Quarkslab-reported issue; this is distinct from the 2026 demonstrated RCE reports. Acknowledgement of later auditing or tooling support does not by itself establish discovery of either CVE.
