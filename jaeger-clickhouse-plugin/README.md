Clone [jaeger-clickhouse](https://github.com/jaegertracing/jaeger-clickhouse) repo locally.

When ClickHouse server has been ready, run in the local repo: `GOOS=linux make build run`

Query traces via ClickHouse server address: `http://localhost:18123` (see screenshot)
