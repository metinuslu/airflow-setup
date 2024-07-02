FROM apache/airflow:2.5.3

WORKDIR /opt/airflow

# COPY ..env .env

COPY requirements.txt requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

# CMD ["bash", "-c", "airflow connections import .env/connections_20240626.json && airflow variables import .env/variables_20240626.json"]
