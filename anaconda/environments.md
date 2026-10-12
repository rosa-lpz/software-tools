## Environments

### Create environments

```bash
conda create --name <my-env>
```

With an specific Python version

```bash
conda create -n myenv python=3.8
```

#### Delete environment

```bash
conda remove --name ENV_NAME --all
```

`ENV_NAME` denotes the name of the environment to be removed/deleted. Make sure you deactivate an environment before removing it by running the `conda deactivate` command.

The `--all` flag removes all the packages installed in that environment.

Here's a summary of the steps involved in deleting an environment in Conda:

- Deactivate the environment using the `conda deactivate` command.
- Delete the environment using the `conda remove --name ENV_NAME --all` command.

**References**

* https://www.freecodecamp.org/news/how-to-delete-an-environment-in-conda/

### Examples

```bash
Examples:  
  
Remove the package 'scipy' from the currently-active environment::  
  
   conda remove scipy  
  
Remove a list of packages from an environment 'myenv'::  
  
   conda remove -n myenv scipy curl wheel  
  
Remove all packages from environment `myenv` and the environment itself::  
  
   conda remove -n myenv --all  
  
Remove all packages from the environment `myenv` but retain the environment::  
  
   conda remove -n myenv --all --keep-env
```

