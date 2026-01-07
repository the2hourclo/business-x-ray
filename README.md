# Business X-Ray

**Map, diagnose, and optimize your business operations through progressive visual analysis.**

Transform your business into clear visual diagrams that reveal bottlenecks, automation opportunities, and growth paths.

---

## What You Get

| Output | Description |
|--------|-------------|
| **Business Map** | 7-column snapshot of your entire business (Traffic, Converters, Products, Funnels, Math, Team, Goals) |
| **Bow-Tie Funnel** | Customer journey from Awareness → Conversion → Results with key metrics |
| **Process Swimlanes** | 3-level drill-down showing WHO does WHAT with WHICH systems |
| **Opportunity Roadmap** | Prioritized action plan based on identified bottlenecks |

---

## Quick Start

### Option 1: GitHub Codespaces (Recommended for Beginners)

**No setup required. Start in 2 minutes.**

**Prerequisites:** A free [GitHub account](https://github.com/signup). That's it - no need to create your own repository.

**To try it out (read-only):**
1. Click the green **"Code"** button above
2. Select **"Open with Codespaces"** → **"New codespace"**
3. Wait for the environment to load (~1 min)
4. Install the **Claude Code extension** from the Extensions panel
5. Connect your Claude account when prompted
6. Say: **"Let's do a business x-ray"**

**To save your diagrams permanently:**
1. First, click **"Fork"** (top right) to create your own copy
2. Then open Codespaces from YOUR fork
3. Your diagrams will save to your fork's `diagrams/` folder
4. Commit changes: Claude will offer to commit, or use `git push`

> **Why fork?** Codespaces on my repo is read-only for you. Forking gives you your own copy where diagrams persist. You can also download `.drawio` files directly without forking.

### Option 2: Install as Plugin (Recommended for Existing Claude Code Users)

**Get automatic updates when new features are released.**

```bash
claude plugins install https://github.com/the2hourclo/business-x-ray
```

Then just say: **"Let's do a business x-ray"**

The plugin syncs with this repo - when I push updates, you get them automatically.

### Option 3: Clone the Repo (For Customization)

**Best if you want to modify the skill or contribute.**

```bash
git clone https://github.com/the2hourclo/business-x-ray.git
cd business-x-ray
claude "Let's do a business x-ray"
```

To get updates: `git pull origin master`

---

## Connect Draw.io to GitHub

Your diagrams save to the `diagrams/` folder. Sync them with Draw.io:

1. Go to [app.diagrams.net](https://app.diagrams.net)
2. Click **File → Open from → GitHub**
3. Authorize with your GitHub account
4. Select this repository
5. Your diagrams will sync automatically!

---

## How It Works

### The Interview Process

Claude acts as a business consultant, asking one question at a time:

1. **Business Map** - Extracts your traffic sources, products, funnels, team, and goals
2. **Bow-Tie Funnel** - Maps your customer journey from discovery to results
3. **Lead Gen Process** - Drills into how you generate and qualify leads
4. **Sales Process** - Maps discovery → presentation → proposal → close
5. **Fulfillment** - Maps onboarding → delivery → support → results

### 3-Level Drill-Down

| Level | Shows | Example |
|-------|-------|---------|
| **Level 1** | WHO does the work | Owner creates content, AI distributes, Team handles support |
| **Level 2** | WHICH systems handle it | ConvertKit for email, Calendly for booking, Notion for CRM |
| **Level 3** | HOW each system works | Step-by-step execution with tool names |

### Opportunity Discovery

As you map your business, Claude identifies:

- **Bottlenecks** (Red) - Steps slowing everything down
- **Automate** (Orange) - AI/tools could handle this
- **High Value** (Green) - Keep doing this yourself
- **Digital Assets** (Purple) - Templates/SOPs needed

---

## Folder Structure

```
business-x-ray/
├── README.md                    ← You are here
├── diagrams/                    ← Your .drawio files go here (syncs with Draw.io)
│   └── .gitkeep
└── .claude/
    └── skills/
        └── business-x-ray/
            ├── SKILL.md         ← Main skill file
            ├── references/      ← Supporting docs
            │   ├── bowtie-funnel.md
            │   ├── business-archetypes.md
            │   ├── drawio-standards.md
            │   ├── opportunity-categories.md
            │   └── swimlane-templates.md
            ├── workflows/       ← Step-by-step guides
            │   ├── progressive-interview.md
            │   ├── expand-process.md
            │   ├── generate-roadmap.md
            │   └── scan-diagram.md
            └── examples/        ← Templates
                ├── example-business-map.xml
                └── example-progress-state.yaml
```

---

## Using with Claude Web App

### Option A: Upload the ZIP

1. Download `business-x-ray.zip` from this repo
2. Upload it to Claude at the start of your conversation
3. Say "Let's do a business x-ray"

### Option B: Copy SKILL.md Content

1. Open `.claude/skills/business-x-ray/SKILL.md`
2. Copy the entire content
3. Paste it into Claude with: "Use this skill to help me map my business"

### Saving Diagrams

When Claude generates XML for a diagram:

1. Copy the XML code block
2. Go to [app.diagrams.net](https://app.diagrams.net)
3. File → New → Create
4. Arrange → Insert → Advanced → XML
5. Paste the XML
6. File → Save to → GitHub
7. Select your repo's `diagrams/` folder

---

## Resume Later

Claude provides a YAML progress block you can save:

```yaml
# Business X-Ray Progress - Copy this to resume later
stage: phase_3_process
business_type: coach
business_map_complete: true
bowtie_complete: true
pain_points: [content_creation, sales_calls]
selected_process: lead_generation
expanded_processes: []
pending: [sales_process, fulfillment]
opportunities_flagged: 3
last_updated: 2024-01-15
```

To resume:
1. Start a new Claude conversation
2. Paste the progress block
3. Say "Continue my Business X-Ray"

---

## For Developers (Claude Code CLI)

If you have Claude Code installed:

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/business-x-ray.git
cd business-x-ray

# Start the X-Ray
claude "Let's do a business x-ray"
```

Claude Code will:
- Generate .drawio files directly in `diagrams/`
- Track progress automatically
- Use sub-agents for efficient diagram generation

---

## Install as Claude Plugin

You can install Business X-Ray as a permanent skill in Claude Code so it's always available.

### Option 1: Install from GitHub (Recommended)

```bash
# Install directly from GitHub
claude plugins install https://github.com/the2hourclo/business-x-ray
```

The skill will be available in all your Claude Code sessions.

### Option 2: Install from Local Clone

```bash
# Clone the repo first
git clone https://github.com/the2hourclo/business-x-ray.git

# Install from local directory
claude plugins install ./business-x-ray
```

### Verify Installation

```bash
# List installed plugins
claude plugins list
```

You should see `business-x-ray` in the list.

### Using the Plugin

Once installed, just say:

```
Let's do a business x-ray
```

Or any of these trigger phrases:
- "Map my business"
- "Identify bottlenecks"
- "Visualize my business"
- "Process improvement"

Claude will automatically load the skill and guide you through the interview.

### Uninstall

```bash
claude plugins uninstall business-x-ray
```

---

## Business Types Supported

| Type | Typical Flow |
|------|--------------|
| **Coach** | YouTube → Email → Call → High-ticket |
| **Course Creator** | Content → Lead Magnet → Webinar → Course |
| **Agency** | Referrals → Proposal → Retainer |
| **SaaS** | Content → Trial → Subscription |
| **Service Provider** | Referrals → Call → Proposal → Retainer |
| **Creator** | Platform → Subscribe → Products |

---

## Need Help?

- **Questions about the skill**: Open an issue in this repo
- **General Claude questions**: [Claude Help Center](https://support.anthropic.com)
- **Draw.io questions**: [Draw.io Documentation](https://www.drawio.com/doc/)

---

## Credits

Created by [Rashid Khamis](https://rashidkhamis.com) | [The 2-Hour CLO](https://the2hourclo.com)

Built with [Claude Code](https://claude.ai/claude-code)
