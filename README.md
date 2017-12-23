# Docker-Postgres-9.6
Docker Postgres 9.6 for development environment

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
