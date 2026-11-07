
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,55:0a1628,100:E8630A&height=190&section=header&text=Mohamed%20Benbouazza&fontSize=43&fontColor=ffffff&fontAlignY=38&desc=SOC%20Systems%20Architect%20%7C%20AI-assisted%20Security%20Operations&descAlignY=60&descSize=15&descColor=c9d1d9" width="100%"/>

### Building AI-assisted systems for repetitive SOC operations.

I turn security alerts, investigation artifacts and detection requirements into structured, reviewable workflows.

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohamedbenbouazza/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/mohamed-ai-sec)
[![Substack](https://img.shields.io/badge/Substack-FF6719?style=flat-square&logo=substack&logoColor=white)](https://substack.com/@benbouazza)
[![X](https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/benbouazza_m)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mbenbouazzam@gmail.com)

[![Open to Work](https://img.shields.io/badge/OPEN%20TO%20WORK-SOC%20%2F%20MSSP%20ROLES-238636?style=flat-square)](mailto:mbenbouazzam@gmail.com)

</div>

---

## About

I'm Mohamed, a cybersecurity technician with a networking background, based in Morocco.

My focus is building practical AI-assisted systems for Security Operations Centers (SOC).

I work on a simple problem: security analysts spend significant time repeating operational tasks that can be structured, documented and assisted by reusable workflows.

My projects explore how **Claude, AI agents, `SKILL.md`, explicit rules and structured workflows** can support:

- Security alert triage.
- Incident investigation and reporting.
- Detection engineering.
- Phishing analysis.
- Repeatable SOC procedures.

The goal isn't to replace the analyst. It's to make the first pass more consistent, explainable and easier to review.

## Open-source SOC systems

Five repositories. Five different responsibilities within security operations.

| Repository | Purpose | Main output |
|---|---|---|
| [soc-l1-triage-engine](https://github.com/mohamed-ai-sec/soc-l1-triage-engine) | Structured L1 alert investigation | TP / FP / Escalate verdict, evidence and confidence |
| [sentinel-soc-ai](https://github.com/mohamed-ai-sec/sentinel-soc-ai) | Broader SOC analyst assistance | L1 / L2 / L3 investigation guidance |
| [soc-auto-report-skill](https://github.com/mohamed-ai-sec/soc-auto-report-skill) | Incident documentation | Structured 12-section incident report |
| [soc-detection-engineer-skill](https://github.com/mohamed-ai-sec/soc-detection-engineer-skill) | Detection engineering assistance | KQL, SPL, Sigma, EQL and other detection drafts |
| [soc-ai-systems](https://github.com/mohamed-ai-sec/soc-ai-systems) | Reusable SOC AI workflow foundation | Skill framework and documentation |

---

## System architecture

The projects address different stages of SOC operations. They are complementary standalone systems, not an already-integrated automated platform.

<div align="center">

<img src="assets/soc-systems-overview.gif" width="100%" alt="SOC systems architecture: alert intake, triage, incident reporting, detection engineering, SENTINEL analyst assistance and human review"/>

</div>

### How the workflow works

```mermaid
flowchart TD
    A["SECURITY INPUT<br/>SIEM Alert · EDR Event · Logs · Email"]
    B["01 — ALERT TRIAGE<br/>soc-l1-triage-engine"]
    C["ASSESSMENT<br/>TP / FP / Escalate"]
    D["02 — INCIDENT REPORTING<br/>soc-auto-report-skill"]
    E["03 — DETECTION ENGINEERING<br/>soc-detection-engineer-skill"]
    F["ANALYST REVIEW<br/>Verify Evidence · Investigate · Decide"]
    S["SENTINEL<br/>L1 / L2 / L3 Analyst Assistance"]
    R["SOC-AI-SYSTEMS<br/>Reusable Skill Foundation"]

    A --> B --> C
    C -->|Further investigation| D
    D --> E
    C --> F
    D --> F
    E --> F
    S -.-> B
    S -.-> F
    R -.-> B
    R -.-> D
    R -.-> E

    style A fill:#161b22,stroke:#8b949e,color:#fff
    style B fill:#161b22,stroke:#E8630A,color:#fff
    style C fill:#161b22,stroke:#E8630A,color:#fff
    style D fill:#161b22,stroke:#E8630A,color:#fff
    style E fill:#161b22,stroke:#E8630A,color:#fff
    style F fill:#161b22,stroke:#238636,color:#fff
    style S fill:#161b22,stroke:#8b949e,color:#fff
    style R fill:#161b22,stroke:#8b949e,color:#fff
```

### 01. SOC L1 Triage Engine

**Repository:** [soc-l1-triage-engine](https://github.com/mohamed-ai-sec/soc-l1-triage-engine)

A structured approach to evaluating SOC alerts before escalation or closure.

Key capabilities:

- Five-dimensional context evaluation.
- True Positive / False Positive / Escalate verdicts.
- Confidence assessment.
- MITRE ATT&CK mapping.
- Alert-specific investigation playbooks.
- Evidence-based reasoning.

**Problem addressed:** Repetitive L1 alert analysis and inconsistent triage decisions.

### 02. SENTINEL — SOC Analyst AI

**Repository:** [sentinel-soc-ai](https://github.com/mohamed-ai-sec/sentinel-soc-ai)

A broader analyst-assistance framework designed around SOC investigation workflows.

Key capabilities:

- L1 / L2 / L3 investigation guidance.
- Phishing investigation.
- Security event analysis.
- KQL and SPL assistance.
- Explicit investigation and enforcement rules.

**Problem addressed:** Providing structured investigation guidance across different SOC responsibilities.

### 03. SOC Auto-Report Engine

**Repository:** [soc-auto-report-skill](https://github.com/mohamed-ai-sec/soc-auto-report-skill)

A reporting workflow that organizes supplied security artifacts into structured incident documentation.

Key capabilities:

- 12-section incident report.
- Executive summary.
- Incident timeline.
- IOC documentation.
- Detection recommendations.
- Multiple security data formats.

**Problem addressed:** Repetitive incident documentation and the time required to prepare consistent reports.

### 04. SOC Detection Engineer Skill

**Repository:** [soc-detection-engineer-skill](https://github.com/mohamed-ai-sec/soc-detection-engineer-skill)

A detection engineering assistant for structuring detection logic and rule development.

Supported detection formats and technologies include:

- KQL
- SPL
- Sigma
- EQL
- YARA
- Zeek
- Falco
- auditd

Key focus areas:

- Detection logic.
- Telemetry assessment.
- Input confidence.
- Rule validation.
- False-positive considerations.

**Problem addressed:** Making detection engineering workflows more structured, transparent and reviewable.

### 05. SOC AI Systems

**Repository:** [soc-ai-systems](https://github.com/mohamed-ai-sec/soc-ai-systems)

The reusable foundation behind my approach to packaging SOC AI workflows.

Focus areas:

- `SKILL.md` structure.
- Reusable instructions.
- Documentation.
- Workflow organization.
- Open-source distribution.

**Problem addressed:** Making SOC AI workflows easier to package, understand and reuse.

---

## Engineering principles

I build around a few rules:

| Principle | Implementation |
|---|---|
| Evidence first | Conclusions must be supported by supplied evidence. |
| No invented IOCs | Missing indicators remain missing. |
| No fabricated timestamps | Unknown timestamps are not reconstructed as facts. |
| Visible uncertainty | Distinguish observed, suspected, confirmed and unknown. |
| Structured output | Use defined formats for repeatable results. |
| Human oversight | Analysts verify findings and make security decisions. |

**AI assists the investigation. The analyst owns the decision.**

## Technology stack

<div align="center">

![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square)
![SKILL.md](https://img.shields.io/badge/SKILL.md-agentskills.io-238636?style=flat-square)
![KQL](https://img.shields.io/badge/KQL-0078D4?style=flat-square)
![SPL](https://img.shields.io/badge/SPL-FF4500?style=flat-square)
![Sigma](https://img.shields.io/badge/Sigma-4A90D9?style=flat-square)
![EQL](https://img.shields.io/badge/EQL-00BFB3?style=flat-square)
![YARA](https://img.shields.io/badge/YARA-E8630A?style=flat-square)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-E8630A?style=flat-square)
![Microsoft Sentinel](https://img.shields.io/badge/Microsoft%20Sentinel-0078D4?style=flat-square)
![Splunk](https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)

</div>

## Installation and usage

Each repository contains its own source files and installation instructions.

For projects packaged as Claude Skills:

1. Open the repository.
2. Read its installation instructions.
3. Inspect the `SKILL.md` and supporting files.
4. Follow the documented installation method.
5. Provide a sanitized security artifact.
6. Review the generated output against the original evidence.

Start with the [SOC L1 Triage Engine](https://github.com/mohamed-ai-sec/soc-l1-triage-engine).

Installation requirements can differ between projects.

## Development roadmap

- [ ] Publish reproducible demonstrations for each project.
- [ ] Expand phishing investigation workflows.
- [ ] Add more sanitized investigation examples.
- [ ] Improve detection validation and testing.
- [ ] Document edge cases and limitations.
- [ ] Continue improving reusable SOC skills.

## Contributions and feedback

Found an incorrect verdict, unsupported assumption or an edge case?

Open an issue in the relevant repository.

Useful reports include:

- A sanitized input example.
- The generated output.
- The unexpected behavior.
- The expected behavior.

Never include real credentials, confidential logs or sensitive organizational data.

## Connect

I'm interested in cybersecurity, SOC operations, detection engineering and practical AI automation.

- LinkedIn: [Mohamed Benbouazza](https://www.linkedin.com/in/mohamedbenbouazza/)
- GitHub: [mohamed-ai-sec](https://github.com/mohamed-ai-sec)
- Substack: [Technical writing](https://substack.com/@benbouazza)
- X: [@benbouazza_m](https://x.com/benbouazza_m)
- Email: [mbenbouazzam@gmail.com](mailto:mbenbouazzam@gmail.com)

---

<div align="center">

**Built in public. Documented with evidence. Open source.**

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:E8630A,45:0a1628,100:0D1117&height=110&section=footer" width="100%"/>

</div>
