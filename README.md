# Cookiecutter Dash

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Powered by [Cookiecutter](https://github.com/audreyr/cookiecutter), Cookiecutter Dash creates a minimal project skeleton for a Dash app.

Styling is with [Bootstrap](https://getbootstrap.com/docs/3.3/).

## Usage

Create a new Dash is as easy as 1-2-3.

1. If you don't already have it, install `cookiecutter` globally:

```shell
pip install cookiecutter
```

2. Run the following command to create the skeleton of your Dash app:

```shell
cookiecutter https://github.com/DC23/cookiecutter-dash
```

3. Follow the instructions in the `README.md` of your generated project.

## Features

Your generated Dash app will have:

- Environment variables loaded from an `.env` file, with [python-dotenv](https://github.com/theskumar/python-dotenv)
- `Procfile` to deploy on Heroku
- Continuous Integration with `.travis.yml` (delete if Travis CI is not required)
- Python code formatting with [black](https://github.com/ambv/black)
- A utility shell script to create a Python virtual environment and create your `Initial commit`

## TODO

- create more tests for this cookiecutter with [pytest-cookies](https://github.com/hackebrot/pytest-cookies).
- add bumpversion config file
- add simple dash callbacks
- More modular project tree?
- Docker integration?
