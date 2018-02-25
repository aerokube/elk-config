# Aerokube ELK Stack Configs

This repository contains example configuration files used to send logs from Aerokube products to [Elastic](http://elastic.co/) stack. We are using:
* [Filebeat](https://www.elastic.co/products/beats/filebeat) to collect log files of running Aerokube tools containers.
* [Logstash](https://www.elastic.co/products/logstash) to preprocess log files.
* [ElasticSearch](https://www.elastic.co/products/elasticsearch) to store and index log data.
* [Kibana](https://www.elastic.co/products/kibana) as user interface.

## Quick Start Guide

1) We assume here that you have two **Linux** hosts: first with Selenoid or Ggr (application host) and second where logs will be stored (ELK host).

2) On application host go to `beats` directory and start Filebeat with Docker Compose:
```
$ cd beats
$ docker-compose up -d
```
3) On the ELK host go to `elk` directory and start ELK stack with Docker compose:
```
$ cd elk
$ docker-compose up -d
```
