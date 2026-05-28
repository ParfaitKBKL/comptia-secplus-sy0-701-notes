# CompTIA Security+ SY0-701 - Study Notes

These are the personal study notes I used to prepare and pass the **CompTIA Security+ SY0-701** certification. The content is structured around the official exam objectives (v5.0) and was written alongside video courses, practice exams, and the official CompTIA objectives PDF. If you're preparing for the same exam, feel free to use these notes as a reference or starting point for your own revision.

---

## Exam at a Glance

| Detail | Value |
|---|---|
| Exam code | SY0-701 |
| Questions | Max 90 (MCQ + PBQ) |
| Duration | 90 minutes |
| Passing score | 750 / 900 |
| Recommended experience | 2+ years IT admin with security focus |

---

## Domain Weights

| # | Domain | Weight |
|---|---|---|
| 1 | [General Security Concepts](./domain-1-general-security-concepts/) | 12% |
| 2 | [Threats, Vulnerabilities, and Mitigations](./domain-2-threats-vulnerabilities-mitigations/) | 22% |
| 3 | [Security Architecture](./domain-3-security-architecture/) | 18% |
| 4 | [Security Operations](./domain-4-security-operations/) | 28% |
| 5 | [Security Program Management and Oversight](./domain-5-security-program-management/) | 20% |

> Domain 4 carries the most weight - prioritize it.

---

## Repository Structure

```
.
├── domain-1-general-security-concepts/
│   ├── 1.1-security-controls.md
│   ├── 1.2-fundamental-security-concepts.md
│   ├── 1.3-change-management.md
│   └── 1.4-cryptography.md
├── domain-2-threats-vulnerabilities-mitigations/
│   ├── 2.1-threat-actors-motivations.md
│   ├── 2.2-threat-vectors-attack-surfaces.md
│   ├── 2.3-vulnerability-types.md
│   ├── 2.4-malicious-activity-indicators.md
│   └── 2.5-mitigation-techniques.md
├── domain-3-security-architecture/
│   ├── 3.1-architecture-models.md
│   ├── 3.2-enterprise-infrastructure.md
│   ├── 3.3-data-protection.md
│   └── 3.4-resilience-recovery.md
├── domain-4-security-operations/
│   ├── 4.1-security-techniques-computing.md
│   ├── 4.2-asset-management.md
│   ├── 4.3-vulnerability-management.md
│   ├── 4.4-alerting-monitoring.md
│   ├── 4.5-enterprise-capabilities.md
│   ├── 4.6-identity-access-management.md
│   ├── 4.7-automation-orchestration.md
│   ├── 4.8-incident-response.md
│   └── 4.9-data-sources-investigation.md
├── domain-5-security-program-management/
│   ├── 5.1-security-governance.md
│   ├── 5.2-risk-management.md
│   ├── 5.3-third-party-risk.md
│   ├── 5.4-security-compliance.md
│   ├── 5.5-audits-assessments.md
│   └── 5.6-security-awareness.md
├── acronyms.md
└── LICENSE
```

---

## Study Resources

### Videos
- **Professor Messer SY0-701** (free on YouTube) - The gold standard reference, follows the official objectives exactly. Watch the full "CompTIA Security+ SY0-701 Course" playlist.
- Use timestamps to target specific weak areas during review.

### Official Objectives
- Download the **"CompTIA Security+ Exam Objectives SY0-701"** PDF directly from the CompTIA website (free).
- This is the only document that guarantees what is on the exam. Check off each objective as you go.

### Practice Exams
- **Jason Dion** (Udemy) - Practice exams very close to the real exam level, highly recommended.
- **CompTIA CertMaster Practice** - Official, questions drawn from the same pool as the actual exam.
- **ExamCompass / MeasureUp** - Good complement for varied question phrasing.
- Aim for **85%+ on practice exams** before sitting the real thing.

---

## Personal Exam Tips

### General Strategy
> **75% practice, 25% memorization.** Understanding *why* a control exists beats memorizing its name. Security+ questions test reasoning, not recitation.

### Question Keywords to Watch For
Pay close attention to **absolute qualifier words** in question stems - they completely change the expected answer:

| Keyword | What it's asking |
|---|---|
| **MOST likely** | Pick the most probable cause or scenario |
| **BEST** | Pick the most appropriate solution given the constraints |
| **FIRST** | Pick what you do before anything else in the process |
| **LEAST** | Pick the option that minimizes something |
| **ONLY** | Eliminate options that apply to multiple cases |
| **ALWAYS / NEVER** | Watch for absolutes - they can be traps |

> Missing one of these keywords is the most common reason for getting a correct-looking answer wrong. Read every question twice before answering.

### Time Management on the 90 Minutes
- **MCQs:** **30 seconds maximum per question.** If you're stuck, flag it and move on. Never stay blocked on a single MCQ.
- **PBQs (Performance-Based Questions):** These are interactive questions (drag and drop, network simulations, log analysis). They take more time and **count for more points**.
  - Recommended strategy: skip PBQs on first pass and answer all MCQs first.
  - At 30 sec/MCQ you free up roughly 20-30 minutes for PBQs.
  - **Reserve 20 to 30 minutes at the end exclusively for PBQs** - these are the high-value questions you cannot rush.
- Never leave a question unanswered - there is no penalty for a wrong answer, just flag them to review at the top right.

### During Revision
- Run **timed practice exams from day one**, not just at the end.
- Analyze every wrong answer: understand *why* the correct answer is right and why the others are not.
- **Review acronyms regularly** - the exam loves testing the exact definition of an abbreviation. Use the [acronyms.md](./acronyms.md) file as a daily flashcard drill.
- **Practice PBQs specifically** - they appear at the start of the exam and catch many people off guard. Look for free PBQ simulators online and on Professor Messer's site.
- Know the **key numbers**: ports (22 SSH, 443 HTTPS, 3389 RDP...), CVSS score ranges, RTO/RPO definitions.

---

## Creating the GitHub Repo and Pushing This Content

### Step 1 - Create the repo on GitHub (actions on github.com)

1. Log in to **github.com**
2. Click **"New repository"** (green button top right or via github.com/new)
3. Fill in the fields:
   - **Repository name:** `comptia-secplus-sy0-701-notes`
   - **Description:** `Personal study notes for CompTIA Security+ SY0-701`
   - **Visibility:** Public or Private based on your preference
   - **Do NOT check** "Add a README file" (we already have one)
   - **Do NOT check** "Add .gitignore" or "Choose a license"
4. Click **"Create repository"**
5. GitHub shows a page with your repo URL, like: `https://github.com/YOUR_USERNAME/comptia-secplus-sy0-701-notes.git`

### Step 2 - Initialize and push from your machine

Open a terminal (PowerShell or Git Bash) in the `comptia-secplus-sy0-701` folder and run these commands in order:

```bash
# 1. Initialize the local Git repository
git init

# 2. Add all files to tracking
git add .

# 3. First commit
git commit -m "Initial commit: CompTIA Security+ SY0-701 study notes"

# 4. Rename the main branch to 'main'
git branch -M main

# 5. Link the local repo to GitHub
#    (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/comptia-secplus-sy0-701-notes.git

# 6. Push content to GitHub
git push -u origin main
```

If GitHub asks for authentication, use a **Personal Access Token (PAT)** instead of your password:
Profile > Settings > Developer settings > Personal access tokens > Generate new token (scope: `repo`).

### Step 3 - Future updates

Each time you modify or add notes:

```bash
git add .
git commit -m "Update: description of the change"
git push
```

---

*Cybersecurity Enthusiast | Blue Team | Detection & Response*

Licensed under the [MIT License](./LICENSE).
