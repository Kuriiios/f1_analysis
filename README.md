# 🏎️ F1 Analysis — Full-Stack Data Ecosystem

This repository serves as the central hub and monorepo for the entire F1 Analysis project suite. It integrates four specialized submodules that collectively form a complete, end-to-end data pipeline: from raw data ingestion and storage to advanced analysis, visualization, and web presentation.

The project is designed to provide comprehensive, high-resolution analytical insights into Formula 1 sessions, focusing on the 2025 season and powered primarily by the FastF1 library and a PostgreSQL backend.

## 🚨 PROJECT STATUS: MULTI-MODULE ARCHITECTURE — ACTIVE DEVELOPMENT 🚧

The overall architecture is validated, with core functionality established across all four submodules. Development efforts are currently focused on refining data processing logic and completing the API/Frontend integration.

## 🧩 Architectural Overview: The Four Pillars

The F1 Analysis Suite is organized into four distinct submodules, each handling a critical step in the data lifecycle.
|Repository | Role in the Pipeline | Core Technology | Description |
| --- | --- | --- | --- |
| [f1_analysis_injestion](https://github.com/Kuriiios/f1_analysis_injestion/) |    Data Source & Storage	|    Python, PostgreSQL    |    Feeds the system. Handles fetching raw F1 data and populating the central PostgreSQL database.|
| [f1_analysis_website](https://github.com/Kuriiios/f1_analysis_website/) |    Backend & API    |    Java (Spring Boot)	|    Serves the data. Provides structured, performant RESTful APIs to access the processed F1 data from the database.|
| [f1_analysis_dashboard](https://github.com/Kuriiios/f1_analysis_dashboard/) |    Interactive Visualization    |    Python (Streamlit)	|    Explores the data. Provides a web-based, real-time (or post-session) dashboard for interactive race and strategy analysis.|
| [f1_analysis_visualization](https://github.com/Kuriiios/f1_analysis_visualization/) |    Automated Reporting	|    Python (FastF1, python-pptx)    |	Generates reports. Automatically produces high-resolution, branded JPEG cards and reports for every session type.|

## 🚀 Getting Started

Since this repository is a container for the submodules, you'll need to clone it recursively to pull all project components.

### Prerequisites

    Git (with submodule support)

    Python ≥ 3.9 (for Ingestion, Dashboard, and Visualization modules)

    Java ≥ 21 (for Website/API module)

    PostgreSQL Database Instance

### Cloning the Project

Use the following command to clone this repository and initialize all four submodules simultaneously:

    git clone --recursive git@github.com:Kuriiios/f1_analysis.git f1_analysis
    cd f1_analysis

### Setup and Workflow

The general deployment workflow follows the data pipeline:

    Database Setup: Configure your PostgreSQL instance and set up the schema using scripts found in the f1_analysis_injestion module.

    Ingestion: Run the scripts in f1_analysis_injestion to populate the database with a desired season's data.

    Backend: Start the Spring Boot application within f1_analysis_website to expose the data via REST APIs.

    Frontend/Analysis: Run or deploy the f1_analysis_dashboard (Streamlit) or execute the generators in f1_analysis_visualization.

## 📂 Repository Structure (Submodules)

Each component is managed as a Git Submodule, allowing for independent development while keeping the overall project unified.
Plaintext

```text
f1_analysis/
│
├── f1_analysis_injestion/    # Data Ingestion Pipeline (Python/PostgreSQL)
├── f1_analysis_website/      # Backend & RESTful API (Java/Spring Boot)
├── f1_analysis_dashboard/    # Interactive Data Dashboard (Python/Streamlit)
├── f1_analysis_visualization/# Automated Report Generator (Python/pptx/jpeg)
│
└── README.md
```

## 🔗 Detailed Component Documentation

For specific instructions on running, configuring, or contributing to a module, please refer to its dedicated README:

* [f1_analysis_injestion](https://github.com/Kuriiios/f1_analysis_injestion/): Details on the data schema and how to load session data.

* [f1_analysis_website](https://github.com/Kuriiios/f1_analysis_website/): API endpoints and service architecture details.

* [f1_analysis_dashboard](https://github.com/Kuriiios/f1_analysis_dashboard/): How to run the Streamlit app and features overview.

* [f1_analysis_visualization](https://github.com/Kuriiios/f1_analysis_visualization/): Report types, generation logic, and export formats.

    
## 👨‍💻 Author

Cyril Leconte 📍 Créteil, France

📧 cyril.leconte@proton.me

🔗 [LinkedIn](https://www.linkedin.com/in/cyril-leconte/) | [Kaggle](https://www.kaggle.com/cyrilleconte)
