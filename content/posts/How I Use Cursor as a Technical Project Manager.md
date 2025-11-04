+++
date = '2025-10-30T09:43:40-04:00'
draft = false
title = 'How I Use Cursor as a Technical Project Manager: A Step-by-Step'
+++

How I Use Cursor as a Technical Project Manager: A Step-by-Step
AI-Driven Workflow For the past two years, I've managed projects with an
AI-first, system-led mindset. I train my team to work the same way. At
our company, we use Cursor. It's the same tool our engineers and
technical specialists use daily, which already makes it a natural fit
for managing technical work. But it goes further. Cursor runs fast as a
desktop app, supports markdown with live previews, integrates directly
with Jira, Confluence, and Notion through MCPs, and gives me access to
multiple LLMs in one place. I don't have to jump between tools or
reformat the same content twice.

## Why Technical PMs Should Be Using Cursor

If you need to make the case for getting Cursor licenses for your
product or project management team, here's a clear list of reasons it's
worth it.

### Multi-Model Access

Cursor lets you access multiple LLMs - GPT-5, Claude, DeepSeek, etc. ---
and switch between them easily. This gives PMs flexibility to get
different responses, tones, or strengths from various models without
changing platforms.

### Built-In File System + Markdown Support

It provides a full file system interface, allowing you to work directly
with .md files: writing, storing, editing, and syncing them like a
developer would. As a PM, you can write your PRD, TDD, architecture
notes, etc., in markdown and see a live preview (with the Markdown
Preview Enhanced plugin).

### Speed & Desktop-Native

Unlike web tools, Cursor runs as a desktop app and is fast. That makes a
difference when you're writing, navigating files, or pushing/pulling
content to other tools.

### Integration via MCPs

Cursor connects directly to tools like Jira, Notion, Confluence, GitHub,
Figma, etc., all from within the same interface. You don't have to jump
between platforms or copy-paste.

### Source Control for Docs

PRDs and technical documents live inside the code repo (via Git). That's
a huge shift: you're working where the engineers work, using the same
tools and versioning everything.

### Fast Iteration with AI Agents + Context

You can set Cursor rules for how the AI should behave, like always
linking Jira tickets to epics or pulling comments from Confluence. These
rules let you scale repeatable tasks.

### A Shared Environment With Engineering

Cursor puts you in the same operational space as engineers. That shared
context makes collaboration smoother.

In this post, I'll walk through exactly how I use Cursor as a technical
project manager, step by step.

## Step 1: Set Up Cursor as Your Operating Environment

-   Install Cursor
-   Enable Markdown Preview Enhanced: Lets you view your docs as
    rendered content, not raw syntax.
-   Create a new folder per project, e.g., `/project-infra-revamp-q4/`
    -   `README.md` → Product Requirement Doc (PRD)
    -   `jira_tickets.md` → Task breakdowns
    -   `status_report.md` → Weekly async updates
    -   `architecture.md` → Flow diagrams and data interfaces

### Use the Three-Pane Layout

-   File explorer on the left
-   Markdown content (PRD, tickets, etc.) in the center
-   AI chat on the right

Set this up once. Every project runs in this structure.

## Step 2: Connect Cursor to the Right MCPs

Start by connecting Cursor to the tools you actually use on the project.
These integrations are called MCPs (Model Context Protocols), and they
let Cursor push and pull content across your entire workflow.

### Set up only what matters

You don't need everything. Just connect the MCPs that make sense for
your stack. For example, I usually enable: - Jira - Confluence -
Notion - GitHub - Figma

### Toggle MCPs based on your workflow

You don't have to keep everything on all the time. Cursor lets you
toggle MCPs on or off depending on what you're working on. For
example: - Writing tickets? Enable Jira only. - Reviewing a design spec?
Turn on Figma. - Publishing a doc? Enable Confluence or Notion.

Keep an eye on the green status light for each MCP. If something's not
syncing, it's usually because the MCP needs to be re-enabled.

## Step 3: Write the PRD in Markdown (Inside Cursor)

Structure your `README.md`, which is your PRD, like this:

``` markdown
# [Project Name]

## Summary
One paragraph clearly explaining what the project is and what outcome it drives.

## Scope
Define what’s in scope and what’s explicitly out of scope. List your connected MCPs and relevant tools.

## Architecture Overview
Describe the high-level system design or attach a diagram via markdown image links. Make this useful for engineers, designers, and reviewers.

## Component Breakdown
Use the same structure for each key component (or module):
- Name of component (e.g., Ingestion Pipeline, Model Scoring API)
- Owner
- Inputs and outputs
- Success criteria

## Timeline
Create a simple table or bullet list of major milestones and their deadlines.

## Risks and Mitigation
List 3–5 key risks and what you're doing to mitigate them.

## Communication Plan
Define how stakeholders will stay informed (e.g., async updates via `status_report.md`, weekly Jira summaries).
```

Once this is complete, commit the file to your Git repo. This becomes
the living source of truth for the project.

## Step 4: Push the PRD to Confluence or Notion

Once your PRD is ready in markdown, publish it using the Confluence or
Notion MCP. This allows other teams to view and comment without needing
access to Cursor or the Git repo.

### Use this process:

1.  Use Cursor to run the MCP push command
2.  The AI will generate a clean, formatted version in your chosen tool
3.  Add the link back to the original markdown doc for easy reference

**Pro tip:** Do this early, even with a rough draft. Share the published
link in your team's PRD channel to collect feedback asynchronously.

## Step 5: Generate Jira Tickets from Your PRD

Create a `jira_tickets.md` file and list your deliverables in plain text
under each component or epic.

Example:

``` markdown
## Component: Ingestion Pipeline
- Define schema
- Build ingestion job
- Validate outputs

## Component: Model Evaluation
- Create test harness
- Run accuracy benchmarks
```

Then prompt Cursor: \> "Convert this into Jira tickets. Include summary,
description, labels, epic link, and link to the PRD."

Cursor will: - Generate well-structured tickets with technical
descriptions - Link them to the right epics - Format them for Jira
import (CSV or API)

Once reviewed, import into Jira. Each component maps to an epic, and
each bullet becomes a story.

## Step 6: Automate Weekly Status Reports

Use the `status_report.md` to summarize project progress every week.
Cursor can generate the content using real-time data from Jira.

### Steps:

1.  Open `status_report.md`
2.  Prompt: \> "Generate a weekly status update from Jira. Group by
    epic. Include status, blockers, % done, and recent progress."

Cursor reads ticket history and outputs a readable update per component.
Paste the final update into Slack, Confluence, or email it to
stakeholders.

## Step 7: Monitor, Iterate, and Stay in Sync

Once setup is done, keep your project moving by: - Updating Jira daily -
Committing any PRD edits to Git - Regenerating status reports weekly -
Toggling MCPs as needed

With this setup, you're working in the same system as engineers, using
AI to eliminate busywork, and staying async by default. No context
switching. No double entry. Just execution at speed.
