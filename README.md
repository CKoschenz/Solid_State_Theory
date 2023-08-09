# Solid_State_Theory
Collection of Notebooks and Programs for Solid State Theory

## Git friendly Juypter notebooks

We use nbdev's git hooks for git friendly notebooks. See https://nbdev.fast.ai/tutorials/git_friendly_jupyter.html


## Conda Environment

We a conda environment for portability. For more information on sharing an environment, see [Conda documentation on sharing environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#sharing-an-environment).

### Create the Environment

Use the file `conda_environment.yml` to create the environment with all depenecies necessary to run the notebooks in this repository.
To create an environment called `my_env` from a the file run the command:

`conda env create --prefix <path_to_project>/<my_env>/ --file conda_environment.yml`

### Start the Environment

To start the conda environemt run the command:

`conda activate ./env`

### Install git hooks

`nbdev_install_hooks`

### Export the Environment

To export the environment as a YAML (`.yml`) file we can use the command:

`conda env export --prefix <path_to_project>/<my_env>/ > my_env.yml`

or

`conda env export | cut -f 1 -d '=' | grep -v "prefix"`

The export command stores the new `.yml` file as `my_env.yml` in the current directory.