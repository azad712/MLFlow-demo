It's assumed that Student is already familiar with working on Jupyter Notebook

Environment Setup : 

Option 1 — Setup Environment Manually (Step-by-step) :

  python -m venv mlflow_env
  
  mlflow_env\Scripts\activate

  pip install --upgrade pip
  
  pip install mlflow scikit-learn matplotlib pandas ipykernel
  
  pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
  
  python -m ipykernel install --user --name=mlflow_env --display-name "Python (MLflow Env)"

Option 2 — Setup Using requirements.txt (Recommended)

If a requirements.txt file is provided in this repository, run:

  pip install -r requirements.txt
  
Launch MLflow UI : 

    mlflow ui
    
    Open in browser: http://127.0.0.1:5000

## MLflow Summary

- The notebook demonstrates experiment tracking with MLflow.
- It trains a Logistic Regression classifier on the Iris dataset.
- Runs are grouped under the `Iris_Experiment` experiment.
- MLflow records run details so experiments can be reviewed and compared.
- Launch `mlflow ui` and open `http://127.0.0.1:5000` to view runs.
