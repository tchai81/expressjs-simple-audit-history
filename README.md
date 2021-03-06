# Framework

```
Prototype build based on https://github.com/diegohaz/rest
Database: MySQL
ORM - http://docs.sequelizejs.com/
```

## Getting Started

1.  git clone https://github.com/tchai81/demo-api.git <folder-name>
2.  Navigate to the folder

```bash
$ cd <folder-name>
```

3.  Installing dependencies

```bash
$ npm install
```

4.  Replicating .env from .env.example

```bash
$  cp .env.example .env
```

5.  Create a MySQL database on your local and state down all details
6.  Make necessary changes to .env
7.  Execute database migration by navigating to <folder-name>\src

```bash
$  ../node_modules/.bin/sequelize db:migrate
```

8.  To restore database to a clean state

```bash
$ ../node_modules/.bin/sequelize db:migrate:undo:all
```

9.  Start the server

```bash
$ npm run prod
```

## Constraints & Assumptions

1.  For {"key" : "value"} pair, "value" only accepts String
2.  For getting a value for a key with timestamp, if timestamp is earlier than creation date, null will be returned
3.  Unit test is incomplete
4.  While testing on live url, you may encountering server not responding error. Please bear with this as this application is hosted on a free tier service.
