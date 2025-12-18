# Git Commit Convention Cheat Sheet

## Format
```
<type>(<scope>): <subject>
```

## Examples

```
feat(user): add profile picture upload

fix(cart): prevent negative quantities

docs: add API documentation

chore(deps): bump react to 18.2.0
```

## Types

| Type | Description | Example |
|------|-------------|---------|
| `feat` | New feature | `feat(auth): add login functionality` |
| `fix` | Bug fix | `fix(api): resolve timeout issue` |
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
