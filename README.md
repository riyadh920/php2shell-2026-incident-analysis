# PHP2Shell 2026: Root Cause, Disclosure, Human Factors, Honeypot Evidence, Business Risk and PHP Ecosystem Resilience

**Author:** Md Riyadh Hasan  
**Affiliation:** Independent Researcher, Oxford, United Kingdom  
**Version:** 1.0.0  
**Release date:** 2026-11-01  
**Document type:** Independent technical incident report

## Abstract

PHP2Shell refers to two critical PHP runtime vulnerabilities, CVE-2026-109618 and CVE-2026-109619, disclosed and patched in October 2026. This rapid incident-analysis report examines the vulnerabilities as a combined technical, disclosure, governance, and internet-business resilience event. It synthesizes PHP project and PHP Foundation statements with public research and defensive telemetry to reconstruct the path from earlier out-of-memory concerns to 2026 vulnerability reports, disrupted coordinated disclosure, emergency patching, scanning, honeypot observations, and subsequent exploitation reporting. The analysis distinguishes confirmed findings from hypotheses, including whether human or social-engineering factors may have contributed to premature attacker knowledge; no reliable public evidence reviewed for this report implicates PHP personnel in intentional insider activity. The report also evaluates the consequences for organizations that depend directly or indirectly on PHP, including service continuity, credential and data exposure, supply-chain dependency, legacy runtime risk, recovery readiness, and architectural concentration. To translate the incident into a reusable defensive model, it introduces the Hasan PHP Dependency Resilience Framework (PDRF), a five-layer framework covering runtime visibility and patchability, exposure control, compromise containment, recovery and evidence, and architectural optionality. Honeypot evidence is treated as an important method for separating broad scanning from exploit-like activity and for reconstructing disclosure-to-exploitation timelines. The report concludes that PHP2Shell is best understood as a critical runtime-security incident amplified by structural and ecosystem factors, and recommends immediate patching together with longer-term resilience engineering for PHP-dependent organizations.

## Keywords

PHP2Shell, PHP security, CVE-2026-109618, CVE-2026-109619, remote code execution, vulnerability disclosure, honeypot, incident response, open-source security, internet business risk, cyber resilience, PHP Dependency Resilience Framework, PDRF, social engineering hypothesis, software supply chain

## Scope and attribution

This report is an independent analysis. It does **not** claim discovery, ownership, or authorship of PHP2Shell, CVE-2026-109618, CVE-2026-109619, PHP, or third-party research.

The PHP Foundation's 21 October 2026 account credits the security research and responsible disclosure contributions of **Calif (especially Ryan A.)**, **OpenAI Codex Security (especially Amy Burnett)**, and **Wiz**, while also acknowledging the earlier 2024 audit work involving **OSTIF and Quarkslab**. The Foundation states that Ryan A. at Calif reported unconditional remote code execution with the same OOM root cause on 11 August 2026; OpenAI independently reported the same root cause and later additional attack vectors; and Wiz reported further attack vectors on 24 August 2026.

The original contribution of this release is the author's synthesis, incident analysis, business-risk analysis, hypothesis framework, figures, and the **Hasan PHP Dependency Resilience Framework (PDRF)**. Third-party discoveries and evidence remain attributed to their respective researchers and organizations.

## Citation

Hasan, M. R. (2026). *PHP2Shell 2026: Root Cause, Disclosure, Human Factors, Honeypot Evidence, Business Risk and PHP Ecosystem Resilience* (Version 1.0.0) [Technical report]. 



[Read the canonical PDF](PHP2Shell_2026_Hasan_v1.0.0.pdf) · [Editable DOCX](PHP2Shell_2026_Hasan_v1.0.0.docx)

## Files

- `PHP2Shell_2026_Hasan_v1.0.0.pdf` - canonical public report
- `PHP2Shell_2026_Hasan_v1.0.0.docx` - earlier editable source; does not include the latest integrated hypotheses section
- `ABSTRACT.md` - abstract and keywords
- `CITATION.cff` - machine-readable citation metadata for GitHub
- `zenodo.json` - draft Zenodo deposition metadata
- `ATTRIBUTION.md` - discovery and source attribution statement
- `LICENSE.txt` - rights statement
- `RELEASE_NOTES.md` - version notes
- `SHA256SUMS.txt` - file-integrity hashes

