# Postgres c PgAdmin и мониторингом (Postgres Exporter, Prometheus, Grafana) развернутые в Docker

* Директорию из проекта `monitoring` поместить в нужную директорию на сервере (по-умолчанию `/home/monitoring`). Указать путь до
  директории в `.env` (`PROMETHEUS_CONFIG`, `GRAFANA_SOURCE`)
* Указать в `monitoring/prometheus/prometheus.yml` в параметре `scrape_configs.static_configs.targets` хост и
  порт Postgres Exporter.
* Указать в `monitoring/grafana/provisioning/datasources/all.yaml` в параметре `datasources.url` URL Prometheus.
* По необходимости поменять параметры с дефолтных в файле `.env`.
