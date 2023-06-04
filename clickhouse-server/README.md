Run ClickHouse server:

`docker run --rm -it -p 18123:8123 -p9000:9000 --name some-clickhouse-server --ulimit nofile=262144:262144 clickhouse/clickhouse-server:22`
