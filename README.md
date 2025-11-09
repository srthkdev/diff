# Multi-Platform Matrix Build with Artifacts

This repository demonstrates a GitHub Actions workflow that uses matrix builds to compile and test software across multiple platforms and configurations in parallel.

## Overview

The workflow implements a matrix build strategy that:
- Runs builds across multiple operating systems (Ubuntu, macOS, Windows)
- Tests with different Python versions (3.9, 3.10, 3.11)
- Generates unique build artifacts for each matrix combination
- Uploads artifacts with the naming convention: `build-5566316-<variant>`

## Workflow Features

- **Matrix Strategy**: Configures parallel builds for 3 different OS/Python combinations
- **Parallel Execution**: Each matrix variant runs as a separate job simultaneously
- **Artifact Management**: Each job generates and uploads build artifacts using `actions/upload-artifact@v4`
- **Cross-Platform Support**: Works on Ubuntu, macOS, and Windows runners

## Matrix Variants

The workflow includes the following matrix combinations:
1. `ubuntu-39`: Ubuntu with Python 3.9
2. `macos-310`: macOS with Python 3.10
3. `windows-311`: Windows with Python 3.11

## Artifacts

Each build job generates:
- `build-output.txt`: Text file containing build information
- `build-info.json`: JSON file with structured build metadata

All artifacts are uploaded with the prefix `build-5566316-` followed by the variant identifier.

## Contact

**Name**: Sarthak Jain  
**Email**: 23f3000839@ds.study.iitm.ac.in

## License

This project is for educational and demonstration purposes.

