# Flat & Fast

A single `CLAUDE.md` file with your brand context, plus skill files for specialized tasks.

## Who this is for

This template works best for **solo marketers or small teams (1–5 people)** who wear many hats and don't have rigid role boundaries. If one person handles email, social, and blog — or if your whole marketing org fits in a single Slack channel — this is your starting point.

## When to Use This

- Your team is small (1-5 people)
- You want a single source of truth with no nesting complexity
- You'd rather iterate on one file than maintain a hierarchy
- Your brand guidelines are straightforward enough to fit in one document

## When to Consider a Different Template

- You have multiple brands or sub-brands with distinct voices
- Different teams (product marketing, growth, content, PR) need isolated contexts
- Your guidelines exceed ~2,000 lines and become hard to navigate
- You need role-based access to different sections

## How to Use

1. **Clone this repo** into your project or marketing workspace
2. **Open `CLAUDE.md`** and replace every `[Bracketed Placeholder]` with your brand info — start with Brand Identity, Voice, and Audiences
3. **Customize the skill files** in `skills/` — delete any you don't need, edit the rest to match your channels and tools
4. **Run your AI agent** from this directory — it reads `CLAUDE.md` automatically and references skills as needed
5. **Iterate** — when the agent gets something wrong, update the relevant file. These docs are living guidelines, not a one-time setup.

## File Structure

```
├── CLAUDE.md                          # The single root guide — brand, voice, audiences, rules
├── README.md                          # You are here
└── skills/
    ├── social-media/
    │   └── SKILL.md                   # Platform-specific social media rules
    ├── email-campaigns/
    │   └── SKILL.md                   # Email marketing guidance
    ├── seo-content/
    │   └── SKILL.md                   # SEO writing and optimization
    └── analytics-reporting/
        └── SKILL.md                   # Data pulling, reporting, attribution
```

## How It Works

1. **`CLAUDE.md`** is loaded automatically whenever an agent operates in this directory. It contains your brand identity, voice guidelines, audience definitions, legal guardrails, and pointers to skills.

2. **Skills** are specialized instruction sets that agents reference for specific tasks. When someone asks for a tweet or an email campaign, the relevant skill file provides task-specific rules on top of the base context in `CLAUDE.md`.

## Getting Started

### Step 1: Customize `CLAUDE.md`

Open `CLAUDE.md` and replace every `[Bracketed Placeholder]` with your actual brand information. Look for `<!-- TODO: -->` comments for additional guidance on what to fill in.

**Start with these sections — they have the highest impact:**
- Brand Identity (your name, mission, pitch)
- Brand Voice & Tone (how you sound)
- Target Audiences (who you're talking to)
- Terminology & Language (words you use and avoid)

### Step 2: Customize the Skills

Each skill file in `skills/` follows the same pattern: structured guidance with placeholders. Customize them based on which channels you actively use. Delete any skill directories you don't need.

### Step 3: Test It

Ask the agent to perform tasks and evaluate the output against your brand standards:

- "Write three LinkedIn posts announcing [product feature]"
- "Draft a nurture email sequence for [audience segment]"
- "Create a blog outline targeting the keyword [keyword]"
- "Summarize last month's campaign performance"

If the output doesn't match your expectations, update the relevant section in `CLAUDE.md` or the skill file. This is an iterative process.

### Step 4: Share With Your Team

Commit this to your team's repo. Everyone working with an agent in this directory gets the same brand context automatically.

## Tips

- **Be specific over general.** "We use short, punchy sentences. Max 15 words." beats "Keep it concise."
- **Include real examples.** Before/after pairs in your voice guide teach agents more than abstract rules.
- **Update regularly.** When your messaging evolves, update the files. Stale guidelines produce stale output.
- **Add more skills as needed.** Creating a new skill is as simple as adding a `skills/[task-name]/SKILL.md` file and referencing it in `CLAUDE.md`.

## License

MIT License. Use this template however you like.
