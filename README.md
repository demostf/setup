# Setup

Hosting setup for demos.tf

## Usage

Create a `.env` file with the following values:

- HOST: the base domain the site will be hosted from
- PORT: the port the webserver will listen to
- DB_PASSWORD: the password that will be used for the database
- DEMO_ROOT: the folder the demos will be stored in
- EDIT_SECRET: private api key for migrating demos to new url

Start the containers:

```bash
docker-compose up -d
```

## Domain names

The setup uses three domains derived from the base domain.

- ${HOST}: the main site
- api.${HOST}: the backend api and upload code
- static.${HOST}: server uploaded demos
