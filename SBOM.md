# Software Bill of Materials (SBOM)

## Project

CS 5340 WeeWX Software Maintenance Project

## Project Contributors

| Contributor | Role |
|---|---|
| Jerry Delva | Project contributor |
| Andrew Nguyen | Project contributor |

## Main Repository

https://github.com/anguyen7-99/CS-5340-Group-2

## External Open-Source Software

| Component | Purpose | Source |
|---|---|---|
| WeeWX v5.2.0 | Baseline comparison version | https://github.com/weewx/weewx |
| WeeWX v5.3.1 | Baseline and refactoring target version | https://github.com/weewx/weewx |
| Python | Runtime environment | https://www.python.org |
| Radon | Static analysis for Cyclomatic Complexity and Maintainability Index | https://radon.readthedocs.io |
| Pylint | Static code quality analysis | https://pylint.pycqa.org |
| Git | Version control | https://git-scm.com |
| GitHub | Repository hosting and collaboration | https://github.com |

## Project Artifacts

| Artifact | Description |
|---|---|
| weewx_v520 | WeeWX v5.2.0 baseline source code |
| weewx_v531 | WeeWX v5.3.1 baseline/refactored source code |
| static_analysis_results | Stored Radon and Pylint analysis outputs |
| README.md | Instructions for setup, analysis, and reproduction |
| requirements.txt | Python package dependencies |
| LICENSE | Project license information |
| canvas_submission_note.txt | Canvas submission summary |

## License Notes

This project is based on WeeWX, which remains under its original open-source license. The original WeeWX source code and license belong to the WeeWX project and its contributors.

The project-specific documentation, static analysis results, scripts, and refactoring work were created for the CS 5340 semester project by Jerry Delva and Andrew Nguyen.

## Notes

This project performs static analysis and targeted refactoring on selected WeeWX source code. The main maintenance focus is on `weecfg/update_config.py`, especially the `update_to_v25` and `update_to_v26` functions.
