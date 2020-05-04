# python-virtualenv

pip install virtualenv

pip list 

mkdir project

cd project

virtualenv project_env

source project_env/bin/activate

which python

which pip

pip list

pip install numpy

pip list

pip freeze --local > requirements.txt

ls

cat requirements.txt

deactivate



which python

pip list

# delete env

rm -rf project_env

# python 2 environment

virtualenv -p /user/bin/python2.7 project_env_v2



# for pyenv

install https://github.com/pyenv/pyenv-virtualenv

pyenv virtualenv 2.7 project_env_v2

pyenv activate project_env_v2

pyenv deactivate



list virtual environments:

pyenv virtualenvs

# end of pyenv:



source project_env_v2/bin/activate

which python

python --version

pip install -r requirements.txt

pip list

deactivate



Don't create project files inside project_env
