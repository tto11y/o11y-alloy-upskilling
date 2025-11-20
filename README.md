# o11y-alloy-upskilling

This repository contains lab material for upskilling on Alloy, the OpenTelemetry collector developed by the Grafana Labs.

Most of the material is based on [Grafana Labs' official Alloy documentation](https://grafana.com/docs/alloy/latest).

## Local Grafana Observability Stack

The [Docker compose file](docker-compose.yml) contains a fully functioning Grafana stack including ...
1. Loki (logs backend)
2. Grafana (observability frontend)
3. Tempo (traces backend)
4. Prometheus (metrics backend)
5. Alloy (Grafana's OpenTelemetry collector)

For the Alloy container to function properly the files [config.alloy](12-Alloy-OTLP-telemetry-pipelines/config.alloy) and [endpoints.json](12-Alloy-OTLP-telemetry-pipelines/endpoints.json) are required.

For the Tempo container to function properly the file [tempo.yaml](12-Alloy-OTLP-telemetry-pipelines/tempo-distributed/tempo.yaml) is required.