# Incidents Service

## Overview
The **Incidents Service** is the core component of the platform, responsible for handling all CRUD (Create, Read, Update, Delete) operations related to incidents. It acts as the source of truth for incident states, severities, and resolutions.

## Features
- Exposes APIs to create, update, and manage incidents.
- Stores incident metadata, logs, and state transitions.
- Integrates with the Dependency Service and Worker Service for automated processing.
- Built with Python, FastAPI, and PostgreSQL.

## Getting Started

### Prerequisites
- Python 3.10+
- `pip` package manager
- Docker (optional for containerized deployment)

### Installation
1. Navigate to the service directory:
   ```bash
   cd services/incidents-service
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Service
To run the service locally for development:
```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

## Docker
Build the Docker image:
```bash
docker build -t incident-tracker/incidents-service .
```
Run the Docker container:
```bash
docker run -p 8000:8000 incident-tracker/incidents-service
```
