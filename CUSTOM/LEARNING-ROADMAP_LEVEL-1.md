
## 🟢 Level 1: Beginner — Getting Started

**For**: Users with 0-2 quiz checks
**Time**: ~3 hours
**Focus**: Immediate productivity, understanding fundamentals
**Outcome**: Comfortable daily user, ready for Level 2

### Milestone 1A: First Commands & Memory

**Topics**: Slash Commands + Memory
**Time**: 1-2 hours
**Complexity**: ⭐ Beginner
**Goal**: Immediate productivity boost with custom commands and persistent context

#### What You'll Achieve
✅ Create custom slash commands for repetitive tasks
✅ Set up project memory for team standards
✅ Configure personal preferences
✅ Understand how Claude loads context automatically

#### Hands-on Exercises

```bash
# Exercise 1: Install your first slash command
mkdir -p .claude/commands
cp 01-slash-commands/optimize.md .claude/commands/

# Exercise 2: Create project memory
cp 02-memory/project-CLAUDE.md ./CLAUDE.md

# Exercise 3: Try it out
# In Claude Code, type: /optimize
```

#### Success Criteria
- [ ] Successfully invoke `/optimize` command
- [ ] Claude remembers your project standards from CLAUDE.md
- [ ] You understand when to use slash commands vs. memory

#### Next Steps
Once comfortable, read:
- [01-slash-commands/README.md](../01-slash-commands/README.md)
- [02-memory/README.md](../02-memory/README.md)

> **Check your understanding**: Run `/lesson-quiz slash-commands` or `/lesson-quiz memory` in Claude Code to test what you've learned.

---

### Milestone 1B: Safe Exploration

**Topics**: Checkpoints + CLI Basics
**Time**: 1 hour
**Complexity**: ⭐⭐ Beginner+
**Goal**: Learn to experiment safely and use core CLI commands

#### What You'll Achieve
✅ Create and restore checkpoints for safe experimentation
✅ Understand interactive vs. print mode
✅ Use basic CLI flags and options
✅ Process files via piping

#### Hands-on Exercises

```bash
# Exercise 1: Try checkpoint workflow
# In Claude Code:
# Make some experimental changes, then press Esc+Esc or use /rewind
# Select the checkpoint before your experiment
# Choose "Restore code and conversation" to go back

# Exercise 2: Interactive vs Print mode
claude "explain this project"           # Interactive mode
claude -p "explain this function"       # Print mode (non-interactive)

# Exercise 3: Process file content via piping
cat error.log | claude -p "explain this error"
```

#### Success Criteria
- [ ] Created and reverted to a checkpoint
- [ ] Used both interactive and print mode
- [ ] Piped a file to Claude for analysis
- [ ] Understand when to use checkpoints for safe experimentation

#### Next Steps
- Read: [08-checkpoints/README.md](../08-checkpoints/README.md)
- Read: [10-cli/README.md](../10-cli/README.md)
- **Ready for Level 2!** Proceed to [Milestone 2A](LEARNING-ROADMAP_LEVEL-2.md#milestone-2a-automation-skills--hooks)

> **Check your understanding**: Run `/lesson-quiz checkpoints` or `/lesson-quiz cli` to verify you're ready for Level 2.
