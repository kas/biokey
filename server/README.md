# Server Commands

## Requirements

* Python 3
* Docker
  * postgres image
    * `docker pull postgres`

## To make and start the database

`python make.py`

## To create the database tables

`python create.py`

## To drop the database tables

`python drop.py`

## To empty data from the database tables

`python truncate.py`

## To start the database

`python start.py`

## To stop the database

`python stop.py`

## To remove the database

`python rm.py`

Remove the database volume mounted at `server/db/`

## To run the server locally

`export DATABASE_URL=postgres:///$(whoami)`

`export FLASK_APP=run.py`

`flask run`

## To push to Heroku

Add Heroku remote `heroku git:remote -a herokuprojectname`

Navigate to project root and run `git subtree push --prefix server heroku master`

Create the database tables with `heroku run python util/db/create.py`

