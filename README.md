# Karsajobs
=============================
Karsajobs is simple jobs application written in Go.

## Clone Codebase
```bash
git clone https://github.com/dicodingacademy/karsajobs.git
```

## Build
```bash
cd karsajobs
docker build -t karsajobs:latest .
```

## Run Container
```bash
docker run -d -p 8080:8080 --name "karsajobs-backend" karsajobs:latest
```

## List Running Container
```bash
docker ps
```

## Stop Container
```bash
docker stop karsajobs-backend
```

## Configuration
Karsajobs read configuration from environment variable

| ENV        |      Description                 |
|------------|:---------------------------------|
| APP_PORT   | run karsajobs in specific port   |
| MONGO_HOST | mongodb hostname                 |
| MONGO_USER | mongodb user                     |
| MONGO_PASS | mongodb password                 |


  
## Endpoint
- /jobs
  - `GET` get list job
- /job
  - `POST` create a job  
- /job/id
  - `GET` get job
  - `DELETE` delete job
- /health
  - `GET` check app health status
