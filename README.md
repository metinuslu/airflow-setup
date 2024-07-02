# Apache Airflow™
> Airflow™ is a platform created by the community to programmatically author, schedule and monitor workflows.

**Core Concept:** https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/index.html  
**Docs:** https://airflow.apache.org/docs/apache-airflow/stable/index.html  
**Examples:** https://github.com/apache/airflow/tree/main/airflow/example_dags  
**Docker Compose File:** https://airflow.apache.org/docs/apache-airflow/2.9.2/howto/docker-compose/index.html


## Airflow Executors
**Executor Types**
> There are two types of executors - those that run tasks locally (inside the scheduler process), and those that run their tasks remotely (usually via a pool of workers). Airflow comes configured with the SequentialExecutor by default, which is a local executor, and the simplest option for execution. However, the SequentialExecutor is not suitable for production since it does not allow for parallel task running and due to that, some Airflow features (e.g. running sensors) will not work properly. You should instead use the LocalExecutor for small, single-machine production installations, or one of the remote executors for a multi-machine/cloud installation. [More Details](https://airflow.apache.org/docs/apache-airflow/stable/core-concepts/executor/index.html)

**Local Executors**
- Sequential Executor  
- Local Executor    

**Remote Executors**
- CeleryExecutor  
- CeleryKubernetesExecutor  
- KubernetesExecutor  
- KubernetesLocalExecutor  

## Installation with Docker
### Build
- `docker-compose up --build -d`

### Start & Stop
- `docker-compose start`
- `docker-compose stop`

### Drop Containers
- `docker-compose down` 

### Drop Images
- `docker rmi $(docker images -q)`

## Connect Container
- `docker ps`
- `docker exec -it CONT_ID/CONT_NAME bash`

## Other Things

### Import Constant
##### Variable (with Manual)
- `airflow variables export /path/variable.json`
- `airflow variables import /path/variable.json`

##### Connections (with Manual)
- `airflow connections import /path/connections.json`
- `airflow connections export /path/connections.json`

### Install Python Library
##### Requirements File with Initial Step  
Please control the *Dockerfile* and *Requirements.txt*  

##### Directly with Late
- `docker exec -it CONT_ID/CONT_NAME bash (Choose WebServer Container)`
- `pip install LIBRARY_NAME`  

## Test  
- `http://localhost:{8080,8081,8082,8083}/home`
- `http://IP-ADDRESS:{8080,8081,8082,8083}/home`


# Contact
- Metin Uslu & Data Engineering Team