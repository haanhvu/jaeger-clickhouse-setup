Run OpenTelemetry Collector with Docker:

`docker run --rm --network host --name otel -p 147.28.187.125:4317:4317 -p 147.28.187.125:8888:8888 -v $(pwd)/config.yaml:/etc/otelcol-contrib/config.yaml otel/opentelemetry-collector-contrib`

When OpenTelemetry Collector has been ready, use OpenTelemetry Tracegen to generate traces with either duration or number of traces:

`tracegen -otlp-insecure -duration 5s`

`tracegen -otlp-insecure -traces 1`

Another option is Jaeger Tracegen:

`docker run --network host jaegertracing/jaeger-tracegen -trace-exporter otlp-grpc -duration 1h`

Query traces via ClickHouse server address: `http://localhost:18123` (see screenshot)
