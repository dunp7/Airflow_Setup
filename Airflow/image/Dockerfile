FROM apache/airflow:2.10.3-python3.12

USER root
RUN apt update && \
    apt-get install -y openjdk-17-jdk && \
    apt-get install -y ant && \
    apt-get install -y git && \
    apt-get clean;

USER airflow 
COPY requirements.txt .
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# Set JAVA_HOME
ENV JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64/" \
    SPARK_HOME="/home/airflow/.local/lib/python3.12/site-packages/pyspark" \
    PYTHONPATH="${PYTHONPATH}:/opt/airflow/scripts"