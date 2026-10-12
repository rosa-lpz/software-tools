# Anaconda commands

```bash
# Create--
conda create -name ENV_NAME python=python_version
conda create -n ENV_NAME python=python_version

# ActivateEnvironments--
conda activate

# See-list-libraries
conda list

# Activate-Specific-Environment--
conda activate <env_name>

# List-all-the-environments--
conda env list

# Deactivate-environment--
conda deactivate

# Update---
conda update -n base -c defaults conda

# Delete-environment--
conda remove --name ENV_NAME --all

# Delete-environment with libraries--
conda remove --n ENV_NAME --all

# Install packages
conda install <package>
```

# **References**

* https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/installing-with-conda.html

## 