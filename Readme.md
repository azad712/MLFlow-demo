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
