# CLAUDE.md

## Folder Structure

```bash
├── infrastructure
│   └── terraform // infrastructure IaC codes
└── src
    ├── backend // all backend projects
    └── frontend // all frontend projects
       └── lp // This is the landing page repo.
```

## Commit Convention

Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/).
The `commit-msg` hook is wired up via [`pre-commit`](https://pre-commit.com/) using
[`conventional-pre-commit`](https://github.com/compilerla/conventional-pre-commit).

One-time setup per clone:

```bash
pre-commit install --hook-type commit-msg
git config commit.template .gitmessage   # optional: prefilled template
```

Allowed types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`,
`ci`, `chore`, `revert`.
Format: `type(scope): subject`.
