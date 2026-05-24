CI: add GitHub Actions workflow with Redis

This PR adds a CI workflow that:
- Installs dependencies with pnpm
- Generates Prisma client
- Runs backend lint and tests with Redis service started in the runner
- Runs frontend lint, build, and tests (non-blocking)

Notes:
- Tests run with `DISABLE_REDIS=false` in CI. Local test environment can set `DISABLE_REDIS=true` to skip Redis.
- If you'd like frontend failures to block the build, I can make those steps strict.
