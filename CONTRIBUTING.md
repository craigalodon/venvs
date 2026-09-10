# Contributing

This is a personal project — a small set of reusable Python environment profiles
that I maintain for my own analytics and notebook work. It's public mainly so I
can clone it anywhere, not because I'm looking for contributions.

That said, you're welcome to use it, fork it, or open an issue.

## If you want to propose a change

- **Bugs / broken locks:** open an issue describing what failed (`uv sync`
  output, OS, `uv --version`).
- **Small fixes:** a PR is fine. Keep it focused on one profile or one concern.
- **New profiles or large dependency changes:** open an issue first so we can
  talk about whether it fits the intent of the repo before you spend time on it.

## Ground rules

Edit `pyproject.toml`, then regenerate the lockfile — never hand-edit `uv.lock`:

```bash
uv lock
uv sync
git add pyproject.toml uv.lock
```

`pre-commit` runs on commit; make sure it passes (`pre-commit run --all-files`).
Don't commit `.venv/` or anything else already in `.gitignore`.

No guarantees on review turnaround. If something sits, a ping on the issue is
fine.
