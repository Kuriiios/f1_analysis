🏎️ F1 Analysis Ecosystem: Master Repository

This master repository serves as the central hub for the F1 Analysis Ecosystem, a comprehensive suite of projects dedicated to processing, visualizing, and reporting on Formula 1 race data, with a strong focus on the 2025 season.

The ecosystem is logically separated into three independent but connected sub-projects(to do), each focusing on a different part of the data workflow: Backend API, Interactive Frontend Dashboard(Prototype), and Automated Report Generation.

🧩 Project Structure and Component Repositories

This project is composed of three distinct repositories:
Component Repository	Technology	Description	Status
[f1-data-api	Java / Spring Boot	](https://github.com/Kuriiios/f1_analysis_website) Backend & API: Processes raw F1 data, runs core pace/strategy logic, and serves structured data via REST endpoints.	🚧 Under Development
[f1-analysis-dashboard	Python / Streamlit	](https://github.com/Kuriiios/f1_analysis_dashboard) Frontend Dashboard: An interactive web application for real-time and post-session visual analysis and performance comparison.	🚨 Prototype & Active Development
[f1-report-suite	Python / FastF1 / python-pptx	](https://github.com/Kuriiios/f1_analysis_visualization) Report Generator: Automated system for creating professional-grade session reports and visual cards (.pptx, .pdf, .jpeg).	🚨 Multi-Module Prototype

1. 🏁 F1 Analysis Race Data Dashboard (Java/Spring Boot) - The Core Logic

This repository hosts the backend and API core, built using Java and Spring Boot 3+. It is the source of truth for all structured F1 session data and analytical results.

Key Functionality

    Data Model / Entities: Comprehensive entity modeling for F1 data, including Session Metadata, Driver, Team, Timing & Lap Data, and Track & External Factors.

    Data Processing Services: Implements the critical business logic:

        Pace Calculation: Normalizes lap times to compare driver performance accurately.

        Qualifying Logic: Custom handling for Q1, Q2, and Q3 cut-off times.

    API Exposure: Structured RESTful APIs expose processed data, ensuring the dashboard and report suite receive consistent, high-fidelity information.

    Time Formatting: Utility classes ensure standard M:SS.mmm time formatting across all API responses.

2. 📊 F1 Analysis Race Data Dashboard (Streamlit) - The Visualization Layer

This repository contains the interactive frontend dashboard, primarily built with Streamlit and the fastf1 library (currently acting as a standalone prototype, with future integration planned with the Java API).

Core Features

    Multi-View Structure: Provides three main views:

        Main Dashboard View: Multi-panel snapshot for live monitoring (timing, track status, team radio).

        Race Recap View: Focuses on post-race analysis (pace comparison, lap time scatter plots, tyre strategy visualization).

        Home/Overview View: Project landing page.

    Data Styling: Advanced visual enhancements include team colors, highlighting personal bests (green) and overall session bests (purple), and applying correct tyre compound colors.

    User Control: A dynamic sidebar allows users to select Year, Race, Session (including support for Sprint weekends), Team, and visualization parameters.

3. 🏎️ F1 Report Suite — Automated Session & Season Analysis Generator - The Output Engine

This repository hosts the automated report generation suite, built in Python using FastF1 and python-pptx. It turns raw and processed data into professional, shareable media.

Available Report Modules

The suite provides five distinct generators, each producing .pptx reports, .pdf documents, and .jpeg race cards:
Module	Focus Area	Output Format
Practice Report	Pace evolution, stint consistency, tyre degradation.	PPtx, PDF, JPEG
Qualifying Report	Sector deltas, Q-session comparison, theoretical best laps.	PPtx, PDF, JPEG
Race Report	Tyre strategy, pit stop breakdowns, lap charts.	PPtx, PDF, JPEG
Quarter-Season Report	Multi-event averages, trends, cumulative scoring.	PPtx, PDF, JPEG
Head-to-Head Report	Driver-vs-driver lap-by-lap performance.	PPtx, PDF, JPEG

Key Workflow Highlights

    Figure Generation: Uses Matplotlib for F1-style charts.

    Report Assembly: python-pptx is used to dynamically build slides with F1-style typography, team branding, and metrics.

    Conversion Pipeline: Utilizes LibreOffice and Poppler to convert reports from .pptx → .pdf → .jpeg, generating high-resolution outputs suitable for media.

👨‍💻 Author

Cyril Leconte 📍 Créteil, France 📧 cyril.leconte@proton.me
