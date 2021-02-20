# Flask blog  tutorial 

### Create virtual environmnet

 `python3 -m venv venv`

### Activate  virtual env

`source venv/bin/activate`

## Install  dependencies

`pip install -e .`

### Execute application 

`export FLASK_APP=flaskr`

`export FLASK_ENV=development`

`flask init-db`

`flask run`


## Run Tests

`pip install pytest coverage`

## Unit Tests

`pytest`

## Test coverage

`coverage run -m pytest`

## Build and install

Install wheel

`pip install wheel`

create build 

`python setup.py bdist_wheel` creates a file on `dist/` 

Create new virtual environment and past file generated on `dist/`

`pip install flaskr-1.0.0-py3-none-any.whl`

`export FLASK_APP=flaskr`

`flask init-db`

`flask run`

## Configure the Secret Key

`python -c 'import os; print(os.urandom(16))'`

`b'_5#y2L"F4Q8z\n\xec]/'`

On file  `venv/var/flaskr-instance/config.py` paste `SECRET_KEY = b'_5#y2L"F4Q8z\n\xec]/'`

## Run with a Production Server

`pip install waitress`

`waitress-serve --call 'flaskr:create_app'`