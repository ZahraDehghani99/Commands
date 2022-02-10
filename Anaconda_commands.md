# Anaconda
Here I gathered some of important commands in Anaconda.

## Create new environment
If you want to create conda env with specific version of `python` and `pip`, you should run the following command:
```
conda create -n <env_name> python==3.7 pip==20.2.4
```
## Activate an environment
```
conda activate <env_name>
```
## Deactivate an environment
```
conda deactivate <env_name>
```
## Remove an environment
If you want to remove an environment, you should first deactivate this enviroment then run the following command:
```
conda env remove -n env_name
```
## List all the packages in an enviroment
```
conda list
```
## List all the environments
```
conda env list
```
## Create a copy from an environment
```
conda create -n <new_env_name> --clone <my_env>
```
