# CS 5340 Software Maintenance Project – WeeWX Refactoring

## Project Overview
This repository contains the final deliverables for our CS 5340 Software Maintenance project on WeeWX.

The project focuses on maintainability analysis and targeted refactoring in the WeeWX codebase. Our primary goal was to identify maintainability hotspots using static analysis and improve code structure without changing intended behavior.

## Grader Note
This `main` branch is the final grader-facing branch.

For most grading, you do not need to fully configure a weather station environment.

You can evaluate the project by:
1. Opening `weewx_v531/src/weecfg/update_config.py`
2. Comparing it with `weewx_v520/src/weecfg/update_config.py`
3. Reviewing `static_analysis_results/`
4. Reading the final paper and presentation in `docs/`

If you want to run the full WeeWX codebase, follow the instructions in the **How to Run Full WeeWX** section below.

## Refactoring Focus
Primary target:
- `src/weecfg/update_config.py`

Key refactored functions:
- `update_to_v25`
- `update_to_v26`

## Repository Layout
- `docs/` — final paper, final presentation, and supporting documentation
- `static_analysis_results/` — saved static analysis outputs
- `weewx_v520/` — baseline WeeWX version used for comparison
- `weewx_v531/` — refactored/comparison WeeWX version

## Important Note About Source Code History
The folders `weewx_v520/` and `weewx_v531/` are Git submodules.

This means:
- `weewx_v520/` points to the baseline WeeWX source repository
- `weewx_v531/` points to the refactored WeeWX source repository
- this repository stores references to specific submodule commits rather than showing the full internal commit history directly in the top-level folder view

## Final Deliverables
- `docs/final-paper.pdf`
- `docs/final-presentation.pdf`
- `docs/user-documentation.md`
- `docs/run-weewx.md`

## How to Clone This Repository
Clone with submodules:

```bash
git clone --recurse-submodules https://github.com/anguyen7-99/CS-5340-Group-2.git
cd CS-5340-Group-2
