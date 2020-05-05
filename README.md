# Python virtual environment management

> virtual environment means a seperated environment from your main global environment

`pip install` installs packages globally for the currently installed python version.

Often we need to works with different versions of python packages as well as python version in different project. Virtual environment comes to this point to help us seperating each project with isolated version of python and python packages. We will use `virtualenv` to create virtual environments.


You can give this a try.

### Table of Contents
- [Installation and usage](#installation-and-usage)
- [Python 2 environment](#python-2-environment)
- [Install packages from requirements.txt](#install-packages-from-requirementstxt)
- [For pyenv users](#for-pyenv-users)


## Installation and usage

```bash
# install virtualenv globally
pip install virtualenv

# show globally installed packages
pip list 

# make a folder for new python project
mkdir project

# go to project folder 
cd project

# create a virtual environment named project_env
virtualenv project_env

# activate virtual environment
source project_env/bin/activate

# check python
which python

# check pip
which pip

# check installed packages, see its listed only locally installed packages 
pip list

# after actvating virtual environment packages will be installed locally
pip install numpy

# check it
pip list

# save locally installed packages to file. It can be used later to install the packages at once.
pip freeze --local > requirements.txt

# see current files
ls

# see details
cat requirements.txt

# deactivate current virtual environment
deactivate

# now check python, its the global version
which python

# list is also showing globally installed packages
pip list

# delete virtual environment is as simple as deleting a folder
rm -rf project_env
```


## Python 2 environment

```bash
# create a virtual environment with different version of python
virtualenv -p path_to_python environment_name
# example: virtualenv -p /user/bin/python2.7 project_env_v2

# activate virtual environment
source project_env_v2/bin/activate

# check python
which python
python --version

```


## Install packages from requirements.txt

```bash
# install packages
pip install -r requirements.txt

#shoe list
pip list
```

> *Don't create project files inside virtual environment folder. For example, here don't create anything inside project_env folder*


## For pyenv users

If you use `pyenv` for managing different pyhton versions then the above process is slightly different.

First install [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)

```bash
# create virtual environment for current global python version
pyenv virtualenv project_env

# create virtual environment for different python version
pyenv virtualenv 2.7 project_env_v2
# unlike raw virtualenv, pyenv virtualenv doesn't create a folder on project directory


# activate a virtual environment
pyenv activate project_env_v2

# deactivate virtual environment
pyenv deactivate

# list all virtual environment
pyenv virtualenvs

# remove virtual environment
pyenv virtualenv-delete project_env_v2
```
