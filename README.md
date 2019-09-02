# Ansible Role: Deploy Prometheus

[![Build Status](https://travis-ci.org/dsgnr/ansible-role-deploy-prometheus.svg?branch=master)](https://travis-ci.org/dsgnr/ansible-role-deploy-prometheus)

This role deploys the Prometheus monitoring package on a device. The devices added to the monitoring list in `prometheus.yml` are collected from the Ansible inventory file. The default groups are `monitoring` and `databases`. Customise these to suit your needs.

## Requirements

- A Slack API key

## Role Variables

    prometheus_user: prometheus
    prometheus_group: prometheus
    prometheus_release_version: latest
    prometheus_config_dir: /etc/prometheus
    prometheus_db_dir: /var/lib/prometheus
    alert_manager_url: https://alerts.example.com
    slack_alert_webhook_url: https://hooks.slack.com/services/WEBHOOK_HASH


## Example Playbook

    ---

    - hosts: prometheus

      roles:
        - deploy-prometheus


## License

GNUv3

## Author Information

This role was created by [Dan Hand](https://danielhand.io).

