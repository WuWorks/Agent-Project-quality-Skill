# Project Quality Governance 🧭

> An open-source quality governance tool for Codex and engineering agents, ensuring that technical specifications, bug/optimisation logs and verification processes remain clear, searchable and traceable.

It condenses the documentation governance methods of mature engineering teams into a lightweight workflow: **first read the core rules, then pinpoint the relevant tasks, and finally complete verification based on risk**. This reduces unnecessary context and redundant checks, whilst ensuring project history is not overwritten and no evidence is fabricated.

## ✨ Why it’ worth using

- 🛡️ **Core rules first**: 安全, data, permissions, scope and validation thresholds are always at the top of the specifications.
- 🎯 **Precise task-based reading**: Through directory and task routing, only the sections truly required for the current task are loaded.
- 🧠 **Control context overhead**: Establish clear limits for entry files, activity logs and terminal output.
- 🐞 **Divide and conquer bugs and optimisations**: The two types of records have different fields whilst sharing a unified status index.
- 🗂️ **Separation of activity logs and historical archives**: Keep day-to-day development lightweight; retrieve records by ID only when traceability is required.
- 🧪 **L1 / L2 / L3 tiered validation**: Select the level of validation based on actual risk, rather than running a full check every time.
- 🔍 **Automated Consistency Checks**: Verify the uniqueness of title hierarchies, IDs, fields, evidence, timestamps and archiving.
- 📌 **Respect Project Facts**: Preserve history, correct relationships and substitute relationships; do not fabricate timestamps or test evidence.
- 🌍 **语言 Adaptation**: Generate corresponding specifications based on the target project language, suitable for different teams and engineering environments.

## ⚙️ How It Works

```text
📦 Inspect the existing repository
        ↓
🛡️ Extract the core rules that must be read every time
        ↓
🗺️ Establish a ‘Task 类型 → Mandatory Sections’ routing system
        ↓
📝 Standardise bug/optimisation records and activity indices
        ↓
🧪 Select L1 / L2 / L3 acceptance checks based on risk
        ↓
🔍 Run read-only validator
        ↓
✅ Output a maintainable, traceable quality governance system
```

### 📖 Progressive Reading

```markdown
Daily tasks: Core rules + current module chapters + activity logs

Historical review: Retrieve corresponding archives by ID or keyword

Release phase: Review release candidates + perform full L3 acceptance testing
```

This structure prevents the Agent from having to rescan the entire specification and all historical data each time, making the development process more linear:

```text
Identify → Modify → Targeted verification → Record results → Deliver
```

## 🚀 Quick Start

### 1. Obtain the Skill

```bash
git clone https://github.com/WuWorks/Agent-Project-quality-Skill.git
```

Copy the repository folder to the Codex skills directory and restart Codex. Alternatively, you can read `SKILL.md` directly to understand the full scope of application.

### 2. Usage Example

```text
Use `project-quality-governance` to review and optimise the current project’ technical specifications, bug/optimisation logs and validation processes.
```

The Skill will first examine the existing structure, then fill in the governance framework with minimal changes; it will not arbitrarily rewrite the project’ history.

## 🧪 Tiered Acceptance Model

| Level | Applicable Scenarios | Typical Validation |
| --- | --- | --- |
| 🟢 L1 | Copy, styling, and minor documentation adjustments | Difference checks and confirmation of affected content |
| 🟡 L2 | Modifications to the logic or structure of a single module | Relevant testing; build execution where necessary |
| 🔴 L3 | High-risk changes or production release boundaries | Comprehensive testing, checks, build and delivery acceptance |

> A Git commit does not automatically escalate to L3; the validation level is determined by the actual risk.

## 🔍 Documentation Validator

The validator only reads explicitly specified files and outputs diagnostics; it **does not automatically modify project documentation**:

```bash
node scripts/validate-quality-docs.mjs \
  --spec path/to/technical-spec.md \
  --log path/to/active-log.md \
  --archives path/to/archive-1.md,path/to/archive-2.md \
  --agents path/to/agent-entrypoint.md \
  --workflow path/to/workflow.md
```

Configuration is available via `--config path/to/config.json`:

- 🆔 Bug and optimisation ID prefixes
- 🏷️ 类型 and content 标签
- ✅ Completion status and mandatory evidence
- 📣 Requirements for release copy
- 📚 Maximum number of activity records
- 📏 Entry file and context budget
- 🧱 Heading hierarchy and section numbering rules

Run the validator test:

```bash
node --test scripts/validate-quality-docs.test.mjs
```

## 🗂️ Project structure

```text
project-quality-governance/
├─ SKILL.md                         # Skill entry point and task routing
├─ README.md                        # Open-source project description
├─ CHANGELOG.md                     # Version update log
├─ LICENSE                          # Apache-2.0
├─ agents/
│  └─ openai.yaml                   # Agent profile information
├─ references/
│  ├─ technical-spec-architecture.md
│  ├─ issue-and-improvement-log.md
│  └─ verification-workflow.md
└─ scripts/
   ├─ validate-quality-docs.mjs
   └─ validate-quality-docs.test.mjs
```

## ✅ Scope of Application

Suitable for:

- Creating, reviewing or refactoring technical specifications
- Maintaining bug and optimisation logs
- Designing tiered acceptance and development processes
- Managing agent context and verification costs
- Checking the structure and factual consistency of engineering documentation

Not suitable for:

- 常规 marketing copy
- Unstructured, off-the-cuff notes
- Content editing unrelated to engineering quality governance

## 🔐 隐私 and Limitations

- Does not require the upload of project files.
- Does not access unauthorised private research, keys or sensitive materials.
- It does not fabricate historical dates, responsible parties or validation evidence for the sake of completing documentation.
- The validation script performs read-only checks and does not automatically rewrite user documents.

## 📦 Versions and Licence

- 🏷️ [View 发布](https://github.com/WuWorks/Agent-Project-quality-Skill/releases)
- 📝 [View the changelog](CHANGELOG.md)
- ⚖️ Released as open source under the [Apache Licence 2.0](LICENSE)

If this Skill helps with your collaborative projects, please feel free to ⭐ star it, raise an issue or contribute to its improvement.
