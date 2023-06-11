/etc/prometheus/

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

--

cat targets-hosts-cadvisor.yml
- targets: ['ip:8080']
  labels:
    job: cadvisor-monitoring
    instance: <instance-name>

