InfluxDB
========

Installs [InfluxDB](http://influxdb.org/) 0.11.x time series database

Installation
--------------

`ansible-galaxy install palkan.influxdb`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value | Description                                                      |
|-----------------------------|---------------|------------------------------------------------------------------|
| influxdb_version            | 0.11.1-1         | Version to install                                               |
| influxdb_web_admin          | True          | Enable web admin interface                                       |
| influxdb_web_admin_port     | 8083          | Web admin interface port                                         |
| influxdb_http_port          | 8086          | HTTP API endpoint port                                           |
| influxdb_udp                | None           | List of UDP endpoints configurations (see influxdb.conf.j2 for more info)  |
| influxdb_config_tpl         | 'influxdb.conf.j2' | A path to config template (to use custom template)               |

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - palkan.influxdb
