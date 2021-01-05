# Member Audit Secure Groups Integration for Alliance Auth

This is an integration between [Member Audit](https://gitlab.com/ErikKalkoken/aa-memberaudit) and [Secure Groups](https://github.com/pvyParts/allianceauth-secure-groups) for [Alliance Auth](https://gitlab.com/allianceauth/allianceauth) (AA).

![release](https://img.shields.io/pypi/v/aa-blueprints?label=release)
![License](https://img.shields.io/badge/license-GPL-green)
![python](https://img.shields.io/pypi/pyversions/aa-blueprints)
![django](https://img.shields.io/pypi/djversions/aa-blueprints?label=django)
![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)
![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)

## Features

- Compliance Filter
- Skill Set Filter
- Asset Filter

# Installation

## Requirements

This integration needs [Member Audit](https://gitlab.com/ErikKalkoken/aa-memberaudit) and [Secure Groups](https://github.com/pvyParts/allianceauth-secure-groups) to function. Please make sure they are installed before continuing.

## Steps

### Step 1 - Install the Package

Make sure you are in the virtual environment (venv) of your Alliance Auth installation. Then install the newest release from PyPI:

`pip install aa-memberaudit-securegroups`

### Step 2 - Config

Add `memberaudit_securegroups` to your `INSTALLED_APPS`.

### Step 3 - Finalize App Installation

Run migrations:

```bash
python manage.py migrate
```

Restart your supervisor services for Auth
