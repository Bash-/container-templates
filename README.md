# container-templates
A collection of useful Docker Compose configuration files, for speeding up tool deployment


## Spark Cluster with PySpark and Jupyter Notebook
For experimenting with PySpark on a Spark Cluster.
##### Deployment
```
cd spark_cluster-pyspark_notebook
sudo docker-compose up --scale spark-worker=[NUMBER_OF_WORKERS]
```
 _(Fill in NUMBER_OF_WORKERS, int > 0)_

##### Usage
- Access Jupyter Notebook via the link (with access token) found in terminal logs
- Access Spark GUI via http://localhost:8080/
- Volume is mounted on ./notebooks and ./data

##### Troubleshooting
Jupyter Notebook does not have write access on local volume (e.g. ./notebooks): ```sudo chmod 777 ./notebooks```

## PostGIS
Postgres database with PostGIS extension for geospatial analysis 

##### Deployment
Fill in database credentials in file ```database.env```
```
cd postgis
sudo docker-compose up
```
##### Usage
- Access database via local port 8082 using your credentials