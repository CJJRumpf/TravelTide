# TravelTide – Data Analytics Project

## Project Overview

TravelTide is a data analytics project designed to explore, process, and analyze travel-related data.

The project aims to apply data analytics techniques to identify patterns, uncover insights, and support data-driven decision-making in the travel industry.

The development environment is built around Python, Jupyter Notebook, and PostgreSQL, providing a structured and reproducible workflow for data exploration, processing, analysis, and visualization.

The project is developed using a modular structure to ensure maintainability, scalability, and reproducibility.

## Prerequisites

The following software is required to work with TravelTide:

- **Python 3.14.6** – Main programming language
- **Git** – Version control
- **Visual Studio Code** – Development environment
- **Jupyter Notebook** – Interactive data analysis
- **PostgreSQL** – Relational database management system

The project uses a Python virtual environment (`.venv`) to isolate dependencies and ensure a reproducible development environment.

## Project Setup

### 1. Clone the repository

```cmd
git clone https://github.com/CJJRumpf/TravelTide.git
cd TravelTide
```

### 2. Create a virtual environment

```cmd
py -3.14 -m venv .venv
```

### 3. Activate the virtual environment

```cmd
.venv\Scripts\activate
```

### 4. Install dependencies

```cmd
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Dependencies

TravelTide uses Python packages for data processing, analysis, visualization, database connectivity, and interactive development.

The project dependencies are defined in `pyproject.toml` and `requirements.txt`.

- `pyproject.toml` defines the project configuration and direct dependencies.
- `requirements.txt` contains the exact installed package versions, including transitive dependencies.

### Updating Dependencies

After installing or updating Python packages, update the requirements file using:

```cmd
python -m pip freeze > requirements.txt
```

## Environment Variables

TravelTide uses environment variables to manage database configuration and sensitive credentials.

### Configuration

1. Create a `.env` file in the project root directory.
2. Use `.env.example` as a template.
3. Add your local database credentials to the `.env` file.

Example configuration:

```dotenv
DB_HOST=localhost
DB_PORT=5432
DB_NAME=traveltide
DB_USER=your_username
DB_PASSWORD=your_password
```

### Security

- Never commit the `.env` file to Git.
- The `.env` file is excluded through `.gitignore`.
- Only `.env.example` is tracked in the repository.
- Never store passwords or other sensitive credentials in source code.

## Usage

### Running Python Scripts

Make sure the virtual environment is activated before running Python scripts.

Example:

```cmd
python src/test_environment.py
```

### Working with Jupyter Notebook

Start Jupyter Notebook from the project root directory:

```cmd
jupyter notebook
```

Open the notebook:

```text
notebooks/00_environment_setup.ipynb
```

Make sure to select the **Python 3.14 (TravelTide)** kernel when working with the project notebooks.

## Data Management

TravelTide uses a structured directory layout to organize input data, processed data, and analysis results.

### Directory Structure

- `data/input/` – Raw input data and source files.
- `data/output/` – Processed data and generated output files.
- `notebooks/` – Jupyter notebooks for data exploration and analysis.
- `reports/` – Analysis reports and project results.

### Data Handling

- Raw input data should remain unchanged.
- Processed data should be stored separately from raw data.
- Large datasets and sensitive data should not be committed to GitHub unless explicitly intended.
- Data files should be documented to ensure traceability and reproducibility.

## Security

Security and data protection are important aspects of the TravelTide project.

The following principles apply:

- Never commit passwords, API keys, or database credentials to GitHub.
- Keep the `.env` file local and excluded from version control.
- Use `.env.example` to document required environment variables without exposing sensitive information.
- Review files before committing changes to ensure that no confidential information is included.
- Handle personal and sensitive data responsibly and in accordance with applicable data protection requirements.




## Project Structure

```text
TravelTide/
│
├── .venv/                      # Python virtual environment
│
├── notebooks/                  # Jupyter notebooks
│   └── 00_environment_setup.ipynb
│
├── data/
│   ├── input/                  # Raw input data
│   └── output/                 # Processed data
│
├── src/                        # Python source code
│   ├── __init__.py
│   └── test_environment.py
│
├── reports/                    # Analysis reports
│
├── .env                        # Local environment variables and credentials
├── .env.example                # Example environment configuration
├── .gitignore                  # Git ignore rules
├── README.md                   # Project documentation
├── pyproject.toml              # Project configuration and dependencies
└── requirements.txt            # Python package requirements
```