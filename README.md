# Kira-Toolkit

Claude Code integration for Kira development standards.

## Installation

1. Add as a submodule to your project:
   ```bash
   git submodule add https://github.com/PhilipLudington/Kira-Toolkit.git kira-toolkit
   git submodule update --init --recursive
   ```

2. Copy commands and rules to your project:
   ```bash
   mkdir -p .claude/commands .claude/rules
   cp kira-toolkit/commands/*.md .claude/commands/
   cp kira-toolkit/reference/rules/*.md .claude/rules/
   ```

3. Add to your CLAUDE.md:
   ```markdown
   See `kira-toolkit/reference/REFERENCE.md` for Kira coding guidelines.
   ```

## Updating

To update to the latest version:
```bash
git submodule update --remote --recursive kira-toolkit
cp kira-toolkit/commands/*.md .claude/commands/
cp kira-toolkit/reference/rules/*.md .claude/rules/
```

## Available Commands

| Command | Purpose |
|---------|---------|
| `/kira-init` | Create new Kira project |
| `/kira-review` | Review code against standards |
| `/kira-safety` | Security-focused review |
| `/kira-check` | Run validation |

## Documentation

Standards and documentation are in `reference/`:
- `reference/STANDARDS.md` - Full coding standards
- `reference/REFERENCE.md` - Quick reference
- `reference/docs/` - Pattern guides

## License

MIT License
