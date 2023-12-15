# Conda Environment Setup

The code in this repository was written in Python and made use of Conda for environemntal control. To replicate the coding environment of this repository use the `environment.yml` file using the following steps:

1. Install [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html), [anaconda](https://www.anaconda.com/download/), or [miniconda](https://docs.conda.io/projects/miniconda/en/latest/miniconda-install.html). 

2. Use the `environment.yml` file to create the `dtw_env` environment.

```conda env create -f environment.yml```

3. Activate the environment to run the code.

```conda activate dtw_env ```

*Note: Even theough the `dtaidistance` package does not require a C compiler with OpenMP it is recomended when using the fast version of the functions in the package. make sure to install a C compiler with OpenMP if the fast parallelized version of the distance calcualting function is used. Refer to the `dtaidistance` [Documentation](https://dtaidistance.readthedocs.io/en/latest/usage/installation.html) for help.
