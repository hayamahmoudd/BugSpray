## 🐞🪳🪲🐜🕷️🐛 Bu-bu-buuuuuuugin 🐛🕷️🐜🪲🪳🐞

**Automating the journey from Jira bug reports to GitHub pull requests, with developers staying in control.**

> **Note:** This project was developed within the FreshBooks organization during an AI hackathon. The source code is maintained in a private organizational repository and is not publicly available. This repository showcases the project's functionality and demo.

## Overview

Bug Spray is an AI-powered developer tool that automates bug resolution by integrating **Jira, GitHub, and Claude AI**.

Instead of manually investigating every bug report, locating the relevant code, implementing a fix, and creating a pull request, developers can review Jira tickets through a centralized dashboard and approve bugs for automated resolution.

Once approved, Bug Spray launches a Claude-powered agent that analyzes the issue, works within the target GitHub repository, and generates a draft pull request for human review.

## Key Features

- **Jira Integration:** Syncs bug reports from Jira into a centralized review dashboard.
- **AI-Powered Bug Fixing:** Uses Claude to analyze Jira tickets, investigate repository code, and generate proposed fixes.
- **Automated Pull Requests:** Creates GitHub draft PRs containing the proposed changes, problem descriptions, and reviewer notes.
- **Human-in-the-Loop Approval:** Developers approve or reject tickets before an AI agent can modify code.
- **Repository Validation:** Verifies GitHub repositories before starting an agent to prevent invalid or unauthorized runs.
- **Optional Code Scoping:** Allows developers to specify relevant files or directories to guide the agent.
- **Sequential Agent Execution:** Queues bug-fixing tasks to prevent overlapping agent runs and manage resource usage.
- **Duplicate Prevention:** Blocks repeated attempts to fix tickets that have already been processed.
- **Execution Controls:** Allows developers to stop an active agent and prevents stopped runs from pushing changes.
- **Workflow Tracking:** Tracks bugs through review, execution, blocked, and completed states, with Jira and GitHub integration.
- **Agent Safety Controls:** Restricts Claude's available tools, protects GitHub workflow configuration files, and requires human review before merging proposed fixes.

## How It Works

1. **Sync:** Import bug tickets from Jira into the dashboard.
2. **Review:** Inspect a ticket, select a GitHub repository, and optionally provide a file or directory scope.
3. **Approve:** Validate the repository and approve the ticket for AI-assisted resolution.
4. **Execute:** Queue a Claude agent to investigate the bug and generate a code fix.
5. **Create PR:** Open a draft pull request on GitHub with the proposed changes and a description of the fix.
6. **Review:** A developer reviews the draft PR before approving and merging it.

Developers can also reject tickets, stop active executions, and investigate blocked or failed runs.

## Tech Stack

- **Python:** Backend orchestration and agent execution
- **Claude AI / Claude CLI:** AI-powered code investigation and bug fixing
- **Jira REST API:** Bug ticket ingestion and workflow integration
- **GitHub CLI:** Repository operations and draft pull request creation

## Demo

[Watch the demo](bug-spray-demo.mp4)
