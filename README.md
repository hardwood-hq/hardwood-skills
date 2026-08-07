# hardwood-skills

Agent skills for the [`hardwood`](https://github.com/hardwood-hq/hardwood) Apache Parquet toolkit, packaged as a [Claude Code](https://claude.com/claude-code) plugin.

This repository is the **distribution channel**. The skills' source of truth lives in the [main hardwood repository](https://github.com/hardwood-hq/hardwood) under `skills/` and is published here — do not edit `skills/` in this repository directly (see [Updating](#updating)).

## What's included

- **hardwood-cli** — teaches an AI coding agent when and how to use the `hardwood` CLI to inspect and debug Parquet files: schema and physical/logical types, why predicate pushdown or page skipping isn't happening, dictionary encodings, footer layout, and CSV/JSON conversion.

## Install (Claude Code)

This repository doubles as a plugin marketplace. Inside Claude Code, run:

```text
/plugin marketplace add hardwood-hq/hardwood-skills
/plugin install hardwood@hardwood-skills
```

The skill then loads automatically in future sessions whenever a task involves a Parquet file. It drives the `hardwood` binary, so make sure `hardwood` is on your `PATH` — see the [CLI reference](https://github.com/hardwood-hq/hardwood/blob/main/docs/content/reference/cli.md).

## Other agent harnesses

The skill follows the [Agent Skills specification](https://agentskills.io). For a harness other than Claude Code, copy `skills/hardwood-cli/SKILL.md` into that tool's skills directory.

## Updating

`skills/` is published from the main repository. Edit the skill there (`skills/hardwood-cli/SKILL.md`) so it stays in lockstep with the CLI it documents, then run the publish step described in the main repo's [`CONTRIBUTING.md`](https://github.com/hardwood-hq/hardwood/blob/main/CONTRIBUTING.md).

## License

Apache-2.0. See [`LICENSE.txt`](LICENSE.txt).
