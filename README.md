https://gabrieltanner.org/blog/grafana-sensor-visualization 

# Docker compose

docker-compose up

# Create the database

docker exec -it influxdb influx

CREATE DATABASE sensors

CREATE USER telegraf WITH PASSWORD 'telegraf'

GRANT ALL ON sensors TO telegraf

# Replace host before deploy 

# Sending data using Golang 

go run mqtt.go

# Access Grafana

Access localhost:3000 (admin/admin)
 
then create the panel as described in the blog 
