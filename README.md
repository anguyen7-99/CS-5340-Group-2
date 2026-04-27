# CS 5340 Software Maintenance Project – WeeWX Refactoring

## Overview
This repository contains the final deliverables for our CS 5340 Software Maintenance project on WeeWX. The project uses static analysis to identify maintainability issues and applies targeted refactoring without changing intended behavior.

## Refactoring Target
Refactored file:
- `weewx_v531/src/weecfg/update_config.py`

Baseline file:
- `weewx_v520/src/weecfg/update_config.py`

Key refactored functions:
- `update_to_v25`
- `update_to_v26`

## Repository Layout
- `docs/` — final paper,final presentation, and midterm presentation
- `static_analysis_results/` — saved Radon and Pylint outputs
- `submission/`— source code and documentations zip file for Canvas
- `weewx_v520/` — baseline WeeWX version
- `weewx_v531/` — refactored/comparison WeeWX version

## Note About Source Code
`weewx_v520/` and `weewx_v531/` are Git submodules. This repository stores pointers to those source code versions.

## Quick Review for Graders
For most grading, you do not need to fully configure WeeWX.

Recommended review steps:
1. Open `weewx_v531/src/weecfg/update_config.py`
2. Compare it with `weewx_v520/src/weecfg/update_config.py`
3. Review `static_analysis_results/`
4. Read the final paper and presentation in `docs/`

## Setup
Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/anguyen7-99/CS-5340-Group-2.git
cd CS-5340-Group-2
```

If already cloned without submodules:

```bash
git submodule update --init --recursive
```

Install dependencies:

### macOS / Linux
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Windows PowerShell
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## Compare the Source Code
```bash
diff -u weewx_v520/src/weecfg/update_config.py weewx_v531/src/weecfg/update_config.py
```

## Run Static Analysis
```bash
radon cc weewx_v520/src/weecfg/update_config.py -s
radon cc weewx_v531/src/weecfg/update_config.py -s

radon mi weewx_v520/src/weecfg/update_config.py
radon mi weewx_v531/src/weecfg/update_config.py

pylint weewx_v520/src/weecfg/update_config.py
pylint weewx_v531/src/weecfg/update_config.py
```

## Run Full WeeWX
Running full WeeWX is optional. Use the refactored fork:

- Repository: `https://github.com/anguyen7-99/weewx`
- Branch: `refactor/update-config`

```bash
git clone --branch refactor/update-config https://github.com/anguyen7-99/weewx.git
cd weewx
python -m venv .venv
source .venv/bin/activate
pip install -U pip
pip install .
```

A valid `weewx.conf` file is required for full execution.

## Course Context
This project was completed for CS 5340 Software Maintenance, Spring 2026.

