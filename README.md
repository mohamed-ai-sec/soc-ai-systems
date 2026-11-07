<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,55:0a1628,100:E8630A&height=200&section=header&text=Mohamed%20Benbouazza&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=SOC%20Systems%20Architect%20%E2%80%94%20AI%20systems%20for%20the%20repetitive%20half%20of%20SOC%20work&descAlignY=60&descSize=15&descColor=c9d1d9&animation=fadeIn" width="100%"/>

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&weight=600&size=16&pause=1400&color=E8630A&center=true&vCenter=true&width=820&lines=A+prompt+is+a+tool.+A+SKILL.md+is+infrastructure.;Alert+%E2%86%92+TP%2FFP+verdict+%E2%86%92+IR+report+%E2%86%92+detection+rule.;5+open-source+SOC+systems.+Free.+Documented.+Versioned." alt="Typing SVG" />
</a>

<br/><br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohamedbenbouazza/)&nbsp;
[![Substack](https://img.shields.io/badge/Substack-FF6719?style=flat-square&logo=substack&logoColor=white)](https://substack.com/@benbouazza)&nbsp;
[![X](https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/benbouazza_m)&nbsp;
[![Linktree](https://img.shields.io/badge/Linktree-43E55E?style=flat-square&logo=linktree&logoColor=white)](https://linktr.ee/mbenbouazzam)&nbsp;
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:mbenbouazzam@gmail.com)

[![Open to work](https://img.shields.io/badge/OPEN%20TO%20WORK-Remote%20SOC%20%2F%20MSSP%20roles-238636?style=flat-square)](mailto:mbenbouazzam@gmail.com)

</div>

---

## Who I am

Network-trained cybersecurity technician, Morocco. I turn repetitive SOC work into open-source AI systems: analysts decide, systems do the first pass.

---

## The systems, in one picture

<div align="center">

<img src="assets/pipeline.gif" alt="One alert flows through triage, report and detection systems, with an always-on analyst persona underneath" width="100%"/>

</div>

| System | Problem it targets | Output | Activity |
|:---|:---|:---|:---|
| [**soc-l1-triage-engine**](https://github.com/mohamed-ai-sec/soc-l1-triage-engine) | L1 time lost on false positives | TP / FP / Escalate verdict with confidence, MITRE-mapped, per-alert-type playbooks | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-l1-triage-engine?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-l1-triage-engine?style=flat-square) |
| [**soc-auto-report-skill**](https://github.com/mohamed-ai-sec/soc-auto-report-skill) | IR reports take hours and cost SLAs | 12-section incident report, exec brief, detection queries | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-auto-report-skill?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-auto-report-skill?style=flat-square) |
| [**soc-detection-engineer-skill**](https://github.com/mohamed-ai-sec/soc-detection-engineer-skill) | Writing detection rules correctly takes days | Structured draft rules in KQL, SPL, Sigma, EQL | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-detection-engineer-skill?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-detection-engineer-skill?style=flat-square) |
| [**sentinel-soc-ai**](https://github.com/mohamed-ai-sec/sentinel-soc-ai) | No senior analyst on every shift | L1 / L2 / L3 analyst persona for Sentinel-style workflows | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/sentinel-soc-ai?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/sentinel-soc-ai?style=flat-square) |
| [**soc-ai-systems**](https://github.com/mohamed-ai-sec/soc-ai-systems) | No standard way to package SOC AI workflows | Master `SKILL.md` framework and docs | ![stars](https://img.shields.io/github/stars/mohamed-ai-sec/soc-ai-systems?style=flat-square&color=E8630A) ![commit](https://img.shields.io/github/last-commit/mohamed-ai-sec/soc-ai-systems?style=flat-square) |

---

## Use them in Claude

<div align="center">

<img src="assets/install-in-claude.gif" alt="Four steps: open Customize then Skills, plus then Create skill, upload the zip, toggle on and ask" width="100%"/>

</div>

1. **Open Customize → Skills** in Claude. Code execution and file creation must be on. *(Older versions: Settings → Capabilities → Skills.)*
2. Click **+**, then **Create skill**.
3. Choose **Upload a skill** and upload the ZIP.
4. Toggle it on. Then ask: *"Use soc-l1-triage-engine on this alert: …"*

**If the upload fails, it's almost always one of these:**
- The ZIP must contain the skill folder as its root, with `SKILL.md` inside it.
- The folder name must match the skill `name`. GitHub's **Download ZIP** names the root `repo-main`, so rename the folder first, then zip it again.
- Skills you upload are private to your account and don't sync between claude.ai, Claude Code and the API.

---

## Why the output stays clean

- **Fixed output format.** The model fills defined sections. It doesn't invent the structure.
- **Rules you can read.** The logic lives in a `SKILL.md` you can open, diff and change. It isn't hidden in a chat.
- **Works from what you paste.** Give it the alert, logs or headers. It reasons from those.
- **Still verify.** This cuts guessing. It doesn't remove it.

---

## See it work

> Replace this block with one real, sanitized run. It's the most important thing on the page.

```text
INPUT    [sanitized alert]
VERDICT  [True Positive]      CONFIDENCE  [__%]
WHY      [2–3 lines of evidence an analyst can verify in 10 seconds]
MITRE    [T1059.001 · PowerShell]
NEXT     [Escalate to L2 · attach IOCs]
TIME     [__ seconds]
```

---

## What these don't do

- They don't see your SIEM. Output quality depends on the context you paste in.
- Confidence scores are a triage aid, not a guarantee. Review before closing a ticket.
- They don't replace L2 investigation.
- [Add one real limit you found while testing.]

Caught a wrong verdict? Open an issue with a sanitized sample. Those are the most useful contributions I get.

---

## Stack

![KQL](https://img.shields.io/badge/KQL-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![SPL](https://img.shields.io/badge/SPL-FF4500?style=flat-square&logo=splunk&logoColor=white)
![Sigma](https://img.shields.io/badge/Sigma-4A90D9?style=flat-square)
![EQL](https://img.shields.io/badge/EQL-00BFB3?style=flat-square&logo=elastic&logoColor=white)
![YARA](https://img.shields.io/badge/YARA-E8630A?style=flat-square)
![Sentinel](https://img.shields.io/badge/Microsoft%20Sentinel-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Defender XDR](https://img.shields.io/badge/Defender%20XDR-0078D4?style=flat-square&logo=microsoft&logoColor=white)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE%20ATT%26CK-E8630A?style=flat-square)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat-square&logo=n8n&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square)
![SKILL.md](https://img.shields.io/badge/SKILL.md-agentskills.io-238636?style=flat-square)

---

## Roadmap

- [ ] `soc-phishing-skill`: phishing analysis pipeline *(in progress)*
- [ ] `soc-enrichment-agent`: IOC enrichment *(planned)*
- [ ] Demo recording for every system
- [ ] [Next real item, with a date only if you will hit it]

---

## Writing

Build logs, failures, and release notes. No theory.

[Substack](https://substack.com/@benbouazza) · [LinkedIn](https://www.linkedin.com/in/mohamedbenbouazza/) · [X](https://x.com/benbouazza_m)

---

<div align="center">

**If one of these saved you a shift, star it. It helps other analysts find it.**

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:E8630A,45:0a1628,100:0D1117&height=120&section=footer&text=Built%20in%20public.%20Shipped%20free.&fontSize=14&fontColor=8b949e&fontAlignY=60&reversal=true" width="100%"/>

</div>
