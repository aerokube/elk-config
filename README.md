# Aerokube ELK Stack Configs

This repository contains example configuration files used to send logs from Aerokube products to [Elastic](http://elastic.co/) stack. We are using:
* [Filebeat](https://www.elastic.co/products/beats/filebeat) to collect log files of running Aerokube tools containers.
* [Logstash](https://www.elastic.co/products/logstash) to preprocess log files.
* [ElasticSearch](https://www.elastic.co/products/elasticsearch) to store and index log data.
* [Kibana](https://www.elastic.co/products/kibana) as user interface.

## Quick Start Guide

1) We assume here that you have two hosts: first with Selenoid or Ggr (application host) and second where logs will be stored (ELK host).

2) Go to `beats` directory and copy `etc/filebeat/filebeat.yml` to respective directory on the application host. Don't forget to edit this file and specify correct name of the ELK host.

3) Use `beats/docker-compose.yml` to start `Filebeat` on application host.
4) Go to `elk` directory and copy `etc/logstash/pipeline/pipeline.yml` to respective directory on the ELK host.
5) Start ELK-stack with `elk/docker-compose.yml`.
