# Run Jupyter Notebooks Programmatically
There are a number of cases where your data scientists have developed some Jupter notebooks and want to run them weekly for data analysis and generating reports.  In such cases, it becomes important to create a worflow and run the notebooks in an automated fashion.

You can achive this goal using `papermill` and `airflow`.

To learn more about `papermill` librray, visit their [papermill repository](https://github.com/nteract/papermill).

## Requirements 
Setting up your `pmill` conda environment: `conda create -n pmill python=3.6`

To activate this environment, run: `conda activate pmill`

To deactivate an active environment, run: `conda deactivate`

If you are experiencing "AttributeError: module 'enum' has no attribute 'IntFlag'" error, run: `unset PYTHONPATH`

You need to install `papermill` in Python 3 kernel.  See `notebooks/setup_environment.ipynb`.

## Running notebooks from command line:
In this demo, we run a sample notebook to which we just pass two parameters and simply print them.  After running the following command, check the `notebooks/output.ipynb` to view the output of your notebook run.

Note that we need to explicitly pass the kernel (i.e. `python3`) when running the notebook using papermill library:


`papermill notebooks/run_me.ipynb notebooks/output.ipynb -p alpha 0.6 -p l1_ratio 0.1 -k python3`
