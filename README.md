# Member Audit Secure Groups Integration for Alliance Auth

This is an integration between [Member Audit](https://gitlab.com/ErikKalkoken/aa-memberaudit) and [Secure Groups](https://github.com/pvyParts/allianceauth-secure-groups) for [Alliance Auth](https://gitlab.com/allianceauth/allianceauth) (AA).

[![Version](https://img.shields.io/pypi/v/aa-memberaudit-secure-groups?label=release)](https://pypi.org/project/aa-memberaudit-secure-groups/)
[![License](https://img.shields.io/github/license/ppfeufer/aa-memberaudit-secure-groups)](https://github.com/ppfeufer/aa-memberaudit-secure-groups/blob/master/LICENSE)
[![Python](https://img.shields.io/pypi/pyversions/aa-memberaudit-secure-groups)](https://pypi.org/project/aa-memberaudit-secure-groups/)
[![Django](https://img.shields.io/pypi/djversions/aa-memberaudit-secure-groups?label=django)](https://pypi.org/project/aa-memberaudit-secure-groups/)
![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)
[![Code Style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](http://black.readthedocs.io/en/latest/)
[![Discord](https://img.shields.io/discord/790364535294132234?label=discord)](https://discord.gg/zmh52wnfvM)
[![Checks](https://github.com/ppfeufer/aa-memberaudit-secure-groups/actions/workflows/automated-checks.yml/badge.svg)](https://github.com/ppfeufer/aa-memberaudit-secure-groups/actions/workflows/automated-checks.yml)
[![codecov](https://codecov.io/gh/ppfeufer/aa-memberaudit-secure-groups/branch/master/graph/badge.svg)](https://codecov.io/gh/ppfeufer/aa-memberaudit-secure-groups)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](https://github.com/ppfeufer/aa-memberaudit-secure-groups/blob/master/CODE_OF_CONDUCT.md)

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/N4N8CL1BY)


## Features

- Activity Filter
- Asset Filter
- Character Age Filter
- Compliance Filter
- Skill Set Filter
- Skill Point Filter

# Installation

## Requirements

This integration needs [Member Audit](https://gitlab.com/ErikKalkoken/aa-memberaudit)
and [Secure Groups](https://github.com/pvyParts/allianceauth-secure-groups) to
function. Please make sure they are installed before continuing.

## Steps

### Step 1 - Install the Package

Make sure you are in the virtual environment (venv) of your Alliance Auth
installation. Then install the newest release from PyPI:

```shell
pip install aa-memberaudit-secure-groups
```


### Step 2 - Config

Add `memberaudit_securegroups` to your `INSTALLED_APPS`.


### Step 3 - Finalize App Installation

Run migrations:

```shell
python manage.py migrate
```

Restart your supervisor services for Auth


# Filters

| Filter Name        | Matches if...                                                           |
|--------------------|-------------------------------------------------------------------------|
| Activity Filter    | User has *at least one* character active within the last X days         |
| Age Filter         | User has *at least one* character over X days old                       |
| Asset Filter       | User has *at least one* character with *any of* the assets defined      |
| Compliance Filter  | User has *all* characters registered on Member Audit                    |
| Skill Point Filter | User has *at least one* character with at least X skill points          |
| Skill Set Filter   | User has *at least one* character with *any of* the selected skill sets |
