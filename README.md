# Stock-price-mlops

Stock-price-mlops/
│
├── data/                  # Raw and processed data
├── models/                # Saved models
├── mlruns/                # MLflow tracking
├── .github/workflows/     # CI/CD pipeline YAML
├── src/                   # Source code for training, utils, etc.
├── main.py                # FastAPI app
├── Dockerfile             # Docker build instructions
├── requirements.txt       # Dependencies
└── README.md              


| Tool           | Purpose                          |
| -------------- | -------------------------------- |
| Python         | Core language for model & logic  |
| Git & GitHub   | Version control & remote repo    |
| GitHub Actions | CI/CD orchestration              |
| MLflow         | Model tracking & versioning      |
| DVC            | Data version control             |
| Trivy          | Security vulnerability scanning  |
| Docker         | Containerization                 |
| FastAPI        | API service for model deployment |
| Scikit-learn   | ML modeling                      |
| Pandas/Numpy   | Data manipulation                |


**CI/CD Pipeline Explanation**
The project uses GitHub Actions to automate testing, model validation, and deployment:
1)Push to main triggers GitHub Actions

2)Trivy scans the Docker image for vulnerabilities

3)Tests run with pytest

4)If tests pass, the model is trained and logged to MLflow

5)Model is packaged into a Docker image

6)Docker image is deployed (or uploaded to Docker Hub)

7)Workflow YAML location:
.github/workflows/mlops-pipeline.yml









