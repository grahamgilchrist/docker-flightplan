# docker-flightplan
Repo to store automated docker build for a flightplan environment

Based on a basic node environment with the flightplan CLI tool added.

Repo structure is based on the same version fodler convention as official docker hub repos (e.g. python: https://github.com/docker-library/python)

# Usage
* Mount a directory with a `flightplan.js` file and anything else you want to be available (e.g. files to deploy) to `/usr/src/app`
* Run the `fly task:server` command as if locally. See [Flightplan docs](https://github.com/pstadler/flightplan)
* `docker run -v ./:/usr/src/app grahamgilchrist/flightplan:0.6 fly task:server`

# Use with docker compose:
`docker-compose.yaml`:
```
flightplan:
  image: grahamgilchrist/flightplan:0.6
  volumes:
    - ./:/usr/src/app
```
* `docker-compose run flightplan fly task:server`
