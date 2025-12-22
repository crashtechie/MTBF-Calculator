# MTBF Calculator

**Version:** 0.1.1

A data analysis tool for calculating Mean Time Between Failures (MTBF) metrics using Python and Jupyter Lab. This project provides a containerized environment for analyzing equipment failure data, computing reliability metrics, and visualizing trends.

## Purpose

The MTBF Calculator is designed to help engineers and reliability analysts:
- Calculate Mean Time Between Failures (MTBF) from equipment failure data
- Analyze failure patterns and trends
- Generate reliability metrics and statistics
- Visualize failure data through charts and graphs
- Process and parse raw failure data into usable formats

## Features

- **Containerized Development**: Docker-based Jupyter Lab environment for consistent setup across systems
- **Data Processing**: Tools for parsing and analyzing raw failure data
- **Statistical Analysis**: Built-in support for pandas, numpy for robust calculations
- **Visualization**: matplotlib and seaborn for creating insightful charts
- **Persistent Storage**: Volume mounting for notebooks and data preservation
- **Environment Configuration**: Flexible setup through .env files

## Prerequisites

- Docker
- Docker Compose

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd MTBF-Calculator
```

### 2. Configure Environment

The project includes a sample environment file. You can use the default settings or customize them:

```bash
# The .env file is already configured for local development
# Optionally, review and modify application/.env as needed
```

### 3. Build and Start the Container

```bash
docker-compose up -d
```

### 4. Access Jupyter Lab

Open your browser and navigate to:
```
http://localhost:8080
```

No authentication is required for local development.

### 5. Stop the Container

```bash
docker-compose down
```

## Project Structure

```
MTBF-Calculator/
├── application/
│   ├── Dockerfile              # Jupyter Lab container configuration
│   ├── .env                    # Environment variables for local development
│   └── .env.example           # Template for environment configuration
├── data/
│   ├── raw-data/              # Raw failure data files
│   └── parsed-data/           # Processed and analyzed data
├── notebooks/
│   └── mtbfCalc.ipynb         # Main MTBF calculation notebook
├── docker-compose.yml          # Docker Compose service definition
├── requirements.txt            # Python package dependencies
├── CHANGELOG.md               # Version history and changes
└── README.md                  # This file
```

## Dependencies

- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization

## Usage

1. Place your raw failure data in the `data/raw-data/` directory
2. Open the Jupyter Lab interface at http://localhost:8080
3. Navigate to `notebooks/mtbfCalc.ipynb`
4. Follow the notebook instructions to process and analyze your data
5. Processed results will be saved to `data/parsed-data/`

## Environment Variables

Key environment variables (configured in `application/.env`):

- `JUPYTER_PORT`: Port for Jupyter Lab (default: 8888)
- `JUPYTER_TOKEN`: Authentication token (empty for no auth)
- `JUPYTER_PASSWORD`: Authentication password (empty for no auth)
- `ENVIRONMENT`: Application environment (development/production)
- `DATA_RAW_PATH`: Path to raw data directory
- `DATA_PARSED_PATH`: Path to processed data directory

## Contributing

Contributions are welcome! Please refer to the CHANGELOG.md for version history and update it when making changes following semantic versioning principles.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Version History

See [CHANGELOG.md](CHANGELOG.md) for detailed version history and changes.
