<div align="center">

# 🐍 {{ cookiecutter.project_name }}

### Modern Python Project Template | Cookiecutter | Best Practices | Production-Ready

[![Python](https://img.shields.io/badge/Python-{{ cookiecutter.python_version }}+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Ruff](https://img.shields.io/badge/Linter-Ruff-D7FF64?style=for-the-badge&logo=ruff&logoColor=black)](https://github.com/astral-sh/ruff)
[![Pre-commit](https://img.shields.io/badge/Pre--commit-Enabled-brightgreen?style=for-the-badge&logo=pre-commit&logoColor=white)](https://pre-commit.com/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

**A production-ready Python project template featuring modern tooling, automated code quality checks, and industry best practices.**

[Quick Start](#-quick-start) •
[Features](#-features) •
[Architecture](#-architecture) •
[Documentation](#-documentation)

</div>

---

## 🎯 Why This Template?

| Metric | Impact |
|--------|--------|
| **10x Faster Linting** | Ruff replaces Black, isort, Flake8 in a single tool |
| **100% Type Coverage** | Full mypy strict mode integration |
| **Zero Config Setup** | One command to scaffold and start coding |
| **CI/CD Ready** | Pre-configured GitHub Actions workflows |
| **Security First** | Bandit security scanning built-in |

---

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────────────────────────────┐
│                      DEVELOPMENT WORKFLOW                           │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│   ┌──────────┐    ┌──────────┐    ┌──────────┐    ┌──────────┐    │
│   │  Write   │───▶│  Save    │───▶│  Commit  │───▶│   Push   │    │
│   │  Code    │    │  File    │    │  Changes │    │  to Repo │    │
│   └──────────┘    └────┬─────┘    └────┬─────┘    └────┬─────┘    │
│                        │               │               │           │
│                        ▼               ▼               ▼           │
│   ┌─────────────────────────────────────────────────────────────┐ │
│   │                    AUTOMATED QUALITY GATES                   │ │
│   ├─────────────────────────────────────────────────────────────┤ │
│   │                                                              │ │
│   │  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────────────┐ │ │
│   │  │  Ruff   │  │  Mypy   │  │ Bandit  │  │   Commitizen    │ │ │
│   │  │ Lint +  │  │  Type   │  │Security │  │   Conventional  │ │ │
│   │  │ Format  │  │  Check  │  │  Scan   │  │     Commits     │ │ │
│   │  └─────────┘  └─────────┘  └─────────┘  └─────────────────┘ │ │
│   │                                                              │ │
│   └─────────────────────────────────────────────────────────────┘ │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────┐
│                       PROJECT STRUCTURE                             │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│   {{ cookiecutter.project_slug }}/                                  │
│   ├── src/                                                          │
│   │   └── {{ cookiecutter.project_slug }}/                          │
│   │       ├── __init__.py      # Package initialization             │
│   │       ├── main.py          # Core application logic             │
│   │       ├── my_cli.py        # Typer CLI interface                │
│   │       └── rich_demo.py     # Rich terminal UI examples          │
│   │                                                                 │
│   ├── tests/                                                        │
│   │   └── test_main.py         # Pytest test suite                  │
│   │                                                                 │
│   ├── pyproject.toml           # Unified Python config              │
│   ├── .pre-commit-config.yaml  # Git hooks configuration            │
│   └── README.md                # Project documentation              │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🔧 Development Tools
- **Ruff** - Lightning-fast linter & formatter
- **Mypy** - Static type checking
- **Pytest** - Testing with async & coverage
- **Pre-commit** - Automated git hooks

</td>
<td width="50%">

### 🛡️ Quality & Security
- **Bandit** - Security vulnerability scanning
- **Commitizen** - Conventional commits
- **pip-tools** - Dependency management
- **GitHub Actions** - CI/CD pipelines

</td>
</tr>
</table>

---

## 🚀 Quick Start

### Prerequisites
- Python {{ cookiecutter.python_version }}+
- [Cookiecutter](https://cookiecutter.readthedocs.io/) (`pip install cookiecutter`)

### Generate Your Project

```bash
# Generate from template
cookiecutter gh:asq-sheriff/cookiecutter-modern-python

# Navigate to your new project
cd your-project-name

# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate  # macOS/Linux
# .venv\Scripts\activate   # Windows

# Install development dependencies
pip install -e ".[dev]"

# Initialize git and pre-commit hooks
git init
pre-commit install --install-hooks
```

---

## 📦 Tool Stack

```
┌────────────────────────────────────────────────────────────────┐
│                     MODERN PYTHON TOOLCHAIN                    │
├────────────────────────────────────────────────────────────────┤
│                                                                │
│  LINTING & FORMATTING          TYPE CHECKING                   │
│  ┌────────────────────┐        ┌────────────────────┐         │
│  │       RUFF         │        │       MYPY         │         │
│  │  ─────────────────  │        │  ─────────────────  │         │
│  │  • Replaces Black  │        │  • Strict mode     │         │
│  │  • Replaces isort  │        │  • Type inference  │         │
│  │  • Replaces Flake8 │        │  • Plugin support  │         │
│  │  • 10-100x faster  │        │  • IDE integration │         │
│  └────────────────────┘        └────────────────────┘         │
│                                                                │
│  TESTING                       SECURITY                        │
│  ┌────────────────────┐        ┌────────────────────┐         │
│  │      PYTEST        │        │      BANDIT        │         │
│  │  ─────────────────  │        │  ─────────────────  │         │
│  │  • Async support   │        │  • SAST scanning   │         │
│  │  • Coverage report │        │  • OWASP checks    │         │
│  │  • Fixtures        │        │  • CI integration  │         │
│  │  • Parameterized   │        │  • Custom rules    │         │
│  └────────────────────┘        └────────────────────┘         │
│                                                                │
└────────────────────────────────────────────────────────────────┘
```

---

## 📋 Configuration

### pyproject.toml (Unified Configuration)

```toml
[build-system]
requires = ["setuptools>=61.0", "wheel"]
build-backend = "setuptools.build_meta"

[project]
name = "{{ cookiecutter.project_slug }}"
version = "0.1.0"
description = "{{ cookiecutter.description }}"
authors = [{ name = "{{ cookiecutter.author_name }}", email = "{{ cookiecutter.author_email }}" }]
readme = "README.md"
requires-python = ">= {{ cookiecutter.python_version }}"

[project.optional-dependencies]
dev = [
    "pre-commit>=4.4.0",
    "ruff>=0.11.9",
    "mypy>=1.15.0",
    "bandit>=1.8.3",
    "docformatter>=1.7.7",
    "commitizen>=4.7.0",
    "pytest>=8.0.0",
    "pytest-cov>=4.1.0",
    "pytest-asyncio>=0.23.0",
]
```

---

## 🔄 Development Workflow

```
┌─────────────────────────────────────────────────────────────┐
│                    COMMIT LIFECYCLE                         │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   git add .                                                 │
│       │                                                     │
│       ▼                                                     │
│   git commit -m "feat: add feature"                         │
│       │                                                     │
│       ▼                                                     │
│   ┌─────────────────────────────────────────────────────┐  │
│   │              PRE-COMMIT HOOKS RUN                    │  │
│   ├─────────────────────────────────────────────────────┤  │
│   │  1. ruff check --fix        (auto-fix lint issues)  │  │
│   │  2. ruff format             (format code)           │  │
│   │  3. mypy                    (type check)            │  │
│   │  4. bandit                  (security scan)         │  │
│   │  5. commitizen              (validate message)      │  │
│   └─────────────────────────────────────────────────────┘  │
│       │                                                     │
│       ▼                                                     │
│   ✅ Commit succeeds (all checks pass)                      │
│   ❌ Commit blocked (fix issues and retry)                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Commands Reference

| Command | Description |
|---------|-------------|
| `ruff check .` | Run linter on all files |
| `ruff check --fix .` | Auto-fix linting issues |
| `ruff format .` | Format all Python files |
| `mypy .` | Run type checking |
| `pytest --cov=src` | Run tests with coverage |
| `bandit -r src/` | Security vulnerability scan |
| `pre-commit run --all-files` | Run all hooks manually |

---

## ⚠️ Known Issues

### Typer/Click Compatibility

As of May 2025, Typer has a known incompatibility with Click 8.2.0+. Workaround:

```bash
pip install "click==8.1.8"
```

Track updates: [Typer GitHub Issue #1215](https://github.com/fastapi/typer/issues/1215)

---

## 📁 Generated Project Structure

```
{{ cookiecutter.project_slug }}/
├── src/
│   └── {{ cookiecutter.project_slug }}/
│       ├── __init__.py
│       ├── main.py          # Core functionality
│       ├── my_cli.py        # CLI with Typer
│       └── rich_demo.py     # Rich terminal demos
├── tests/
│   └── test_main.py
├── .pre-commit-config.yaml
├── pyproject.toml
├── .gitignore
└── README.md
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feat/amazing-feature`)
3. Commit changes (`git commit -m 'feat: add amazing feature'`)
4. Push to branch (`git push origin feat/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

### Attribution

If you use this template, please acknowledge the creator:

```
Created by Aejaz (https://github.com/asq-sheriff)
Template: cookiecutter-modern-python
```

Or include a badge in your README:

```markdown
[![Template](https://img.shields.io/badge/Template-cookiecutter--modern--python-blue)](https://github.com/asq-sheriff/cookiecutter-modern-python)
```

---

## 👤 Author

**Aejaz**
- GitHub: [@asq-sheriff](https://github.com/asq-sheriff)

---

<div align="center">

**Built with modern Python best practices**

*Python • Ruff • Mypy • Pytest • Pre-commit • GitHub Actions*

Keywords: Python template, Cookiecutter, Python best practices, Ruff linter, Mypy type checking,
pre-commit hooks, Python project structure, modern Python development, Python CI/CD,
Python testing, pytest, Python security, bandit, Python automation, Python tooling

</div>
