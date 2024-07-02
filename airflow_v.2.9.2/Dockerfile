FROM apache/airflow:2.9.2

WORKDIR /opt/airflow

# COPY .env .env

COPY requirements.txt requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

# RUN airflow db init
# RUN airflow variables import /opt/airflow/.env/variables_20240626.json
# RUN airflow connections import /opt/airflow/.env/connections_20240626.json

# CMD ["bash", "-c", "airflow db init && airflow connections import /opt/airflow/.env/connections_20240626.json && airflow variables import /opt/airflow/.env/variables_20240626.json"]
