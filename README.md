## Prerequisites
1. Should have python version 3.11 install on the system
2. Should have PostgreSQL server setup

## Installation

To run the server :
1. clone the repository with
`git clone <url>`

2. Go into the backend end directory (`./backend`)

3. install _uv_ if not installed with `pip install uv`

4. run the command `uv sync` to install all the dependecies

5. activate the new virtual environment if not activated automatically by running `source .venv/Scripts/activate`

6. Modify variables starting with `POSTGRES` with appropriate values in the .env file in the root directory (one folder above the backend directory)
For PosgreSQL on local system all values will be the same except the `POSTGRES_DB` and `POSTGRES_PASSWORD`.
Create a Database in the PostgreSQL server if one doesn't already exist for the server

7. (_OPTIONAL_) Add starting data into the DB by un-commenting line 19 and line 23 in backend/app/core/db.py and then running the command `python app/initial_data.py` from the backend directory

8. Start the fastAPI server in development mode by running the command `fastapi dev app/main.py'