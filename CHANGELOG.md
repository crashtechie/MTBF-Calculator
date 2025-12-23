# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0] - 2025-12-23

### Added
- Fiscal calendar generation with weeks starting on Mondays (52 weeks per fiscal year)
- Fiscal year, week, month, and quarter tracking functionality
- MTBF calculation functions for specified time periods
- MTBF comparison and percentage change calculations
- Weekly MTBF analysis and comparison between fiscal years (FY25 vs FY26)
- Data export functionality for fiscal calendar and enriched outage data
- Formatted MTBF display in dd hh:mm:ss format

### Changed
- Enhanced mtbfCalc.ipynb notebook with comprehensive MTBF analysis features
- Improved data processing with fiscal period assignments using merge_asof
- Updated data structure to include fiscal period metadata

### Fixed
- Case-sensitive string replacement issues in data parsing
- Fiscal year and week calculation logic to properly handle 52-week fiscal years

## [0.1.1] - 2025-12-22

### Added
- MIT License file for open source distribution
- License section in README.md

## [0.1.0] - 2025-12-22

### Added
- Initial project setup for MTBF Calculator
- Jupyter Lab environment with Docker support
- Docker Compose configuration for containerized development
- Python dependencies: pandas, numpy, matplotlib, seaborn
- Data directory structure for raw and parsed data
- Notebook directory with mtbfCalc.ipynb
- Environment configuration with .env and .env.example files
- Git ignore and Docker ignore files
- Project documentation structure (README.md, CHANGELOG.md)

### Infrastructure
- Dockerfile for Jupyter Lab base image
- Docker Compose service configuration
- Volume mounting for notebooks and data directories
- Environment variable support for flexible configuration
- Port mapping (8080:8888) for Jupyter Lab access
- No-authentication setup for local development

[0.2.0]: https://github.com/crashtechie/MTBF-Calculator/compare/v0.1.1...v0.2.0
[0.1.1]: https://github.com/crashtechie/MTBF-Calculator/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/crashtechie/MTBF-Calculator/releases/tag/v0.1.0
