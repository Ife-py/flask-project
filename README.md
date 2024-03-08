# Market App

A flask-based ecommerce app.


## Development Setup

This project requires `python 3.12` and uses `pipenv` for managing its dependencies.
If you don't have pip installed globally you can install it with `pip install pipenv`

### Steps
- Clone this repository.
- Switch to the project's root.
- Run `pipenv shell` to initialize a virtual environment for the project.
- Install the project's dependencies with `pipenv install`

### Creating database tables

Currently, the project has only one model. To create the database tables required
by the project.

#### Steps
- You have to set the environmental variable `FLASK_APP` to point to the project's
    entry point i.e. `market.py` on linux you can achieve this with `export FLASK_APP=market`
    If this doesn't work on windows, find the windows equivalent of that command.
- Now we launch a flask shell with `flask shell`. Follow the code snippet that follows to
    create the database tables.

```bash
Python 3.12.1 (main, Dec 29 2023, 21:46:19) [GCC 13.2.1 20230801] on linux
App: market
Instance: /home/gbenga/Documents/Projects/flask-project/instance
>>> from market import db, Item
>>> db.create_all()
>>> exit()
```

### Running the app

You can run the app with `python market.py`