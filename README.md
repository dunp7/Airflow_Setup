# Docker and Airflow Setup Guide

## Build the Docker Image

Navigate to the `Image` directory:
```bash
cd Image
docker build -t your_custom_image_name .
```

## Run the Container
```bash
docker-compose up -d 
```

## To add DAGs into this setup

### Activate the airflow scheduler
```bash
docker exec -d your_custom_image_name airflow scheduler
```
### How to add file and run

1. Add `py` DAGs file into `dags` directory 
2. Add `py` DAGs file into `scripts` directory

#### Convert ipynb to py file

```bash
python -m nbconvert --to script scripts/your_notebook.ipynb
```

## Access url - Refresh to get update

```bash
localhost:9080
```






