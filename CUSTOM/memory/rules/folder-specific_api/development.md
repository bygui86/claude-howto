<!-- Path-Specific Rules with YAML Frontmatter -->

<!-- 
  Glob Pattern Examples:

  **/*.ts - All TypeScript files
  src/**/* - All files under src/
  src/**/*.{ts,tsx} - Multiple extensions
  {src,lib}/**/*.ts, tests/**/*.test.ts - Multiple patterns
 -->

---
paths: src/api/**/*.ts
---

# API Development Rules

- All API endpoints must include input validation
- Use Zod for schema validation
- Document all parameters and response types
- Include error handling for all operations
