Run OpenTelemetry Collector with Docker:

`docker run --network host --name otel -p 145.40.102.147:4317:4317 -p 145.40.102.147:8888:8888 -v $(pwd)/config.yaml:/etc/otelcol-contrib/config.yaml otel/opentelemetry-collector-contrib:0.78.0`

When OpenTelemetry Collector has been ready, use OpenTelemetry Tracegen to generate traces with either duration or number of traces:

`tracegen -otlp-insecure -duration 5s`

`tracegen -otlp-insecure -traces 1`

Another option is Jaeger Tracegen:

`docker run --network host jaegertracing/jaeger-tracegen -trace-exporter otlp-grpc -duration 1h`

Query traces via ClickHouse server address: `http://localhost:18123` (see screenshot)
