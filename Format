/etc/prometheus/prometheus.yml

Jobs format:

- job_name: "cadvisor-monitoring"
    file_sd_configs:
      - files:
        - /etc/prometheus/targets-hosts-cadvisor.yml

  - job_name: "nginx-exporter"
    file_sd_configs:
      - files:
        - /etc/prometheus/targets-hosts-nginx-exporter.yml

  - job_name: "node-exporter"
    file_sd_configs:
      - files:
        - /etc/prometheus/targets-hosts-node-exporter.yml


target-hosts-format:

- targets: ['ip:8080']
  labels:
    job: cadvisor-monitoring
    instance: <instance-name>

