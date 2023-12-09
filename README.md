Start copying the following template: https://github.com/new?template_name=docker-rails7&template_owner=gjuliao

# Rails 7 on Docker demo application

This app demonstrates Rails 7 with PostgreSQL, import maps, turbo, stimulus and hotwire, all running in Docker.

## Features

* Rails 7
* Ruby 3
* Dockerfile and Docker Compose configuration
* PostgreSQL database
* Redis
* GitHub Actions for 
  * tests
  * Rubocop for linting
  * Security checks with [Brakeman](https://github.com/presidentbeef/brakeman) and [bundler-audit](https://github.com/rubysec/bundler-audit)
  * Building and testing of a production Docker image
* Dependabot for automated updates

## Requirements

Please ensure you are using Docker Compose V2. This project relies on the `docker compose` command, not the previous `docker-compose` standalone program.

https://docs.docker.com/compose/#compose-v2-and-the-new-docker-compose-command

Check your docker compose version with:
```
% docker compose version
Docker Compose version v2.10.2
```

## Initial setup
```
- create a .env file, and add the following variables:
   - POSTGRES_DB=db
   - PGHOST=db
   - POSTGRES_USER=postgres
   - POSTGRES_PASSWORD=password12345
  
docker compose build
docker compose run --rm web bin/rails db:setup
```

## Running the Rails app
```
docker compose up
```

## This template was made thanks to Ryan Williams

- Check original template: https://github.com/ryanwi/rails7-on-docker/generate