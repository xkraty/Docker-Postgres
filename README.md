# Docker Postgres
Docker Postgres for development environment
## Requirements
```
brew install libpq
```

## Rails
```
gem install pg -v '0.21.0' --without-pg
```

## Running postgres
```
docker-compose up
```

To run daemonized
```
docker-compose up -d
```

To stop daemon
```
docker-compose postgres stop
```

## PSQL
```
docker exec -it postgres psql -h postgres -U pguser
```

## Bash

It still an alpine machine
```
docker exec -it  postgres bash
```

## Aliases
```
alias postgres_start="docker-compose -f ~/projects/postgres/docker-compose.yml up -d"
```

```
alias postgres_stop="docker-compose -f ~/projects/postgres/docker-compose.yml stop"
```

```
alias psql="docker exec -it postgres psql -h postgres -U pguser"
```


## PG Dump All

```
docker-compose exec -it postgres pg_dumpall -U pguser > pgdump
```

## Restore All

```
docker exec -i postgres psql -U pguser < pgdump
```
