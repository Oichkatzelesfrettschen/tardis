# Installation Requirements (tardis)

`tardis` is a forked upstream submodule. In this meta-repo we enforce strict
gates only on a **small, stable surface** (phased expansion).

## Prerequisites

- Python (see `tardis/pyproject.toml`)

## Install (dev)

```bash
cd tardis
python -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install -e .
```

## Quality gates (warnings-as-errors)

- Ruff (local): `cd tardis && ruff check .`
- Mypy (scoped): `cd tardis && mypy --config-file mypy.ini`

From the meta-repo, strict gates are driven by the contract:
`scripts/audit/run_tiers.sh`.

