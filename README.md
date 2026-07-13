# Cognitive Check Skill

Cognitive Check is a reusable skill for ChatGPT and Codex. It evaluates whether a document, memo, strategy, plan, claim set, deck, transcript, report, recommendation, or draft is trustworthy, well-reasoned, appropriately scoped, honestly uncertain, and ready to use.

It helps you:

- separate verified facts from interpretations and assumptions;
- identify load-bearing claims, evidence gaps, bias, causal leaps, and scope risks;
- map arguments and surface missing objections;
- examine source quality, independence, diversity, and fit;
- generate alternative hypotheses and an assumption ledger;
- turn findings into a prioritized upgrade plan;
- optionally produce structured HTML and PDF reports.

## Download

[Download the latest `cognitive-check-skill.zip`](https://github.com/bchallamel/cognitive-check-skill/releases/latest/download/cognitive-check-skill.zip).

## Install in ChatGPT Work

If Skills are enabled in your ChatGPT Work workspace:

1. Open your profile menu and select **Skills**.
2. Select **New skill** and then **Upload from computer**.
3. Upload `cognitive-check-skill.zip`.
4. Review the skill instructions before installing it.

## Install in a Codex project

Unzip the download and place the `cognitive-check` folder here:

```text
your-project/
  .agents/
    skills/
      cognitive-check/
        SKILL.md
        agents/
        references/
```

Restart or reload Codex if the skill does not appear immediately.

## Use

Attach or identify an artifact, then start with:

```text
Use $cognitive-check to evaluate this artifact for claim validity, reasoning quality, assumptions, evidence, and upgrade steps.
```

Ask for a **full cognitive check** when you want the complete report. Ask for an **HTML report** or **PDF report** when you want a shareable visual output.

## What is included

```text
cognitive-check/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── report-architecture.md
    └── report-rendering.md
```

The skill contains editable Markdown instructions and reference files. It contains no executable code, credentials, or external connections.

## Important note

Cognitive Check supports better judgment; it does not replace qualified professional advice or human accountability. Verify consequential claims and decisions against appropriate primary sources and experts.

## License

MIT License. See [LICENSE](LICENSE).
