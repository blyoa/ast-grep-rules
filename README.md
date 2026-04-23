# ast-grep-rules

A collection of [ast-grep](https://ast-grep.github.io/) lint rules.

## Installation

Copy the rules you need into your rule directory and configure `sgconfig.yml`:

```yaml
ruleDirs:
  - rules
testConfigs:
  - testDir: rule-tests
```

## Conflicting Rules

Some rules are mutually exclusive. Enable only one from each group.

## Adding a Rule

1. Create `rules/{category}/{rule-name}.yml`
2. Create `rule-tests/{category}/{rule-name}-test.yml`
3. Run `sg test --skip-snapshot-tests` to verify valid/invalid cases
4. Run `sg test -U` to generate snapshots
