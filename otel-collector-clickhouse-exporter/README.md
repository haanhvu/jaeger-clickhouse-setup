Run OpenTelemetry Collector with Docker:

`docker run --network host -v $(pwd)/config.yaml:/etc/otelcol-contrib/config.yaml otel/opentelemetry-collector-contrib`

When OpenTelemetry Collector has been ready, generate traces with either duration or number of traces:

`tracegen -otlp-insecure -duration 5s`

`tracegen -otlp-insecure -traces 1`

Query traces via ClickHouse server address: `http://localhost:18123` (see screenshot)
