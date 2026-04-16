# app-planner — Claude Code Skill

> Plan any app meticulously before writing a single line of code.

A Claude Code skill that runs a structured planning session before any build starts.
It interviews you, challenges assumptions, defines your stack, models your data, and
produces a complete documentation folder — ready to hand directly to Claude Code.

---

## What it does

Instead of jumping straight into code, `app-planner` walks you through 9 planning phases:

1. **Problem & Purpose** — who, what, why, scale
2. **Features & User Stories** — brain-dump → MVP scope → user stories by role
3. **Tech Stack** — opinionated recommendation with tradeoffs + full cost table
4. **Data Model** — full Postgres schema, relationships, flags for sensitive data
5. **Security** — auth model, permissions, non-negotiables
6. **Architecture** — folder structure + rules for CLAUDE.md
7. **Documentation** — writes all 8 files automatically
8. **Roadmap** — exact Claude Code sessions with copy-paste start prompts

**No code is written during this skill. Only plans.**

---

## Output

After running, you'll have:

| File | Purpose |
|---|---|
| `docs/SPEC.md` | Master project spec |
| `docs/USER_STORIES.md` | All user stories by role |
| `docs/DATA_MODELS.md` | Full database schema |
| `docs/TECH_STACK.md` | Every tech choice + rationale + cost |
| `docs/SECURITY_PLAN.md` | Auth, permissions, risk surface |
| `docs/DEVELOPMENT_PLAN.md` | Phased build plan |
| `README.md` | Project README |
| `CLAUDE.md` | Claude Code standing instructions |
| `ROADMAP.md` | Ordered session plan with prompts |

---

## Install

```bash
# Via npx
npx skills add natalietill/app-planner

# Or manually — global (all projects)
git clone https://github.com/natalietill/app-planner ~/.claude/skills/app-planner

# Or project-level
git clone https://github.com/natalietill/app-planner .claude/skills/app-planner
```

---

## Usage

Once installed, trigger it in Claude Code by saying anything like:

- *"I want to build an app that..."*
- *"Help me plan a new project"*
- *"I have an idea for a tool"*
- *"/app-planner"*

The skill will interview you before anything gets built.

---

## Tech stack coverage

The skill covers opinionated defaults for:

- **Web**: Next.js + Vercel + Supabase + Clerk + Tailwind + Shadcn/ui
- **Mobile**: React Native + Expo
- **AI-powered apps**: Anthropic SDK / Vercel AI SDK + pgVector
- **Backend-only**: TypeScript + Bun + Fastify, or Python + FastAPI
- **Payments**: Stripe
- **Email**: Resend

---

## Philosophy

> Spend 3–4x more time planning than building. This is the right ratio.

Built from lessons in [The Art of Gathering](https://priyaparker.com/book-art-of-gathering),
the [PDF guide by Carter Dean](https://github.com/carterdea), and months of vibe coding across multiple projects.

---

## License

MIT
