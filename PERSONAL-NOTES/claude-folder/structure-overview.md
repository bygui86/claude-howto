
# `.claude` folder structure

## user `~/.claude`

```
.claude/
│
├── agents/				# subagent personas
│	├── agent-A.md
│	├── agent-B.md
│	└── ...
│
├── downloads/			# ?
│	└── ?
│
├── hooks/				# ?
│	└── ?
│
├── plugins/			# ?
│	└── ?
│
├── projects/			# ?
│	└── ?
│
├── rules/				# modular instruction files to better organise memory (aka CLAUDE.md)
│	├── rule-A.md
│	├── rule-B.md
│	└── ...
│
├── skills/					# auto-invoked workflows (context aware automatic workflows) + custom slash commands (repeatable manual workflows)
│	├── skill-A/
│	│	├── examples/
│	│	│	└── sample.md 		# Example output showing expected format
│	│	│
│	│	├── scripts/			# Scripts Claude can execute
│	│	│	└── script-A.sh
│	│	│	└── script-B.py
│	│	│
│	│	├── templates/
│	│	│	└── template-A.sh 	# Template for Claude to fill in
│	│	│
│	│	└── SKILL.md 			# Main instructions (required)
│	│
│	├── skill-B/
│	│	└── SKILL.md
│	│
│	└── ...
│
├── CLAUDE.md 			# global personal memory
│
└── settings.json		# global personal permissions + config
```

## project `path/to/project/.claude`

```
project/
│
├── .claude/
│	│
│	├── agents/					# specialized subagent personas
│	│	├── agent-A.md
│	│	├── agent-B.md
│	│	└── ...
│	│
│	├── rules/					# modular instruction files to better organise memory (aka CLAUDE.md)
│	│	├── rule-A.md
│	│	├── rule-B.md
│	│	└── ...
│	│
│	├── skills/					# auto-invoked workflows (context aware automatic workflows) + custom slash commands (repeatable manual workflows)
│	│	├── skill-A/
│	│	│	├── examples/
│	│	│	│	└── sample.md 		# Example output showing expected format
│	│	│	│
│	│	│	├── scripts/			# Scripts Claude can execute
│	│	│	│	└── script-A.sh
│	│	│	│	└── script-B.py
│	│	│	│
│	│	│	├── templates/
│	│	│	│	└── template-A.sh 	# Template for Claude to fill in
│	│	│	│
│	│	│	└── SKILL.md 			# Main instructions (required)
│	│	│
│	│	├── skill-B/
│	│	│	└── SKILL.md
│	│	│
│	│	└── ...
│	│
│	├── settings.json			# project shared permissions + config / committed to git repo
│	│
│	└── settings.local.json		# project personal permissions + config / gitignored
│
├── CLAUDE.md 					# project shared memory / committed
│
└── CLAUDE.local.md				# project personal memory / gitignored
```
