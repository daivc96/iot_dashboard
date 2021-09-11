https://gabrieltanner.org/blog/grafana-sensor-visualization 

# Docker compose

docker-compose up

# Create the database

docker exec -it influxdb influx

CREATE DATABASE sensors

CREATE USER telegraf WITH PASSWORD 'telegraf'

GRANT ALL ON sensors TO telegraf

# Replace host before deploy 

Replace urls, server in telegraf.conf

# Sending data using Golang 

go run mqtt.go

# Access Grafana

Access localhost:3000 (admin/admin)
 
then create the panel as described in the blog 

# Access Node-RED

Access localhost:1880

# Configure Node-RED (MQTT --> Node RED -> InfluxDB)

![image](https://user-images.githubusercontent.com/37267523/132954934-10ae1e30-8afa-4a22-9acf-ab73c78780d4.png)

1. sensors as "mqtt in"
![image](https://user-images.githubusercontent.com/37267523/132954986-265ee42b-d6bf-4c92-8e2b-09996d9b2c9b.png)

Click server edit
![image](https://user-images.githubusercontent.com/37267523/132954993-fac9e83f-1941-4d6f-af22-c30bd09bafc2.png)

 2. influxdb as "influxdb out"
![image](https://user-images.githubusercontent.com/37267523/132955012-6d49a4ed-e3d8-44af-9bd7-16ef019fefc7.png)

Click server edit

![image](https://user-images.githubusercontent.com/37267523/132955024-7818aee9-3ab0-429f-b902-4712706002b0.png)

