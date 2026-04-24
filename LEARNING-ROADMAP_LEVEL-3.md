
## 🔴 Level 3: Advanced — Power User & Team Lead

**For**: Users with 6-8 quiz checks
**Time**: ~5 hours
**Focus**: Team tooling, CI/CD, enterprise features, plugin development
**Outcome**: Power user, can set up team workflows and CI/CD

### Prerequisites Check

Before starting Level 3, make sure you're comfortable with these Level 2 concepts:

- [ ] Can create and use skills with auto-invocation ([03-skills/](03-skills/))
- [ ] Have set up hooks for event-driven automation ([06-hooks/](06-hooks/))
- [ ] Can configure MCP servers for external data ([05-mcp/](05-mcp/))
- [ ] Know how to use subagents for task delegation ([04-subagents/](04-subagents/))

> **Gaps?** Review the linked tutorials above before continuing.

---

### Milestone 3A: Advanced Features

**Topics**: Advanced Features (Planning, Permissions, Extended Thinking, Auto Mode, Channels, Voice Dictation, Remote/Desktop/Web)
**Time**: 2-3 hours
**Complexity**: ⭐⭐⭐⭐⭐ Advanced
**Goal**: Master advanced workflows and power user tools

#### What You'll Achieve
✅ Planning mode for complex features
✅ Fine-grained permission control with 6 modes (default, acceptEdits, plan, auto, dontAsk, bypassPermissions)
✅ Extended thinking via Alt+T / Option+T toggle
✅ Background task management
✅ Auto Memory for learned preferences
✅ Auto Mode with background safety classifier
✅ Channels for structured multi-session workflows
✅ Voice Dictation for hands-free interaction
✅ Remote control, desktop app, and web sessions
✅ Agent Teams for multi-agent collaboration

#### Hands-on Exercises

```bash
# Exercise 1: Use planning mode
/plan Implement user authentication system

# Exercise 2: Try permission modes (6 available: default, acceptEdits, plan, auto, dontAsk, bypassPermissions)
claude --permission-mode plan "analyze this codebase"
claude --permission-mode acceptEdits "refactor the auth module"
claude --permission-mode auto "implement the feature"

# Exercise 3: Enable extended thinking
# Press Alt+T (Option+T on macOS) during a session to toggle

# Exercise 4: Advanced checkpoint workflow
# 1. Create checkpoint "Clean state"
# 2. Use planning mode to design a feature
# 3. Implement with subagent delegation
# 4. Run tests in background
# 5. If tests fail, rewind to checkpoint
# 6. Try alternative approach

# Exercise 5: Try auto mode (background safety classifier)
claude --permission-mode auto "implement user settings page"

# Exercise 6: Enable agent teams
export CLAUDE_AGENT_TEAMS=1
# Ask Claude: "Implement feature X using a team approach"

# Exercise 7: Scheduled tasks
/loop 5m /check-status
# Or use CronCreate for persistent scheduled tasks

# Exercise 8: Channels for multi-session workflows
# Use channels to organize work across sessions

# Exercise 9: Voice Dictation
# Use voice input for hands-free interaction with Claude Code
```

#### Success Criteria
- [ ] Used planning mode for a complex feature
- [ ] Configured permission modes (plan, acceptEdits, auto, dontAsk)
- [ ] Toggled extended thinking with Alt+T / Option+T
- [ ] Used auto mode with background safety classifier
- [ ] Used background tasks for long operations
- [ ] Explored Channels for multi-session workflows
- [ ] Tried Voice Dictation for hands-free input
- [ ] Understand Remote Control, Desktop App, and Web sessions
- [ ] Enabled and used Agent Teams for collaborative tasks
- [ ] Used `/loop` for recurring tasks or scheduled monitoring

#### Next Steps
- Read: [09-advanced-features/README.md](09-advanced-features/README.md)

> **Check your understanding**: Run `/lesson-quiz advanced` to test your mastery of power user features.

---

### Milestone 3B: Team & Distribution (Plugins + CLI Mastery)

**Topics**: Plugins + CLI Mastery + CI/CD
**Time**: 2-3 hours
**Complexity**: ⭐⭐⭐⭐ Advanced
**Goal**: Build team tooling, create plugins, master CI/CD integration

#### What You'll Achieve
✅ Install and create complete bundled plugins
✅ Master CLI for scripting and automation
✅ Set up CI/CD integration with `claude -p`
✅ JSON output for automated pipelines
✅ Session management and batch processing

#### Hands-on Exercises

```bash
# Exercise 1: Install a complete plugin
# In Claude Code: /plugin install pr-review

# Exercise 2: Print mode for CI/CD
claude -p "Run all tests and generate report"

# Exercise 3: JSON output for scripts
claude -p --output-format json "list all functions"

# Exercise 4: Session management and resumption
claude -r "feature-auth" "continue implementation"

# Exercise 5: CI/CD integration with constraints
claude -p --max-turns 3 --output-format json "review code"

# Exercise 6: Batch processing
for file in *.md; do
  claude -p --output-format json "summarize this: $(cat $file)" > ${file%.md}.summary.json
done
```

#### CI/CD Integration Exercise
Create a simple CI/CD script:
1. Use `claude -p` to review changed files
2. Output results as JSON
3. Process with `jq` for specific issues
4. Integrate into GitHub Actions workflow

#### Success Criteria
- [ ] Installed and used a plugin
- [ ] Built or modified a plugin for your team
- [ ] Used print mode (`claude -p`) in CI/CD
- [ ] Generated JSON output for scripting
- [ ] Resumed a previous session successfully
- [ ] Created a batch processing script
- [ ] Integrated Claude into a CI/CD workflow

#### Real-World Use Cases for CLI
- **Code Review Automation**: Run code reviews in CI/CD pipelines
- **Log Analysis**: Analyze error logs and system outputs
- **Documentation Generation**: Batch generate documentation
- **Testing Insights**: Analyze test failures
- **Performance Analysis**: Review performance metrics
- **Data Processing**: Transform and analyze data files

#### Next Steps
- Read: [07-plugins/README.md](07-plugins/README.md)
- Read: [10-cli/README.md](10-cli/README.md)
- Create team-wide CLI shortcuts and plugins
- Set up batch processing scripts

> **Check your understanding**: Run `/lesson-quiz plugins` or `/lesson-quiz cli` to confirm your mastery.
