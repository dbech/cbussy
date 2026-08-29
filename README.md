# Cbussy

One Agent Skill for SpaceLogic C-Bus. Layout matches `npx skills add`: `skills/cbussy/SKILL.md`.

Not an official Schneider Electric product.

## Install

```bash
npx skills add dbech/cbussy
```

Local:

```bash
npx skills add /absolute/path/to/cbussy --list
npx skills add /absolute/path/to/cbussy -s cbussy
```

`-g` installs for the user across projects.

## Layout

```
skills/cbussy/SKILL.md
skills/cbussy/references/     # topic notes + CORPUS.md + manual .txt extracts
skills/cbussy/agents/openai.yaml
```

Manual extracts travel inside the skill folder, so a receiving agent can open them after install. One copy.
