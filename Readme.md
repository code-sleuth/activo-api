## Activo
An asset-management tool

# Description 
 The **activo-api** is the backbone of an application for managing physical assets of the organisation. The project enables  centralised management of the assets of the organisation.The the api provides features for registering the allocation and usage of assets, repairs and conditions of devices, allocation of computer devices and seat allocations.

 ## Key Application features  
1.	Inventory Management
2.	Asset Allocations
3.	Asset Maintenance & Repair logs


### Dependencies
* <a href ="https://www.python.org">Python</a> A programming language for serverside development
* <a href ="https://www.postgresql.org">Postgres DBMS: </a> An open-source RDBMS for storing data
* <a href ="https://www.sqlalchemy.org">SQLAlchemy ORM: </a>A Python-based ORM for mapping Python objects to DB tables.
* <a href ="https://http://flask.pocoo.org">Flask: </a>A microframework for Python based on Werkzeug, Jinja 2 and good intentions.
* <a href ="https://jwt.io/">JSON Web Token: </a> A JSON-based standard for creating access tokens.
* <a href ="https://www.npmjs.com/package/bcrypt">Bcrypt: </a> A package for hashing password.


## Development set up
- Check that python 3, pip, virtualenv and postgress are installed

- Clone the activo-api repo and cd into it
    ```
    git clone https://github.com/andela/activo-api.git
    ```
- Create virtual env
    ```
    virtualenv --python=python3 venv
    ```
- Activate virtual env
    ```
    source venv/bin/activate
    ```
- Install dependencies
    ```
    pip install -r requirements.txt
    ```
- Create Application environment variables and save them in .env file
    ```
    export APP_SETTINGS="Development" # set app Enviroment.
    export SECRET_KEY="some-very-long-string-of-random-characters"
    export DEV_DATABASE_URL="" # Db for Development.
    export TEST_DATABASE_URL="" # Db for Testing
    export DATABASE_URL="" # Db for Production
    ```
- Running migrations

    - Migrate database to new structure. Run the command below:
        ```
        alembic revision --autogenerate -m "Migration message"
        ```
    - Upgrade to new structure.Run the command below:
        ```
        alembic upgrade head
        ```
- Run application.
    ```
    python manage.py runserver
    ```



## Contribution guide
##### Contributing
All proposals for contribution must satisfy the guidelines in the product wiki.
When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change.This Project shall be utilising a [Pivotal Tracker board](https://www.pivotaltracker.com/n/projects/2170023) to track  the work done.

 ##### Pull Request Process
- A contributor shall identify a task to be done from the [pivotal tracker](https://www.pivotaltracker.com/n/projects/2170023).If there is a bug , feature or chore that has not been included among the tasks, the contributor can add it only after consulting the owner of this repository and the task being accepted.
- The Contributor shall then create a branch off  the ` develop` branch where they are expected to undertake the task they have chosen.
- After  undertaking the task, a fully detailed pull request shall be submitted to the owners of this repository for review. 
- If there any changes requested ,it is expected that these changes shall be effected and the pull request resubmitted for review.Once all the changes are accepted, the pull request shall be closed and the changes merged into `develop` by the owners of this repository.
