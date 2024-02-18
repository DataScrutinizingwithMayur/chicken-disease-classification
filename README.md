# Chicken Disease Classification Project

## Overview
This project focuses on classifying fecal specimen images into two categories: coccidiosis fecal and non-coccidiosis fecal. It leverages deep learning models to automate the classification process, providing a robust tool for chicken disease management.

## Technical Workflow

### Configuration Files
- **`config.yaml`**: Update this file to modify the project configuration.
- **`secrets.yaml`** (Optional): Update this file to include any secrets or sensitive information.
- **`params.yaml`**: Define or update parameters for model training and evaluation.
- **Entity and Configuration Management**: Make necessary updates in the `src/config` directory to reflect changes in the entity and configuration manager.

### Components and Pipeline
- Update the components and the pipeline configuration as needed.
- Modify `main.py` and `dvc.yaml` to reflect changes in the project's data processing and model training workflows.

## Installation and Running the Project

### Clone the Repository
git clone https://github.com/DataScrutinizingwithMayur/chicken-disease-classification

### Environment Setup
1. Create and activate a new Conda environment:
conda create -n cnncls python=3.8 -y
conda activate cnncls

2. Install the required dependencies:
pip install -r requirements.txt

3. Run the application:
python app.py

After running, open your local host and port as directed by the application output.

### DVC Commands
To manage and track data versions, use the following DVC commands:
dvc init
dvc repro
dvc dag


## AWS CI/CD Deployment with GitHub Actions

### AWS Setup
1. **IAM User Creation**: Create an IAM user with EC2 access, ECR access for managing docker images, and full access policies:
   - `AmazonEC2ContainerRegistryFullAccess`
   - `AmazonEC2FullAccess`
2. **ECR Repository**: Create an ECR repository to store your docker images. Note the URI for later use.
3. **EC2 Setup**: Launch an EC2 instance (Ubuntu) and install Docker.

### Deployment Steps
1. Build the docker image of the source code.
2. Push the docker image to your ECR repository.
3. Launch your EC2 instance and pull the image from ECR.
4. Launch the docker image in EC2.

### GitHub Actions for CI/CD
- Configure your EC2 as a self-hosted runner.
- Setup GitHub secrets for AWS credentials and repository details.

## Contributing
Contributions are welcome! For major changes, please open an issue first to discuss what you would like to change.
