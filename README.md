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


