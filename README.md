# Loki 

## Integrting with Grafana

# Set up the sample application

* In this step, you’ll set up the sample application, as well as supporting services, such as Prometheus and Loki.

```
3. Make sure Docker is running:
```
docker ps
```
4. Start the sample application:
```
docker-compose up -d
```
5. Ensure all services are up-and-running:
```
docker-compose ps
```
6. Browse to the sample application on localhost:8081.


## Log in to Grafana

* Grafana is an open-source platform for monitoring and observability that lets you visualize and explore the state of your systems.

1. Open a new tab.
2. Browse to localhost:3000
3. then Log In the dashboard


## Add a logging data source : Loki

* Loki is a Prometheus-inspired horizontally scalable, highly available, multi-tenant log aggregation solution. It is made to be very simple to use and very cost-effective. Instead of indexing the logs' content, it creates a list of labels for each log stream.


1. In the side bar, hover your cursor over the Configuration (gear) icon, and then click Data Sources.
2. Click Add data source.
3. In the list of data sources, click Loki.
4. In the URL box, enter http://loki:3100.
5. Click Save & Test to save your changes.

## Exploring the logs

1. In the side bar, click the Explore (compass) icon.
2. In the data source list at the top, select the Loki data source.
3. In the Query editor, enter:
```
{filename="/var/log/tns-app.log"}
```
4. Grafana displays all logs within the log file of the sample application. The height of each bar encodes the number of logs that were generated at that time.
5. Click and drag across the bars in the graph to filter logs based on time.
