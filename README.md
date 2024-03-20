# kidney disease classification

## Workflows


1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline
8. Update the main.py
9. Update the dvc.yaml
10. app.py

### How to run?

#### STEPS:Clone the repository

https://github.com/vogulam2306/kidneydisease.git

#### STEP 01- Create a conda environment after opening the repository

conda create -n kidney python=3.8 -y

conda activate kidney 

#### STEP 02- install the requirements

pip install -r requirements.txt

### Finally run the following command
python app.py



export MLFLOW_TRACKING_URI=https://dagshub.com/vogulam2306/kidneydisease.mlflow
export MLFLOW_TRACKING_USERNAME=vogulam2306
export MLFLOW_TRACKING_PASSWORD=328469a285a833106c83198b75a0283965ec6fa6