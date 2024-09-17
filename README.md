# README

## Versão Utilizada

A versão atual utilizada é a **2.53.2**

## Download

Você pode baixar o Prometheus versão 2.53.2 para Linux AMD64 a partir do seguinte link:

[Download Prometheus 2.53.2](https://github.com/prometheus/prometheus/releases/download/v2.53.2/prometheus-2.53.2.linux-amd64.tar.gz)

## Instruções de Instalação

1. Faça o download do arquivo tar.gz usando o link fornecido.
   ```bash
   wget https://github.com/prometheus/prometheus/releases/download/v2.53.2/prometheus-2.53.2.linux-amd64.tar.gz
   ```
2. Extraia o arquivo com o comando:
   ```bash
   tar -xzvf prometheus-2.53.2.linux-amd64.tar.gz
   ```
3. Renomeie o diretório extraído com o comando:
   ```bash
   mv prometheus-2.53.2.linux-amd64 prometheus
   ```
4. Navegue até o diretório extraído:
   ```bash
   cd prometheus
   ```
5. Inicie o prometheus:
   ```bash
   ./prometheus --config.file=prometheus.yml
   ```

## Inicialização do Prometheus
Com o prometheus em execução, você terá uma saída similar a essa abaixo:
   ```shell
ts=2024-09-17T14:53:59.525Z caller=main.go:589 level=info msg="No time or size retention was set so using the default time retention" duration=15d
ts=2024-09-17T14:53:59.525Z caller=main.go:633 level=info msg="Starting Prometheus Server" mode=server version="(version=2.53.2, branch=HEAD, revision=6e971a7dc905696d4bc4ffa150bf282fcfac5fa9)"
ts=2024-09-17T14:53:59.525Z caller=main.go:638 level=info build_context="(go=go1.22.6, platform=linux/amd64, user=prometheus@deb12, date=20240809-14:55:04, tags=netgo,builtinassets,stringlabels)"
ts=2024-09-17T14:53:59.526Z caller=main.go:639 level=info host_details="(Linux kernel version, architecture=x86_64)"
ts=2024-09-17T14:53:59.526Z caller=main.go:640 level=info fd_limits="(soft=524288, hard=524288)"
ts=2024-09-17T14:53:59.526Z caller=main.go:641 level=info vm_limits="(soft=unlimited, hard=unlimited)"
ts=2024-09-17T14:53:59.530Z caller=web.go:568 level=info component=web msg="Start listening for connections" address=0.0.0.0:9090
ts=2024-09-17T14:53:59.531Z caller=main.go:1148 level=info msg="Starting TSDB ..."
ts=2024-09-17T14:53:59.532Z caller=tls_config.go:313 level=info component=web msg="Listening on" address=[::]:9090
ts=2024-09-17T14:53:59.532Z caller=tls_config.go:316 level=info component=web msg="TLS is disabled." http2=false address=[::]:9090
ts=2024-09-17T14:53:59.539Z caller=head.go:626 level=info component=tsdb msg="Replaying on-disk memory mappable chunks if any"
ts=2024-09-17T14:53:59.539Z caller=head.go:713 level=info component=tsdb msg="On-disk memory mappable chunks replay completed" duration=2.675µs
ts=2024-09-17T14:53:59.539Z caller=head.go:721 level=info component=tsdb msg="Replaying WAL, this may take a while"
ts=2024-09-17T14:53:59.539Z caller=head.go:793 level=info component=tsdb msg="WAL segment loaded" segment=0 maxSegment=0
ts=2024-09-17T14:53:59.539Z caller=head.go:830 level=info component=tsdb msg="WAL replay completed" checkpoint_replay_duration=84.562µs wal_replay_duration=347.475µs wbl_replay_duration=501ns chunk_snapshot_load_duration=0s mmap_chunk_replay_duration=2.675µs total_replay_duration=569.553µs
ts=2024-09-17T14:53:59.544Z caller=main.go:1169 level=info fs_type=XFS_SUPER_MAGIC
ts=2024-09-17T14:53:59.546Z caller=main.go:1172 level=info msg="TSDB started"
ts=2024-09-17T14:53:59.547Z caller=main.go:1354 level=info msg="Loading configuration file" filename=prometheus.yml
ts=2024-09-17T14:53:59.549Z caller=main.go:1391 level=info msg="updated GOGC" old=100 new=75
ts=2024-09-17T14:53:59.550Z caller=main.go:1402 level=info msg="Completed loading of configuration file" filename=prometheus.yml totalDuration=2.61764ms db_storage=1.944µs remote_storage=1.773µs web_handler=1.033µs query_engine=1.182µs scrape=1.960701ms scrape_sd=29.312µs notify=23.352µs notify_sd=9.036µs rules=1.904µs tracing=8.024µs
ts=2024-09-17T14:53:59.550Z caller=main.go:1133 level=info msg="Server is ready to receive web requests."
ts=2024-09-17T14:53:59.550Z caller=manager.go:164 level=info component="rule manager" msg="Starting rule manager..."
   ```

## Prometheus Web UI

Para acessar a interface web do prometheus, basta colar no navegador:

[Prometheus WEB UI](http://localhost:9090)
