# {{cookiecutter.project_name}}

{% if cookiecutter.open_source_license == "MIT" %}
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
{% elif cookiecutter.open_source_license == "BSD" %} [![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
{% elif cookiecutter.open_source_license == "GPLv3" %} [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)
{% elif cookiecutter.open_source_license == "Apache Software License 2.0" %} [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
{% endif %}
[![Build Status](https://travis-ci.org/{{cookiecutter.github_username}}/{{cookiecutter.repo_name}}.svg?branch=master)](https://travis-ci.org/{{cookiecutter.github_username}}/{{cookiecutter.repo_name}})
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

{{cookiecutter.description}}

## Usage

Create the Python virtual environment with [Pipenv](https://pipenv.readthedocs.io/en/latest/):

```shell
pipenv install --dev
```

To install [`black`](https://github.com/ambv/black) for code formatting, you need to install manually with pip after creating the main environment with pipenv. This is because `black` seems to be permanently in pre-release mode and I don't want to globally enable pre-releases in the `Pipfile`. The command is:

```shell
pipenv run pip install black
```

Then you will need to create an `.env` file where to store your environment variables (SECRET key, plotly credentials, API keys, etc). Do **NOT TRACK** this `.env` file in source control. See `.env.example`.

Run all tests with a simple:

```shell
pytest -v
```

## Run your Dash app

Check that the virtual environment is activated, then run:

```shell
cd {{cookiecutter.package_name}}
python app.py
```

## Code formatting

To format all python files, run:

```shell
black .
```

## Pin your dependencies

```shell
pipenv lock
```

## Deploy on Heroku

Follow the [Dash deployment guide](https://dash.plot.ly/deployment) or have a look at the [dash-heroku-template](https://github.com/plotly/dash-heroku-template)
