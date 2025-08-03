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

## Transfer an environment to another server
When the internet connection in one server is poor, we can follow this instruction to pack and transfer env to another server.

### On Source Server
```
conda install -c conda-forge conda-pack # Install conda-pack if not available
conda pack -n your_env_name -o your_env_name.tar.gz # Pack your environment
scp your_env_name.tar.gz username@destination_ip:/path/to/ # Copy the archive to the destination server
```

### On the target server (with poor internet)
unpack the environment:
```
mkdir -p ~/your_env_name
tar -xzf your_env_name.tar.gz -C ~/your_env_name

```
Activate the environment:

```
source ~/your_env_name/bin/activate
```
