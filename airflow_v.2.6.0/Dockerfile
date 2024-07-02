FROM apache/airflow:2.6.0

WORKDIR /opt/airflow

COPY requirements.txt requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

RUN airflow db upgrade
