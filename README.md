# MetricsCatalog

`metrics-catalog` is a full-stack study project of mine. It contains three different codebases which includes a REST API ([metrics-catalog-api](https://github.com/doganozturk/metrics-catalog-api)), a dashboard that visualizes data through consuming that API ([metrics-catalog-dashboard](https://github.com/doganozturk/metrics-catalog-dashboard)) and a tiny client-side JS library ([metrics-catalog-js](https://github.com/doganozturk/metrics-catalog-js)) that collects web performance data on any website it is added on and sends them to the same API.

## Features
- Project uses Git Submodules for organizing three different repositories under single one.
- Project is Dockerized. Specific Dockerfiles can be found on api & dashboard repos. This main repository also includes `docker-compose.yml` for orchestrating the whole project. API, MongoDB and dashboard are connected through this structure.
- JS library is published on NPM. It can be installed in any project with a simple `npm install metrics-catalog-js`. For local development a separate local package can be created of course.
- Project has CI/CD. Known services' free tiers are great for such a purpose of course. I used CircleCI for CI work. Now.sh is used for CD process of dashboard. Heroku is used for CD process of API.
- Projects all have tests to some extent. Builds depend on success of these tests through CI processes.
- Projects have linting & formatting setup. Community favorites Eslint & Prettier are used.
- Projects have pre-commit hooks for linting & tests.
- Projects are written in TypeScript.

## Get Started
`git clone` this repo, then simply use `docker-compose up -d` on the root. This will up API (`http://localhost:3001`), MongoDB and dashboard (`http://localhost:3000`). For JS library you need to get a specific build with correct `.env` variables. Then you can use that on any website you want.  

## Contribution
Pull requests and feature requests are welcome!

## Author
* **Doğan Öztürk** - [Github](https://github.com/doganozturk)