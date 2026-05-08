<!-- File: ./CLAUDE.md -->

# Project Configuration

## Project Overview
<!-- provide roject general info -->
- **Name**: draft
- **Tech Stack**: Node.js, React 18, PostgreSQL, Docker, Kubernetes

## Architecture
<!-- reference important documentation -->
<!-- DONT: Copying content that exists elsewhere -->
<!-- DO: Instead of copying README content into CLAUDE.md, just import it -->
@docs/architecture.md
@docs/api-standards.md
@docs/database-schema.md

## Development Standards

<!-- ### Code Style -->
<!-- no need to load or define code style for TypeScript as already in ./claude/rules/typescript/code-style.md -->

<!-- ### Naming Conventions -->
<!-- no need to load or define any naming conventions as already in ./claude/rules/naming-conventions.md -->

### Git Workflow
- Branch names: `feature/description` or `fix/description`
- Commit messages: Follow conventional commits
- PR required before merge
- All CI/CD checks must pass
- Minimum 1 approval required
- Always run tests before committing
- Use semantic versioning for all releases

### Testing Requirements
- Minimum 80% code coverage
- All critical paths must have tests
- Use Jest for unit tests
- Use Cypress for E2E tests
- Test filenames: `*.test.ts` or `*.spec.ts`

### API Standards
- RESTful endpoints only
- JSON request/response
- Use HTTP status codes correctly
- Version API endpoints: `/api/v1/`
- Document all endpoints with examples

### Database
- Use migrations for schema changes
- Never hardcode credentials
- Use connection pooling
- Enable query logging in development
- Regular backups required

### Deployment
- Docker-based deployment
- Kubernetes orchestration
- Blue-green deployment strategy
- Automatic rollback on failure
- Database migrations run before deploy

## Common Commands

| Command | Purpose |
|---------|---------|
| `npm run dev` | Start development server |
| `npm test` | Run test suite |
| `npm run lint` | Check code style |
| `npm run build` | Build for production |
| `npm run migrate` | Run database migrations |

## Team Contacts
- Tech Lead: Sarah Chen (@sarah.chen)
- Product Manager: Mike Johnson (@mike.j)
- DevOps: Alex Kim (@alex.k)

## Known Issues & Workarounds
- PostgreSQL connection pooling limited to 20 during peak hours
- Workaround: Implement query queuing
- Safari 14 compatibility issues with async generators
- Workaround: Use Babel transpiler

## Related Projects
- Analytics Dashboard: `/projects/analytics`
- Mobile App: `/projects/mobile`
- Admin Panel: `/projects/admin`

---
**Last Updated**: April 9, 2026
