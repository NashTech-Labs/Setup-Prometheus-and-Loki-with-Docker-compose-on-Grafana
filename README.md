# Loki 

## Integrting with Grafana

# Set up the application in the same directory(as a build context).

1. Start the application by using command:
```
docker-compose up -d
```
2. Ensure all services are up-and-running:
```
docker-compose ps
```

## Log in to Grafana


1. Open a new tab.
2. Browse to localhost:3000
3. then Log In the dashboard

## for prometheus
1. click on add data source.
2. Select "Prometheus".
3. Set the Prometheus server URL (for example, http://localhost:9090/)
4. Click "Save & Test" to save the new data source.


## Add a logging data source : Loki

1. In the side bar, hover your cursor over the Configuration (gear) icon, and then click Data Sources.
2. Click Add data source.
3. In the list of data sources, click Loki.
4. In the URL box, enter http://loki:3100.
5. Click Save & Test to save your changes.

## Exploring the logs

1. In the side bar, click the Explore (compass) icon.
2. In the data source list at the top, select the Loki data source.
3. In the Query editor, type you query
4. Click and drag across the bars in the graph to filter logs based on time.
