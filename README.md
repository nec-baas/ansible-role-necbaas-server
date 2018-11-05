# Ansible Role: NEC Mobile Backend Platform Server

## Description

Installs API / Console server of NEC Mobile Backend Platform.

## Supports

* RedHat >= 7
* CentOS >= 7

## Requirements

* openjdk >= 8
* tomcat >= 8.5
* MongoDB >= 3.6

## Role Variables

* ``baas_server_tomcat``: Tomcat service name (string, default: tomcat)
* ``baas_server_webapps_dir``: Tomcat webapps directory (string, default: /var/lib/tomcat/webapps)
* ``baas_server_api_base_uri``: External URL of API server (Usually https://[FQDN]/api/) (string, default: https://localhost:8080/api/)
* ``baas_server_api_internal_base_uri``: Internal Base URI of API server  (default: use ``baas_server_api_base_uri``)
* ``baas_server_mongodb_servers``: MongoDB server url (string, default: localhost:27017)
* ``baas_server_mongodb_enable_auth``: Enable MongoDB authentication (boolean, default: false)
* ``baas_server_mongodb_auth_user``: MongoDB auth username (string, default: '')
* ``baas_server_mongodb_auth_password``: MongoDB auth password (string, default: '')
* ``baas_server_mongodb_auth_source``: MongoDB auth DB (string, default:'admin')
* ``baas_server_mongodb_max_conns``: Max connections per MongoDB host (number, default:200)
* ``baas_server_amqp_addrs``: AMQP server addresses (string, default: '')
* ``baas_server_amqp_username``: AMQP auth username (string, default: '')
* ``baas_server_amqp_password``: AMQP auth password (string, default: '')
* ``baas_server_amqp_vhost``: AMQP VHOST (string, default: '')
* ``baas_server_amqp_uri``: AMQP URI (string, default: '')
* ``baas_server_system_no_charge_key``: No charge key (string)

## License

Apache 2.0
