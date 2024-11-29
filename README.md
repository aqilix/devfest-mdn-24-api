# Google DevFest Medan 2024 Workshop API

This API is purposed for the [Google DevFest 2024 Workshop](https://gdg.community.dev/events/details/google-gdg-medan-presents-devfest-medan-2024/). This is only a simple API that is built with [FastAPI](https://fastapi.tiangolo.com/) and [FastAPIUsers](https://fastapi-users.github.io/fastapi-users/latest/) for user registration, authentication, and authorization.

This API is designed to be as customizable and adaptable as possible.


## Usage
Create your `.env` file, I have provide `.env.dist` as template for configurations. Just run `cp .env.dist .env` to create the file. Then adjust these configurations:


1. `DB_HOST`
   It uses `pgsql` by default for development using docker. Just replace it with the database server IP address once deploying to the server.

```bash
DB_HOST="pgsql"
```

2. `DB_USER`
   It has a default value; just adjust this with the user from your database server.

```bash
DB_USER="postgres"
```

3. `DB_PASS`
   It has a default value; just adjust this with the password from your database server.

```bash
DB_PASS="devfest24"
```

4. `DB_NAME`
   It has a default value; just adjust this with the database name from your database server.

```bash
DB_NAME="app_dev"
```

### Installation
I have prepare `docker-compose.yaml`, so just run these command, then the API will be run in port `8080`

```bash
docker-compose up -d
```


### API Features

-  `POST /auth/register`
-  `POST /auth/jwt/login`
-  `GET  /users/me`
-  `PATCH  /users/me`
-  `GET /authenticated-route`

Please check the Postman collection in the [docs](./docs) folder, then import it to your Postman for trying the API.

### Authors

- [Dolly Aswin Harahap](https://medium.com/@dollyaswin)

### License
The MIT License is used for this project. You can find the full license text here: https://opensource.org/license/mit.
