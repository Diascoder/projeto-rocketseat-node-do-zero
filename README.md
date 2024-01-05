# Videos Api

> Project based on rocketseat video: [Como sair do ZERO em Node.js em apenas UMA aula](https://youtu.be/hHM-hr9q4mo?si=D1y773dP2GtdJQZg)

## Table of content
- [Videos Api](#video-api)

  - [Installation](#installation)

## Installation

Before start the project locally you must have [docker](https://www.docker.com/),  [docker compose](https://docs.docker.com/compose/) and  [Node.js](https://nodejs.org/en/download) installed on your machine.

First go to the project's ./docker folder and run the following command in the terminal:

``` shell
docker-compose up -d
```

After that, go to the root of the project where package.json is and run the following command to install the dependencies:

``` shell
npm install
```
Following these steps, just run the project start command
```
npm run dev
```

## Endpoints Manual

### Videos endpoint

| Method | Route            | Functionality                   | Body Data                           | Query Params | Auth Required | Content Return   |
| ------ | ---------------- | ------------------------------- | ----------------------------------- | ------------ | ------------- | ---------------- |
| POST   | /videos           | create a new video description | { email: string, password: string } | empty        | false         | empty            |
| GET    | /videos           | show all videos                | empty                               | page: number | false         | User Schema List |
| GET    | /videos/:id       | show video                     | empty                               | empty        | false         | User Schema      |
| GET    | videos?search=    | show video with criteria       | empty                               | empty        | false         | User Schema List |
| PUT    | /videos/:id       | edit video                     | { email: string, password: string } | empty        | false         | empty            |
| DELETE | /videos/:id       | delete video                   | empty                               | empty        | false         | empty            |


## Project Structure

This API was written in [javascript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript) together with the [fastify](https://fastify.dev/) framework for http operations and [postgres](https://www.postgresql.org/) database.

Below is the current project directory structure:

```
├── docker
│   ├── docker-compose.yaml
├── .gitignore
├── database-memory.js
├── database-postgres.js
├── db.js
├── package-lock.json
├── package.json
├── README.md
├── routes.http
├── server.js
```

## Data Schemas

The project have the current data schemas:

- ### Video Schema

```
{
  id: string;
  title: string;
  description: string;
  duration: int;
}
```

