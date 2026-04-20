It's assumed that Student is already familiar with working on Jupyter Notebook

Environment Setup : 
  python -m venv mlflow_env
  mlflow_env\Scripts\activate
  pip install --upgrade pip
  pip install mlflow scikit-learn matplotlib pandas ipykernel
  pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
  python -m ipykernel install --user --name=mlflow_env --display-name "Python (MLflow Env)"
  
  Launch MLflow UI : 

    mlflow ui
    Open in browser: http://127.0.0.1:5000
