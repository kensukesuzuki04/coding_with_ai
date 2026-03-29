# Student Copilot Instructions

## Purpose

This guide explains how students should use GitHub Copilot in this course, why we use it, and how it supports learning.

## Why We Use Copilot

- To help you start coding tasks faster.
- To help you understand syntax and structure in Python and Quarto.
- To practice reading, testing, and improving generated code.
- To build debugging and problem-solving skills with support.

Copilot is a learning assistant, not a replacement for your own reasoning.

## What Students Should Do

### 1. Before class

- Sign in to GitHub in VS Code.
- Confirm Copilot is active.
- Open the class folder in VS Code.
- Review the assignment prompt before asking Copilot for help.

### 2. During coding

- Write your own problem statement first in plain language.
- Ask Copilot for a first draft of code.
- Read every suggested line before accepting it.
- Run the code in small steps.
- Check outputs and error messages.
- Revise prompts when results are incorrect or unclear.

### 3. After getting suggestions

- Explain the code in your own words.
- Add comments where logic is not obvious.
- Test edge cases and confirm results.
- Keep only code you understand.

## How Copilot Helps You

- Faster first draft of code and text.
- Better understanding of common coding patterns.
- Quicker troubleshooting when errors occur.
- More time to focus on interpretation and economic reasoning.
- Improved confidence for beginners.

## Good Prompt Examples

- Write Python code to load a CSV file and show the first 10 rows.
- Explain this error message and suggest two fixes.
- Create a Quarto section with a figure, table, and short interpretation.
- Refactor this code to be easier to read.

## Using Agent Roles (Reviewer, Coauthor)

### Why this matters

- Different tasks need different feedback styles.
- A `reviewer` role can focus on errors, logic gaps, and missing evidence.
- A `coauthor` role can focus on structure, clarity, and argument quality.
- Using role-specific instructions gives more consistent and useful responses.

### How to set up agents in a class folder

1. In your project folder, create `.github/agents/`.
2. Add a file for each role, for example:
	- `.github/agents/reviewer.agent.md`
	- `.github/agents/coauthor.agent.md`
3. Put clear instructions in each file (what to check, output format, tone).
4. Save files and reopen Copilot Chat if needed.

Minimal example for `coauthor.agent.md`:

```markdown
---
description: Coauthor feedback for economics writing and revisions
tools: ['codebase', 'editFiles', 'runCommands']
---

You are a coauthor for an economics writing assignment.
Give direct, constructive feedback.
Focus on argument, evidence, and clarity.
Return feedback with these sections:
1. What Works
2. Major Issues
3. Minor Issues
4. Next Steps
```

### How to use these agents

1. Open Copilot Chat in VS Code.
2. Select the custom agent role (for example `coauthor` or `reviewer`) if it appears in the chat mode or agent list.
3. If your setup exposes slash commands, run the role command (for example `/coauthor`).
4. Paste your draft or ask the agent to review the current file.
5. Revise your document based on the feedback and run the role again.

Tip: Use `coauthor` for draft improvement and `reviewer` for stricter checks before submission.

## Class Rules for Responsible Use

- You are responsible for all submitted work.
- Verify all code and outputs before submission.
- Do not submit AI-generated content that you cannot explain.
- Follow all course policies on collaboration and academic integrity.
- When required, disclose where Copilot assisted your work.

## Quick Workflow

1. Read the task.
2. Ask Copilot for a draft.
3. Run and test.
4. Debug and revise.
5. Explain results in your own words.

## Final Reminder

Use Copilot to learn actively. The goal is not just to finish code, but to understand the method, the output, and the economic meaning behind the result.
