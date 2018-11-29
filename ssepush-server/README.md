# Ansible Role: NEC Mobile Backend Platform SSEPush Server

## Description

Installs SSEPush Server of NEC Mobile Backend Platform.

## attention

Don't use multicast configuration, When clustering is performed.
Please use tcp-ip configuration instead.

## Supports

* RedHat >= 7
* CentOS >= 7

## Requirements

* openjdk >= 8
* tomcat >= 8.5

## Example Playbook

    - hosts: target
      roles:
        - openjdk
        - tomcat
        - necbaas/ssepush-server

## Variables

* ``ssepush_server_tomcat``: Tomcat service name (string, default: tomcat)
* ``ssepush_server_webapps_dir``: Tomcat webapps directory (string, default: /var/lib/tomcat/webapps)
* ``ssepush_amqp_uri``: AMQP URI (string, default:"amqp://rabbitmq:rabbitmq@localhost:5672")
* ``ssepush_hazelcast_port``: Hazelcast: cluster listen port (number, default:5701)
* ``ssepush_hazelcast_multicast_enabled``: Hazelcast: multicast enabled (string, default:"false")
* ``ssepush_hazelcast_multicast_group``: Hazelcast: the address by join multicast group (string, default:"224.2.2.3")
* ``ssepush_hazelcast_multicast_port``: Hazelcast: the port by join multicast group (number, default:54327)
* ``ssepush_hazelcast_tcpip_enabled``: Hazelcast: enable tcp-ip (string, default:"false")
* ``ssepush_hazelcast_tcpip_members``: Hazelcast: the members of tcp-ip. The format is "host:port". (array, default:[])


## License

Apache 2.0

