# Ansible Role: NEC Mobile Backend Platform Cloud Functions

## Description

Installs Cloud Functions of NEC Mobile Backend Platform.

## Supports

* RedHat >= 7
* CentOS >= 7

## Requirements

* openjdk >= 8

## Role

* openjdk
* system/epel ※ Docker environment only
* docker ※ Docker environment only
* nodejs ※ Dockerless environment only

## Example Playbook

    - hosts: target
      roles:
        - system/epel
        - openjdk
        - { role: docker, when: cloudfn_system_type == 'docker' }
        - { role: nodejs, when: cloudfn_system_type == 'direct' }

        - necbaas/cloudfn-server

## Variables

* ``cloudfn_system_type``: Cloud Functions system type:(docker: Use Docker. direct: Dockerless) (string, default: direct)
* ``cloudfn_amqp_uri``: AMQP URI (string, default: amqp://rabbitmq:rabbitmq@localhost:5672)
* ``cloudfn_spec_node``: Node.js Spec value (string, default: node)
* ``cloudfn_spec_java``: Java Spec value (string, default: java)
* ``cloudfn_system_no_charge_key``: No charge key (string)

### Variables on Docker environment only

* ``cloudfn_docker_uri``: Docker URI (string, default: unix:///var/run/docker.sock)
* ``cloudfn_docker_node_repoTag``: Node server Docker RepoTag (String, default: necbaas/node-logic-server:8)
* ``cloudfn_docker_java_repoTag``: Java server Docker RepoTag (String, default: necbaas/java-logic-server:11)

## License

Apache 2.0
