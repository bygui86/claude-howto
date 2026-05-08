
# Do's - What To Include

- Be specific and detailed: Use clear, detailed instructions rather than vague guidance
  - ✅ Good: "Use 2-space indentation for all JavaScript files"
  - ❌ Avoid: "Follow best practices"

- Keep organized: Structure memory files with clear markdown sections and headings

- Use appropriate hierarchy levels:
  - Managed policy: Company-wide policies, security standards, compliance requirements
  - Project memory: Team standards, architecture, coding conventions (commit to git)
  - User memory: Personal preferences, communication style, tooling choices
  - Directory memory: Module-specific rules and overrides

- Leverage imports: Use @path/to/file syntax to reference existing documentation
  - Supports up to 5 levels of recursive nesting
  - Avoids duplication across memory files
  - Example: See @README.md for project overview

- Document frequent commands: Include commands you use repeatedly to save time

- Version control project memory: Commit project-level CLAUDE.md files to git for team benefit

- Review periodically: Update memory regularly as projects evolve and requirements change

- Provide concrete examples: Include code snippets and specific scenarios

# Don'ts - What To Avoid

- Don't store secrets: Never include API keys, passwords, tokens, or credentials

- Don't include sensitive data: No PII, private information, or proprietary secrets

- Don't duplicate content: Use imports (@path) to reference existing documentation instead

- Don't be vague: Avoid generic statements like "follow best practices" or "write good code"

- Don't make it too long: Keep individual memory files focused and under 500 lines

- Don't over-organize: Use hierarchy strategically; don't create excessive subdirectory overrides

- Don't forget to update: Stale memory can cause confusion and outdated practices

- Don't exceed nesting limits: Memory imports support up to 5 levels of nesting
