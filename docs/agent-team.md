# Agent team

The custom agent team orchestrating Mona's Project Pulse dashboard uses GitHub Copilot CLI in a Codespace to coordinate specialized AI agents working together toward a unified goal.

## Team members

### Orchestrator
- **Model**: Claude Opus 4.7
- **Definition**: `.github/agents/orchestrator.agent.md`
- **Responsibility**: Coordinates the entire agent team, breaking down complex requests into tasks, delegating work to specialists, and ensuring the integrated result is cohesive. Acts as the project orchestrator managing phases, file scopes, and dependencies.

### Planner
- **Model**: Claude Opus 4.7
- **Definition**: `.github/agents/planner.agent.md`
- **Responsibility**: Creates comprehensive implementation plans by researching the codebase, documentation, and dependencies. Produces ordered implementation steps, file assignments, edge case analysis, and validation strategies without writing code.

### Coder
- **Model**: GPT-5.5
- **Definition**: `.github/agents/coder.agent.md`
- **Responsibility**: Implements code-oriented tasks with clear structure, explicit errors, and testable behavior. Writes production-ready code, fixes bugs, creates support configuration files (like `.vscode/launch.json`), and validates changes before reporting completion.

### Designer
- **Model**: Gemini 3.1 Pro
- **Definition**: `.github/agents/designer.agent.md`
- **Responsibility**: Handles all UI/UX work including accessibility, information architecture, interaction flow, and visual design. Creates a polished dashboard with visible project cards, status badges, responsive layout, and consistent product patterns.

## Orchestration approach

Working in GitHub Copilot CLI within a Codespace, the Orchestrator sequences agent work by parsing plans into phases, managing file scope assignments, running tasks in parallel when possible, and ensuring dependencies are respected. Each specialist agent operates within an explicit scope and reports progress, keeping the user informed throughout the build process.
