# MLflow and DVC Demo

A small, notebook-based demonstration of experiment tracking with [MLflow](https://mlflow.org/) and scikit-learn. The main notebook trains a Logistic Regression classifier on the Iris dataset and records the run in MLflow. Supporting Word and PowerPoint files provide additional MLflow/DVC learning material.

## Repository contents

- [`mlflow.ipynb`](./mlflow.ipynb) — hands-on Iris classification and MLflow experiment-tracking demo.
- [`DVC Demo.docx`](./DVC%20Demo.docx) — DVC demonstration notes.
- [`MLflow and DVC.pptx`](./MLflow%20and%20DVC.pptx) — presentation material about MLflow and DVC.

## Prerequisites

- Python 3 and `pip`.
- Jupyter Notebook or JupyterLab.
- Familiarity with running notebook cells is helpful.

This repository does not currently include a `requirements.txt`; install the notebook dependencies in a virtual environment as shown below.

## Set up the environment

From the repository directory, create and activate a virtual environment.

### Windows PowerShell

```powershell
python -m venv mlflow_env
.\mlflow_env\Scripts\Activate.ps1
```

If PowerShell prevents activation, you can activate the environment from Command Prompt instead:

```bat
mlflow_env\Scripts\activate.bat
```

### macOS or Linux

```bash
python -m venv mlflow_env
source mlflow_env/bin/activate
```

Then install the packages used by the notebook and register the environment as a Jupyter kernel:

```bash
python -m pip install --upgrade pip
python -m pip install mlflow scikit-learn pandas matplotlib notebook ipykernel
python -m ipykernel install --user --name mlflow_env --display-name "Python (MLflow Env)"
```

## Run the notebook

1. Start Jupyter from the repository directory:

   ```bash
   jupyter notebook
   ```

   Alternatively, run `jupyter lab` if JupyterLab is installed.
2. Open `mlflow.ipynb` in the browser.
3. Select the **Python (MLflow Env)** kernel, then run the cells from top to bottom.
4. The notebook demonstrates an Iris classification experiment using Logistic Regression. It uses the MLflow experiment named `Iris_Experiment`; rerunning the notebook can add more runs to that experiment.

## View experiment runs in MLflow

After running the notebook, open a second terminal, activate the same environment, and change to the repository directory. Start the MLflow tracking UI:

```bash
mlflow ui
```

Open [http://127.0.0.1:5000](http://127.0.0.1:5000) to browse the recorded experiments and runs. Keep the UI process running while viewing the page; stop it with `Ctrl+C` when finished. If port 5000 is already in use, start the UI on another port, for example `mlflow ui --port 5001`, and visit `http://127.0.0.1:5001`.

Run the notebook and start the UI from the same repository directory so both use the same local MLflow tracking data, unless you have explicitly configured a different tracking location.

## Troubleshooting

- **The notebook cannot find a package:** confirm that the notebook is using the **Python (MLflow Env)** kernel and install the missing package in that environment with `python -m pip install <package>`.
- **No runs appear in the UI:** check that the notebook completed its MLflow cells and that the notebook and UI were launched from the same directory and environment.
- **The UI does not start:** use another port with `mlflow ui --port 5001` and open the matching URL.

## Learning goals

- Run a scikit-learn classification example in a Jupyter notebook.
- Record and inspect MLflow experiment runs.
- Explore the accompanying DVC/MLflow presentation and demo material.
