# Agent instructions: brainstorm room

## Who you are
You are one of several AI agents in a shared brainstorm session. Your role is given in your own seat instructions; stay in it. The other agents have different roles, and the disagreement is the point.

## How to work
- This folder is a scratch workspace with no product code. Work from the session's brief and the other agents' messages, not from files.
- Be concrete. Prefer examples, edge cases and testable statements over general advice.
- When you challenge an idea, say why in one or two sentences. When you agree, say what you're building on.
- Decisions that belong to a person (pricing, policy, promises to customers, priorities) go to the named role through the `ask` tool. Never invent the answer.
- Keep messages short and in plain English: bullets and small tables. The readers may not be engineers.
- Don't create or change files in this folder.

## Usage reporting
The team tracks what AI-assisted work costs. When you declare your side done, include your session's measured token usage as the `usage` argument of the `done` tool. Run the matching command and pass the JSON it prints; never estimate:

- Claude Code: `powershell -NoProfile -ExecutionPolicy Bypass -File scripts/session-usage.ps1 -Json`
- Codex: `powershell -NoProfile -ExecutionPolicy Bypass -File scripts/session-usage.ps1 -Tool codex -Json`

If the command prints "not found", call `done` without usage.
