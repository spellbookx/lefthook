# @spellbookx/lefthook

Shared Lefthook configurations for common tools and package managers.

## Usage

In your `lefthook.yml`:

```yaml
remote:
  git:
    url: https://github.com/spellbookx/lefthook
    ref: main
  configs:
    - @commit-msg/npx-commitlint.yml
    - @pre-commit/npx-eslint-prettier-tsc.yml
```

### Available Configurations

Replace `npx` with your preferred runner: `npx`, `bunx`, `yarndlx`, `pnpmdlx`.

#### Commit Message
- `@commit-msg/{runner}-commitlint.yml`: Lints commit messages using `commitlint`.

#### Pre-commit
- `@pre-commit/{runner}-eslint.yml`: Runs `eslint --fix`.
- `@pre-commit/{runner}-prettier.yml`: Runs `prettier --write`.
- `@pre-commit/{runner}-eslint-prettier.yml`: Runs both `eslint` and `prettier`.
- `@pre-commit/{runner}-tsc.yml`: Runs `tsc --noEmit`.
- `@pre-commit/{runner}-eslint-prettier-tsc.yml`: Runs all three.

#### Pre-push
- `@pre-push/{runner}-vitest.yml`: Runs `vitest run`.
- `@pre-push/{runner}-jest.yml`: Runs `jest`.

## Runners
- `npx`: Node.js package executor
- `bunx`: Bun's `bun x`
- `yarndlx`: Yarn's `yarn dlx`
- `pnpmdlx`: pnpm's `pnpm dlx`
