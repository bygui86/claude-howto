
## 🔵 Level 2: Intermediate — Building Workflows

**For**: Users with 3-5 quiz checks
**Time**: ~5 hours
**Focus**: Automation, integration, task delegation
**Outcome**: Automated workflows, external integrations, ready for Level 3

### Prerequisites Check

Before starting Level 2, make sure you're comfortable with these Level 1 concepts:

- [ ] Can create and use slash commands ([01-slash-commands/](../01-slash-commands/))
- [ ] Have set up project memory via CLAUDE.md ([02-memory/](../02-memory/))
- [ ] Know how to create and restore checkpoints ([08-checkpoints/](../08-checkpoints/))
- [ ] Can use `claude` and `claude -p` from the command line ([10-cli/](../10-cli/))

> **Gaps?** Review the linked tutorials above before continuing.

---

### Milestone 2A: Automation (Skills + Hooks)

**Topics**: Skills + Hooks
**Time**: 2-3 hours
**Complexity**: ⭐⭐ Intermediate
**Goal**: Automate common workflows and quality checks

#### What You'll Achieve
✅ Auto-invoke specialized capabilities with YAML frontmatter (including `effort` and `shell` fields)
✅ Set up event-driven automation across 28 hook events
✅ Use all 5 hook types (command, http, mcp_tool, prompt, agent)
✅ Enforce code quality standards
✅ Create custom hooks for your workflow

#### Hands-on Exercises

```bash
# Exercise 1: Install a skill
cp -r 03-skills/code-review ~/.claude/skills/

# Exercise 2: Set up hooks
mkdir -p ~/.claude/hooks
cp 06-hooks/pre-tool-check.sh ~/.claude/hooks/
chmod +x ~/.claude/hooks/pre-tool-check.sh

# Exercise 3: Configure hooks in settings
# Add to ~/.claude/settings.json:
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Bash",
        "hooks": [
          {
            "type": "command",
            "command": "~/.claude/hooks/pre-tool-check.sh"
          }
        ]
      }
    ]
  }
}
```

#### Success Criteria
- [ ] Code review skill automatically invoked when relevant
- [ ] PreToolUse hook runs before tool execution
- [ ] You understand skill auto-invocation vs. hook event triggers

#### Next Steps
- Create your own custom skill
- Set up additional hooks for your workflow
- Read: [03-skills/README.md](../03-skills/README.md)
- Read: [06-hooks/README.md](../06-hooks/README.md)

> **Check your understanding**: Run `/lesson-quiz skills` or `/lesson-quiz hooks` to test your knowledge before moving on.

---

### Milestone 2B: Integration (MCP + Subagents)

**Topics**: MCP + Subagents
**Time**: 2-3 hours
**Complexity**: ⭐⭐⭐ Intermediate+
**Goal**: Integrate external services and delegate complex tasks

#### What You'll Achieve
✅ Access live data from GitHub, databases, etc.
✅ Delegate work to specialized AI agents
✅ Understand when to use MCP vs. subagents
✅ Build integrated workflows

#### Hands-on Exercises

```bash
# Exercise 1: Set up GitHub MCP
export GITHUB_TOKEN="your_github_token"
claude mcp add github -- npx -y @modelcontextprotocol/server-github

# Exercise 2: Test MCP integration
# In Claude Code: /mcp__github__list_prs

# Exercise 3: Install subagents
mkdir -p .claude/agents
cp 04-subagents/*.md .claude/agents/
```

#### Integration Exercise
Try this complete workflow:
1. Use MCP to fetch a GitHub PR
2. Let Claude delegate review to code-reviewer subagent
3. Use hooks to run tests automatically

#### Success Criteria
- [ ] Successfully query GitHub data via MCP
- [ ] Claude delegates complex tasks to subagents
- [ ] You understand the difference between MCP and subagents
- [ ] Combined MCP + subagents + hooks in a workflow

#### Next Steps
- Set up additional MCP servers (database, Slack, etc.)
- Create custom subagents for your domain
- Read: [05-mcp/README.md](../05-mcp/README.md)
- Read: [04-subagents/README.md](../04-subagents/README.md)
- **Ready for Level 3!** Proceed to [Milestone 3A](LEARNING-ROADMAP_LEVEL-3.md#milestone-3a-advanced-features)

> **Check your understanding**: Run `/lesson-quiz mcp` or `/lesson-quiz subagents` to verify you're ready for Level 3.
