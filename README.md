


# Build Image

cd Image
run docker build -t your_custom_image_name . 

# Run 


docker exec -d airflow_webserver airflow scheduler
python -m nbconvert --to script scripts/ticket_analyze.ipynb