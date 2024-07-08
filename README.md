# Kidney-Disease-Classification-MLflow-DVC

### Project Overview
This project aims to develop and deploy a robust deep learning model for kidney disease classification using ultrasound images. The objective is to enhance early detection accuracy and streamline deployment processes by leveraging various MLOps tools and cloud deployment strategies.

### Workflows

1. Update `config.yaml`
2. Update `secrets.yaml` [Optional]
3. Update `params.yaml`
4. Update the entity
5. Update the configuration manager in `src/config`
6. Update the components
7. Update the pipeline
8. Update the `main.py`
9. Update the `dvc.yaml`

### How to Run?

### STEPS:

#### Clone the Repository

```bash
https://github.com/vogulam2306/kidneydisease.git
```

#### STEP 01 - Create a Conda Environment

```bash
conda create -n kidney python=3.8 -y
conda activate kidney
```

#### STEP 02 - Install the Requirements

```bash
pip install -r requirements.txt
```

#### STEP 03 - Run the Application

```bash
python app.py
```

Now, open up your local host and port.

### DVC Commands

```bash
dvc init
dvc repro
dvc dag
```

### MLflow

[MLflow Documentation](https://mlflow.org/docs/latest/index.html)

#### Commands

```bash
mlflow ui
```

### DagsHub

[DagsHub](https://dagshub.com/)

```bash
MLFLOW_TRACKING_URI=
MLFLOW_TRACKING_USERNAME=
MLFLOW_TRACKING_PASSWORD=
python script.py
```

Run this to export as environment variables:

```bash
export MLFLOW_TRACKING_URI=
export MLFLOW_TRACKING_USERNAME=
export MLFLOW_TRACKING_PASSWORD=
```

## AWS-CICD-Deployment-with-Github-Actions

### 1. Login to AWS Console.

### 2. Create IAM User for Deployment

With specific access:

1. **EC2 Access:** Virtual machine.
2. **ECR:** Elastic Container Registry to save your Docker image in AWS.

**Description:**

1. Build Docker image of the source code.
2. Push your Docker image to ECR.
3. Launch your EC2.
4. Pull your image from ECR in EC2.
5. Launch your Docker image in EC2.

**Policy:**

1. `AmazonEC2ContainerRegistryFullAccess`
2. `AmazonEC2FullAccess`

### 3. Create ECR Repo to Store/Save Docker Image

### 4. Create EC2 Machine (Ubuntu)

### 5. Open EC2 and Install Docker in EC2 Machine

Optional:

```bash
sudo apt-get update -y
sudo apt-get upgrade
```

Required:

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker
```

### 6. Configure EC2 as Self-Hosted Runner

Go to `settings > actions > runner > new self-hosted runner`, choose OS, then run commands one by one.

### 7. Setup GitHub Secrets:

- `AWS_ACCESS_KEY_ID=`
- `AWS_SECRET_ACCESS_KEY=`
- `AWS_REGION=`
- `AWS_ECR_LOGIN_URI=`
- `ECR_REPOSITORY_NAME=simple-app`

## About MLflow & DVC

### MLflow

- Production grade.
- Trace all of your experiments.
- Logging & tagging your model.

### DVC

- Lightweight for POC only.
- Lightweight experiments tracker.
- Can perform orchestration (creating pipelines).

## Key Contributions and Actions

### Development and Environment Setup

- **GitHub for Version Control:** Established a Git-based workflow for efficient collaboration and code management.
- **Docker for Consistent Environments:** Utilized Docker to ensure consistent development, training, and deployment environments.

### Data Management

- **Data Version Control (DVC):** Managed and versioned large datasets to ensure data integrity and reproducibility.
- **Data Collection:** Collected and annotated kidney ultrasound images from open medical repositories.

### Model Development

- **VGG Model Development:** Engineered and trained a VGG model using TensorFlow/Keras.
- **Hyperparameter Optimization:** Fine-tuned hyperparameters to achieve a classification accuracy of 92%.

### Experimentation and Optimization

- **MLflow Integration:** Implemented MLflow for experiment tracking, facilitating iterative model improvements and performance monitoring.

### Automation and Deployment

- **CI/CD Pipelines:** Configured GitHub Actions for automated model training, evaluation, and deployment workflows.
- **AWS Deployment:** Deployed the model on AWS using Docker containers, ensuring scalability and reliability.

### Performance Monitoring

- **Real-time Monitoring:** Integrated Prometheus and Grafana to track and analyze model performance in production.

## Results and Achievements

- **High Accuracy:** Achieved a classification accuracy of 92%.
- **Enhanced Reproducibility:** Improved reproducibility through DVC and MLflow integration.
- **Streamlined Automation:** Automated development and deployment processes with GitHub Actions and Docker.
- **Scalability and Reliability:** Ensured reliable performance monitoring and scalability with AWS deployment.

## Learnings and Skills Acquired

- **MLOps Expertise:** Strengthened skills in integrating MLOps tools and methodologies.
- **Data Versioning and Model Optimization:** Enhanced proficiency in data versioning, model optimization, and performance monitoring.
- **Cloud Deployment:** Gained experience in deploying and monitoring deep learning models in cloud environments like AWS.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
