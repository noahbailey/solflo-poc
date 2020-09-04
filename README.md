# SolFlu

SolFlu is a log server based on Apache Solr and Fluentd. 

The main objective of this system is to offer an experience similar to Elastic Stack, but without the bloat and breaking changes. 

## Setup

It's easy to get started: 

    git clone https://github.com/noahbailey/solflu.git && cd solflu

    docker-compose build
    docker-compose up -d

## Proof of Concept

This project is in its very early stages. Right now, a POC environment exists with the following components: 

* Fluentd listening on 5514/udp for Syslog messages
* A single index Solr server 

## Goals

* Integration with a modern log shipper such as Filebeat
* Log pipelines
* GeoIP lookups for public IPs
* More data sources
    * OSSEC json line format
    * Suricata EVE format
    * Windows perhaps
