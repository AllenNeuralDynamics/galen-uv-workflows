# AIND GitHub Actions (Reusable Workflows)
aind-github-actions

[![License](https://img.shields.io/badge/license-MIT-brightgreen)](LICENSE)

## This repository is for workflows that may be reused in other workflows and repositories.

GitHub actions workflows are found in .github/workflows.

Example calling workflows are in `examples/`

The UV CI workflow depends on your project having a `dev` group of optional
dependencies with `ruff`, `interrogate`, `codespell`, `pytest`, and
`pytest-cov`.

The bump workflow requires `commitizen` configuration in the calling project's
`pyproject.toml`, and that projects follow
[conventional commits](https://www.conventionalcommits.org/en/v1.0.0/).

The publish workflow can be configured to publish to pypi, as well as make a
github release. See the example `examples/publish-call.yml` for more
information.

### Pull requests

For internal members, please create a branch. For external members, please fork
the repository and open a pull request from the fork. We'll primarily use
[conventional commits](https://www.conventionalcommits.org/en/v1.0.0/).
```text
<type>(<scope>): <short summary>
```

where scope (optional) describes the packages affected by the code changes and
type (mandatory) is one of:

- **build**: Changes that affect build tools or external dependencies (example scopes: pyproject.toml, setup.py)
- **ci**: Changes to our CI configuration files and scripts (examples: .github/workflows/ci.yml)
- **docs**: Documentation only changes
- **feat**: A new feature
- **fix**: A bugfix
- **perf**: A code change that improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **test**: Adding missing tests or correcting existing tests