## DOI

No DOI has been issued. The archival deposit is pending publication.

## DOI workflow

1. Create a public GitHub repository and upload this release package.
2. Create/tag release `v1.0.0`.
3. Deposit the canonical PDF and supporting metadata in Zenodo (or connect the GitHub repository to Zenodo if desired).
4. Publish the Zenodo record to obtain the DOI.
5. Update `CITATION.cff`, `README.md`, and the GitHub release with the assigned DOI.
6. Do not claim a DOI until the archival service has actually issued one.

## Research-integrity note

The report contains explicit hypotheses about disclosure and human factors. They are presented as hypotheses rather than accusations. No named PHP contributor, Foundation employee, researcher, or vendor is alleged to have participated in an attack unless supported by reliable evidence.

## Key findings

- PHP2Shell concerns PHP runtime memory and request-state handling, rather than a single application or CMS.
- Runtime inventory, patching, worker restart and verification are essential defensive actions.
- Disclosure disruption and limited specialist capacity are relevant to ecosystem resilience.
- Scanning, exploit-like traffic and confirmed execution require distinct evidence.

## PHP2Shell incident scope

The report analyses CVE-2026-109618 and CVE-2026-109619, the October 2026 disclosure and patch response, and public evidence reviewed through 1 November 2026.

## Figures

The report includes ten original visual syntheses: incident timeline; defensive technical model; evidence ladder; personnel context; hypothesis matrix; Telekom honeypot observations; PHP dependency concentration; business-impact propagation; PDRF; and a defensive response decision tree. Source-derived information remains attributed to its sources.

## Hypotheses

Structural and process failure, disclosure acceleration, human communication pathways, insider involvement and honeypot reconstruction are assessed separately. Social engineering and an insider pathway remain research hypotheses. No reliable public evidence reviewed in the report establishes intentional involvement by PHP Foundation personnel. Personnel timelines are contextual evidence only.

## Honeypot evidence

The report synthesizes third-party AWS and Telekom observations. It does not claim that the author collected those observations or conducted an exploitation experiment. A safe, isolated defensive honeypot study is proposed for future work.

## Hasan PHP Dependency Resilience Framework (PDRF)

The author's five-layer framework covers runtime visibility and patchability, exposure control, compromise containment, recovery and evidence, and architectural optionality.

## Responsible disclosure/discovery attribution

See [ATTRIBUTION.md](ATTRIBUTION.md) for source-grounded credits. Md Riyadh Hasan is the author of this independent report and does not claim vulnerability discovery.

## Evidence classification

| Class | Meaning |
| --- | --- |
| Confirmed evidence | Directly established within the cited source's stated scope. |
| Corroborated evidence | Supported by independent sources; shared sourcing alone is insufficient. |
| Reported evidence | Attributed to a source and not independently reproduced by this author. |
| Hypothesis | A testable explanation whose causal pathway remains unestablished. |
| Unsupported allegation | An allegation lacking reliable supporting evidence; not a finding. |

Vendor telemetry remains reported evidence in this synthesis even when the vendor confirms a result within its own environment.

## Version

1.0.0 — publication date 1 November 2026. Repository commits and the formal release provide platform timestamps; a DOI is claimed only after archival publication.

## License/rights

Copyright © 2026 Md Riyadh Hasan. Original text, figures, synthesis and PDRF are covered by [LICENSE.txt](LICENSE.txt). Public reading and citation of the unmodified report are permitted under that rights statement. PHP, the CVEs, vulnerability discoveries, third-party material and trademarks remain with their respective owners.

## Disclaimer

Independent technical report / cybersecurity incident analysis; not peer-reviewed. This report does not establish employee involvement or identify any person as an attacker. It is a time-bounded synthesis, and later evidence may revise incident understanding. Defensive analysis is not authorization to test systems.

## PDF replacement — 1 November 2026

The canonical 25-page PDF incorporates the author-supplied hypotheses-integrated revision, including section 2A and the executive-summary hypothesis focus. Only its cover title/version was standardized for publication. The DOCX is an earlier editable source and is not synchronized with this PDF. The original v1.0.0 tag preserves the first repository snapshot; the main branch and replacement release assets contain this revision.
