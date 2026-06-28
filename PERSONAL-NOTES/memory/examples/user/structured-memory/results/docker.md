
<!-- Path -->

/memory/tools/docker.md

<!-- Content -->

## Docker

- 2026-02-12: Must use `host.docker.internal` not `localhost` for DB connections from containers — spent 30 min debugging this
- 2026-02-13: Project Dockerfile needs `--platform=linux/amd64` on M1 Macs or builds silently produce broken images
- 2026-02-13: docker compose v2 uses `docker compose` (no hyphen) — old scripts with `docker-compose` fail on CI
