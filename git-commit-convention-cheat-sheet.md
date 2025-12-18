# Git Commit Convention Cheat Sheet

## Format
```
<type>(<scope>): <subject>
```

## For Learning Projects

| Type | Description | Example |
|------|-------------|---------|
| `learn` | Following Tutorials/Courses | `learn(udm): add database migrations (chapter 7)` |
| `experiment` |  Trying New Things | `experiment: try Redux instead of Context API` |
| `practice` | Applying What You Learned | `practice: recreate Netflix UI from scratch` |
| `checkpoint` | Milestones/Working States | `checkpoint: MVP features done` |
| `wip` | work in progress | `wip: implement login feature` |

## Standard Practice

| Type | Description | Example |
|------|-------------|---------|
| `feat` | New feature | `feat(auth): add login functionality` |
| `fix` | Bug fix | `fix(api): resolve timeout issue` |
| `wip` | work in progress | `wip: implement new shopping cart logic` |
| `docs` | Documentation only | `docs(readme): update installation steps` |
| `style` | Code style/formatting | `style: fix indentation` |
| `refactor` | Code restructuring | `refactor(parser): simplify logic` |
| `test` | Adding/updating tests | `test(api): add unit tests` |
| `chore` | Maintenance tasks | `chore: update dependencies, create folders` |
| `perf` | Performance improvements | `perf(db): optimize queries` |
| `ci` | CI/CD changes | `ci: add GitHub Actions workflow` |
| `build` | Build system changes | `build: update webpack config` |
| `revert` | Revert previous commit | `revert: revert commit abc123` |

## Quick Rules

- **Subject**: lowercase, no period, imperative mood ("add" not "added")
- **Scope**: optional, component/module name
- **Body**: optional, explain *what* and *why* (not *how*)
- **Footer**: optional, breaking changes or issue references
