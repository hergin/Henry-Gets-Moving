# Development
This project runs with Node and Node Package Manager (NPM), both of which will be needed to compile it. Running `npm i` at the project root for each repository (backend and frontend) will acquire all the dependencies from `package.json` (such as React, Jest, TypeScript).

## Folder structure
### Frontend
In the frontend repository, the typical directory structure of React is used: under the `src` folder, there is an `Assets` folder, containing images and assets used on pages, a `Components` folder, containing React components' source code to be included on pages, a `Pages` folder, containing actual page React code, and a `Tests` folder, containing unit tests that are run when `npm test` is called. In the root of the project, there are also `package.json` and `package_lock.json`, both of which are typical files included with Node projects that dictate dependencies to be installed with `npm i` and `npm ci`. There is a `Dockerfile`, a `.gitignore`, and a `tsconfig.json` file, with configurations of the TypeScript environment. Also in the `src` folder is `App.tsx`, which is the main renderer of the app, plus various `index.*` files, which dictate the structure of the app when it is run. At the root of the repository, there is a `public` folder, containing the main `index.html` and other assets used by the browser, and there is a `.github` file, containing the YAML code for the automated unit test runner on GitHub Actions.

### Backend
There is an `app` folder, containing controllers for the various tables, exception handlers, Adonis middleware, and models. The `commands` folder only contains a commands to list the directory structure, the `config` folder contains various configurations in TypeScript, the `contracts` folder contains more TypeScript handling authentication, the `database` folder contains Factories, used to mock objects, and Migrations, essentially tables in Adonis. There is a `providers` folder containing a file dictating how the database should be run, a `start` folder containing startup code, and a `tests` folder containing unit tests. In terms of files, there is `.adonisrc` for Adonis configuration, `.dockerignore` for files that shouldn't be included in the Docker container, a `Dockerfile`, `package.json` and `package_lock.json` for Node as explained above, and `server.ts` and `test.ts` which are the entry-points for `node ace serve` and `node ace test`.

## Replication of development environment:
- Clone backend and frontend repositories
> **With Git**:<br>
>   `git clone https://github.com/MarsWilliamsCode/Henry-Gets-Moving-Backend`<br>
>   `git clone https://github.com/kiri-woodruff/Henry-Gets-Moving-Frontend`<br>
> **With GitHub CLI**:<br>
>   `gh repo clone MarsWilliamsCode/Henry-Gets-Moving-Backend`<br>
>   `gh repo clone kiri-woodruff/Henry-Gets-Moving-Frontend`<br>
- For each repository:
  - `cd` into the root directory
  - Run `npm i`
### To run:
- In the backend repository:
  - Run `node ace migration:run`
  - Run `node ace serve`
- In the frontend repository:
  - Run `npm start`
- Navigate to http://localhost:3000 in your browser
### To test:
- In the backend:
  - Make sure your .env declares the MYSQL_HOST as "localhost"
> This means it should have a line `MYSQL_HOST=localhost` somewhere inside a file called `.env` in the repository root
  - Run `node ace test`
    - To run with coverage, use `npm run coverage`
- In the frontend:
  - Run `npm test`
    - To run with coverage, use `npm test -- --coverage`
- Information about how many tests in which suites passed and failed will be displayed

## Replicating via Docker:
### Frontend
- Clone project repository (`git clone https://github.com/kiri-woodruff/Henry-Gets-Moving-Frontend`)
- `cd` into the project directory
- Run `npm start`
- Navigate to http://localhost:3000 in your browser!

### Backend
- Clone project repository (`git clone https://github.com/MarsWilliamsCode/Henry-Gets-Moving-Backend`)
- `cd` into the project directory
- Run `docker compose up`
- Allow the migrations to run

## Linting
### Frontend and Backend
- `cd` into the project directory
- Run `npm run lint`
