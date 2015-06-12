InfluxDB
========

Install [InfluxDB](http://influxdb.org/) 0.9.x time series database

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value | Description                                                      |
|-----------------------------|---------------|------------------------------------------------------------------|
| influxdb.version            | 0.9.0         | Version to install                                               |
| influxdb.web_admin          | True          | Enable web admin interface                                       |
| influxdb.web_admin_port     | 8083          | Web admin interface port                                         |
| influxdb.http_port          | 8086          | HTTP API endpoint port                                           |
| influxdb.udp                | False         | Enable UDP endpoint                                              |
| influxdb.udp_port           | 4444          | UDP port                                                         |
| influxdb.udp_db             | udp_db        | Database name for UDP data                                       |
| influxdb.config_tpl         | 'influxdb.conf.j2' | A path to config template (to use custom template)               |

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - palkan.influxdb
