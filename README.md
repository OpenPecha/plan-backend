#backend for PLAN

## Development
 
```bash
poetry shell
uvicorn plan_api.main:app --reload
```

## Docker (Postgres + Dragonfly) for local setup

Prerequisites:
- Docker Engine and Docker Compose v2 installed

Start the services:
```bash
cd local_setup
docker compose up -d
```

Check status/logs:
```bash
docker compose ps
docker compose logs -f db-local dragonfly
```

Stop the services:
```bash
docker compose down
```
Notes:
- Both services run on the `plan-network` Docker network.
- If ports 5434 or 6379 are in use, stop the conflicting service or adjust the mappings in `local_setup/docker-compose.yml`.


