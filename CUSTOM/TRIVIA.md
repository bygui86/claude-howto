
# TRIVIA

## General

N/A

---

## Memory

- Q: How to edit "./CLAUDE.md" or "~/.claude/CLAUDE.md" from prompt?
  A: `TODO`
  Explanation:
    `TODO`
  Example:
    `TODO`
  Notes:
    - "Remember" and "#" go by default to auto-memory

- Q: Can a lower-priority memory tier override a higher one?
  A: No — higher tiers always take precedence
  Explanation:
    The memory hierarchy is strictly ordered. Managed Policy always beats Project Memory, which
    always beats User Memory, and so on down to Auto Memory. Lower tiers add context, they don't override.

- Q: You work across two repositories and want Claude to load CLAUDE.md from both. What flag do you use?
  A: --add-dir flag
  Explanation:
    The --add-dir flag allows Claude Code to load CLAUDE.md files from additional directories beyond the current working directory. 
    This is useful for monorepos or multi-project setups where context from other directories is relevant.
  Example
    `claude --add-dir /path/to/other/project`

---

## Skills

- Q: How do you inject live shell output into a skill's prompt?
  A: !`command`
  Explanation:
    Claude Code uses its own syntax for dynamic context injection. $(command) is evaluated by the
    shell when you type it, not by Claude Code at skill execution time. The !`command` syntax tells Claude Code
    to run the command and inject its output when the skill is loaded.
  Example:
    ```markdown
    ---
    name: commit
    description: Create a git commit with context
    allowed-tools: Bash(git *)
    ---
    
    ## Context
    
    - Current git status: !`git status`
    - Current git diff: !`git diff HEAD`
    - Current branch: !`git branch --show-current`
    - Recent commits: !`git log --oneline -5`
    
    ## Your task
    
    Based on the above changes, create a single git commit.
    ```

---

## Plugins

N/A

---

## Sandbox

N/A
