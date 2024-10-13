### Hexlet tests and linter status:
[![Actions Status](https://github.com/JuggernautMX/python-project-83/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/JuggernautMX/python-project-83/actions)
[![Project Check](https://github.com/JuggernautMX/python-project-83/actions/workflows/project-check.yml/badge.svg)](https://github.com/JuggernautMX/python-project-83/actions/workflows/project-check.yml)
[![Maintainability](https://api.codeclimate.com/v1/badges/91917d2b5315c84dbe1c/maintainability)](https://codeclimate.com/github/JuggernautMX/python-project-83/maintainability)

Page Analyzer is a site that analyses specified pages for SEO-suitability.
It's [Online on render.com](https://python-project-83-qq6j.onrender.com).
To run the app locally, check the description below.


### Requirements

- [python](https://www.python.org/), version 3.9 or higher
- [poetry](https://python-poetry.org/docs/#installation), version 1.0.0 or higher


### Installation

Clone this repo:
```ch
git clone https://github.com/JuggernautMX/python-project-83.git
```
or download it with pip:
```ch
pip install --user git+https://github.com/JuggernautMX/python-project-83.git
```

Install dependencies:
```ch
cd $PATH_TO_CLONED_DIR <--- Directory where project cloned
make install
```

### Install Database (PostgreSQL)
Use these commands or download DB from [official website](https://www.postgresql.org/download/):
```ch
brew install postgresql             # MacOS
sudo apt install postgresql         # Linux
```

Create database and set schema:
```ch
createdb db
psql db < database.sql
```

### Create .env file
```ch
nano .env
```
And write down the following environment variables (paste your data):
```ch
DATABASE_URL = 'postgres://<username>:<password>@<localhost>:<port>/db'
SECRET_KEY = '$SECRETKEY'
```

### Now package ready to go
Run WSGI HTTP server and follow the [link you will see](http://0.0.0.0:8000):
```ch
make start
```
Or run locally with flask:
```ch
make dev
```
