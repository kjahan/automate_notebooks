# papermill_demo
Running Jupyter notebooks programmatically.  There are a number if cases where your data scientist team have developed some Jupter notebooks to run weekly for doing some data analysis and perhaps generate a report or dashboard.  In such cases, it becomes important to create a worflow and run these notebooks. 

You can achive such goals using `papermill` and `airflow` or even simpe cron jobs.

## Requirements 
Setting up your Uatu conda environment: `conda create -n pmill python=3.6`

To activate this environment, run: `conda activate pmill`

To deactivate an active environment, run: `conda deactivate`

If you are experiencing "AttributeError: module 'enum' has no attribute 'IntFlag'" error, run: `unset PYTHONPATH`

You need to install `papermill` in Python 3 kernel.  See `notebooks/setup_environment.ipynb`.

## Run notebook from command line:
In this example, we run a demo notebook in which we just pass two parameters and print them.  After running the following command, check the `notebooks/output.ipynb` to view the output of your notebook run.

Note that we need to explicitly pass the kernel (i.e. `python2`) when running the notebook using papermill:


`papermill notebooks/run_me.ipynb notebooks/output.ipynb -p alpha 0.6 -p l1_ratio 0.1 -k python3`
