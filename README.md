# City Temperature Management API

A FastAPI-based application designed to manage city data and track their 
current temperatures using a third-party Weather API.

## Features

* City Management: Create, list, update, and delete cities.
* Temperature Tracking: Fetch current temperatures for all stored cities from weatherapi.com.
* Pagination: Standardized paginated responses for city and temperature lists.
* Async Performance: Fully asynchronous database operations using SQLAlchemy and aiosqlite.
* Migrations: Database version control with Alembic.

## Tech Stack

* Framework: FastAPI
* Database: SQLite (via aiosqlite)
* ORM: SQLAlchemy 2.0
* Validation: Pydantic v2
* Migrations: Alembic
* HTTP Client: HTTPX

## Installing / Getting started

**1. Clone the repository:**
```shell
  git clone https://github.com/Slava-Nykonenko/py-fastapi-city-temperature-management-api.git
  cd py-fastapi-city-temperature-management-api
```

**2. Configure Environment Variables:**

Create a .env file in the root directory, based on the .env.sample file. 
Add your Weather API key.

**3. Install Dependencies:**
```shell
  pip install -r requirements.txt
```

**4. Create and run migrations:**
```shell
  alembic revision --autogenerate -m "Initial migration"
  alembic upgrade head
```
**5. Start the server:**
```shell
  python.exe -m uvicorn main:app --reload 
```
### API Usage examples

**Cities**
* `GET /cities/`: Retrieve a paginated list of cities.
* `POST /cities/`: Register a new city.
* `DELETE /cities/{id}`: Remove a city from the database.

**Temperatures**
* `GET /temperatures/`: View stored temperature data.
* `POST /temperatures/update/`: Triggers a global update that fetches the 
latest weather data for all cities and saves it to the database.

## Links

- Repository: [GitHub](https://github.com/Slava-Nykonenko/py-fastapi-city-temperature-management-api)
- In case of sensitive bugs like security vulnerabilities, please contact
slava.nykon@gmail.com directly. We value your effort to improve the security 
and privacy of this project!
- Related projects:
  - [Emerald Railroads](https://github.com/Slava-Nykonenko/emerald-railroads)
  - [Skyway Airlines](https://github.com/Slava-Nykonenko/skyway-airlines)
  - [Statusphere](https://github.com/Slava-Nykonenko/statusphere)

## Author
Viacheslav Nykonenko<br>
[slava.nykon@gmail.com](mailto:slava.nykon@gmail.com)<br>
[GitHub](https://github.com/Slava-Nykonenko) |
[DockerHub](https://hub.docker.com/repositories/slavanykonenko) |
[LinkedIn](https://www.linkedin.com/in/viacheslav-nykonenko-49211b316/)<br>
+353 85 222 1534 <br>
Carlow, Ireland

## Licensing
The code in this project is licensed under [MIT license](LICENSE.txt).
