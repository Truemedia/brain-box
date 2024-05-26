# Brain box
Docker machine for running Mind Stack instance

## Installation
Build images
```bash
  docker-compose build
```

Symlink env file
```bash
  ln -s .env.example .env
```

## Usage
```bash
  docker-compose up
```
### Running specialised stacks
#### NLU (Rasa)
```bash
  docker-compose -f docker-compose.nlu.yml -f docker-compose.db.yml -f docker-compose.queue.yml --env-file config/mongo/.env.example up
```

## Scaffold a new rasa project (in /rasa folder)
docker run -v $(pwd)/rasa:/app rasa/rasa:3.6.20-full init --no-prompt