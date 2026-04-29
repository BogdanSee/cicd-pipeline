# CI/CD Pipeline with GitHub Actions

## Description
A CI/CD pipeline built with GitHub Actions that automatically runs tests
and builds a Docker image on every git push.

## How it works
Every time code is pushed to the main branch, GitHub Actions automatically:
1. Sets up a clean Ubuntu environment
2. Runs all Python tests with pytest
3. Builds a Docker image (only if tests pass)

## Project Structure
- app.py - Python calculator application
- test_app.py - Automated tests (6 tests)
- Dockerfile - Container configuration
- .github/workflows/pipeline.yml - CI/CD pipeline definition

## Pipeline Jobs
- test - Runs pytest, must pass before build
- build - Builds Docker image only if tests pass

## Technologies Used
- Python 3.12
- pytest
- Docker
- GitHub Actions
- Linux/Ubuntu

## Run locally

Bash
# Run the app
python3 app.py

# Run tests
pytest test_app.py -v

# Build Docker image
docker build -t cicd-pipeline .
