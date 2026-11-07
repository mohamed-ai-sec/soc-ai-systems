<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,55:0a1628,100:E8630A&height=200&section=header&text=Mohamed%20Benbouazza&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=SOC%20Systems%20Architect%20%E2%80%94%20AI%20systems%20for%20the%20repetitive%20half%20of%20SOC%20work&descAlignY=60&descSize=15&descColor=c9d1d9&animation=fadeIn" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=600&size=16&pause=1400&color=E8630A&center=true&vCenter=true&width=820&lines=A+prompt+is+a+tool.+A+SKILL.md+is+infrastructure.;Alert+%E2%86%92+TP%2FFP+verdict+%E2%86%92+IR+report+%E2%86%92+detection+rule.;5+open-source+SOC+systems.+Documented.+Versioned." alt="A prompt is a tool. A SKILL.md is infrastructure." />

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/mohamedbenbouazza/)
[![Substack](https://img.shields.io/badge/Substack-FF6719?style=flat-square)](https://substack.com/@benbouazza)
[![X](https://img.shields.io/badge/X-000000?style=flat-square)](https://x.com/benbouazza_m)
[![Linktree](https://img.shields.io/badge/Linktree-43E55E?style=flat-square)](https://linktr.ee/mbenbouazzam)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square)](mailto:mbenbouazzam@gmail.com)

[![Open to work](https://img.shields.io/badge/OPEN%20TO%20WORK-Remote%20SOC%20%2F%20MSSP%20roles-238636?style=flat-square)](mailto:mbenbouazzam@gmail.com)

</div>

---

## Who I am

Network-trained cybersecurity technician, Morocco. I turn repetitive SOC work into open-source AI systems: analysts decide, systems do the first pass.

---

## Systems

| System | Problem it targets | Output | Activity |
|:---|:---|:---|:---|
| [**soc-l1-triage-engine**](https://github.com/mohamed-ai-sec/soc-l1-triage-engine) | L1 time lost on false positives | TP / FP / Ambiguous verdict, confidence X/5, MITRE mapping, escalation or closure note | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-l1-triage-engine?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-l1-triage-engine?style=flat-square) |
| [**soc-auto-report-skill**](https://github.com/mohamed-ai-sec/soc-auto-report-skill) | IR reporting takes hours and costs SLAs | 12-section report + PIR, detection queries, executive brief, regulatory notice, staff update | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-auto-report-skill?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-auto-report-skill?style=flat-square) |
| [**soc-detection-engineer-skill**](https://github.com/mohamed-ai-sec/soc-detection-engineer-skill) | Detection rules take days to write correctly | Structured draft rules in KQL, SPL, Sigma, EQL | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-detection-engineer-skill?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-detection-engineer-skill?style=flat-square) |
| [**sentinel-soc-ai**](https://github.com/mohamed-ai-sec/sentinel-soc-ai) | No senior analyst on every shift | L1 / L2 / L3 AI analyst | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/sentinel-soc-ai?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/sentinel-soc-ai?style=flat-square) |
| [**soc-ai-systems**](https://github.com/mohamed-ai-sec/soc-ai-systems) | No standard way to package SOC AI workflows | Master `SKILL.md` framework and docs | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-ai-systems?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-ai-systems?style=flat-square) |

Typical order of use. Each skill also works on its own.

```mermaid
flowchart LR
    A["Alert or log"] --> B["soc-l1-triage-engine<br/>verdict"]
    B --> C["soc-auto-report-skill<br/>incident report"]
    C --> D["soc-detection-engineer-skill<br/>detection rules"]
```

Each repo has a **How it works** diagram:
[triage engine](https://github.com/mohamed-ai-sec/soc-l1-triage-engine#how-it-works) ·
[report skill](https://github.com/mohamed-ai-sec/soc-auto-report-skill#how-it-works) ·
[how a skill runs](https://github.com/mohamed-ai-sec/soc-ai-systems#how-a-skill-runs-in-claude)

---

## Install in Claude

1. Open **Customize → Skills**. Code execution and file creation must be on. *(Older versions: Settings → Capabilities → Skills.)*
2. Click **+**, then **Create skill**, then **Upload a skill**.
3. Upload the ZIP and toggle the skill on.
4. Ask: *"Use soc-l1-triage-engine on this alert: …"*

The ZIP needs the skill folder as its root:

```text
soc-l1-triage-engine.zip
└── soc-l1-triage-engine/        folder name = skill name
    └── SKILL.md
```

| If the upload fails | Fix |
|:---|:---|
| Root folder name doesn't match the skill `name` | GitHub's **Download ZIP** names it `repo-main`. Rename the folder, then zip it again. |
| Files sit directly in the ZIP root | Put them inside one skill folder. |
| The file isn't called `SKILL.md` | Rename it. |
| Invalid characters in name or description | Use lowercase letters, numbers and hyphens in the name. |

Uploaded skills are private to your account and don't sync between claude.ai, Claude Code and the API.

---

## How they're built

- **Plain text.** Every rule lives in a `SKILL.md` you can read, diff and change.
- **Defined structure.** The triage engine, for example, runs fixed phases (intake, five-dimension context, playbook, score, close-out) and always ends in the same verdict report.
- **Evidence before verdict.** The skills tell you what to check. You run the lookups and paste the results.

## Limits

- They don't connect to your SIEM or run threat-intel lookups.
- Output depends on the context you paste in.
- Confidence scores are a triage aid. Review before you close a ticket or send a report.
- They don't replace L2 investigation.

Caught a wrong verdict? Open an issue with a sanitized sample. Those are the most useful contributions.

---

## Stack

![KQL](https://img.shields.io/badge/KQL-0078D4?style=flat-square)
![SPL](https://img.shields.io/badge/SPL-FF4500?style=flat-square)
![Sigma](https://img.shields.io/badge/Sigma-4A90D9?style=flat-square)
![EQL](https://img.shields.io/badge/EQL-00BFB3?style=flat-square)
![YARA](https://img.shields.io/badge/YARA-E8630A?style=flat-square)
![Microsoft Sentinel](https://img.shields.io/badge/Microsoft%20Sentinel-0078D4?style=flat-square)
![Defender XDR](https://img.shields.io/badge/Defender%20XDR-0078D4?style=flat-square)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-E8630A?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square)
![SKILL.md](https://img.shields.io/badge/SKILL.md-agentskills.io-238636?style=flat-square)

## On the list

`soc-phishing-skill` (phishing analysis pipeline) · `soc-enrichment-agent` (IOC enrichment)

## Writing

Build logs, failures and release notes: [Substack](https://substack.com/@benbouazza) · [LinkedIn](https://www.linkedin.com/in/mohamedbenbouazza/) · [X](https://x.com/benbouazza_m)

---

<div align="center">

**If one of these saved you a shift, star it. It helps other analysts find it.**

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:E8630A,45:0a1628,100:0D1117&height=120&section=footer&text=Built%20in%20public.&fontSize=14&fontColor=8b949e&fontAlignY=60&reversal=true" width="100%"/>

</div>
