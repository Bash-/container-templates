# container-templates
A collection of useful Docker Compose configuration files, for speeding up tool deployment

## Contents
### Spark Cluster with PySpark and Jupyter Notebook
For experimenting with PySpark on a Spark Cluster. \
Deploy: ```sudo docker-compose -f docker-compose.yml --spark-worker=[NUMBER_OF_WORKERS]```
 _(Fill in NUMBER_OF_WORKERS, int > 0)_

Use: 
- Access Jupyter Notebook via the link (with access token) found in terminal logs
- Access Spark GUI via http://localhost:8080/
- Volume is mounted on ./notebooks and ./data

Troubleshooting: \
Jupyter Notebook does not have write access on local volume (e.g. ./notebooks): ```sudo chmod 777 ./notebooks```  