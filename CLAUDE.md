# Claude Code Configuration

## Git Commit Rules

- Follow [Conventional Commits](https://www.conventionalcommits.org/) specification
- Format: `<type>(<scope>): <description>`
- Types: feat, fix, docs, style, refactor, perf, test, build, ci, chore, revert
- Keep commit message to ONE line in most cases, only use multi-line for large feature implementations
- Keep message concise but meaningful (e.g., "add hands-on projects roadmap" not "update TODO")
- Use imperative mood, not third person (e.g., "add" not "adds")
- Skip trivial changes in message (e.g., don't mention gitignore updates)
- Do NOT use emojis in commit messages
- Do NOT add Claude Code attribution or Co-Authored-By lines
- Only squash/amend when user explicitly requests it
- When user says "squash", default to amending the last commit; user will specify if more commits needed

## GUIDE.md Documentation Rules

- Each subproject has its own GUIDE.md (already gitignored)
- Include official framework class hierarchy at the beginning
- Focus on teaching implementation details, not just listing tasks
- Include: package structure, class definitions, method signatures, implementation details
- Provide detailed explanations, not just code snippets
- No "phase" style formatting (e.g., "Phase 1: xxx")
- Code examples should have thorough comments explaining the logic

## General Rules

- Never use emojis in any responses or generated content
- Response in Chinese or English based on user's language
