
# Ansible Kafka cluster

Ansible роль для развертывания кластера Kafka.


## TL;DR

### Подготовка нод кластера
```
ansible-playbook -i inventory/dev-cluster/hosts.yaml playbook.yaml --tags 'preinstall'
```
### Установка kafka кластера
```
ansible-playbook -i inventory/dev-cluster/hosts.yaml playbook.yaml --tags 'install-kafka'
```
### Настройка kafka кластера
```
ansible-playbook -i inventory/dev-cluster/hosts.yaml playbook.yaml --tags 'configure-kafka'
```
### Установка zookeeper кластера
```
ansible-playbook -i inventory/dev-cluster/hosts.yaml playbook.yaml --tags 'install-zookeeper'
```
### Настройка zookeeper кластера
```
ansible-playbook -i inventory/dev-cluster/hosts.yaml playbook.yaml --tags 'configure-zookeeper'
```
### Установка docker engine
```
ansible-playbook -i inventory/dev-cluster/hosts.yaml playbook.yaml --tags 'install-docker' --limit 'kafka-01-dev'
```
### Running a Docker Image Kafka UI
The official Docker image for UI for Apache Kafka is hosted here: [hub.docker.com/r/provectuslabs/kafka-ui](https://hub.docker.com/r/provectuslabs/kafka-ui).

Launch Docker container in the background:
```sh

docker run -p 8080:8080 \
	-e KAFKA_CLUSTERS_0_NAME=local \
	-e KAFKA_CLUSTERS_0_BOOTSTRAPSERVERS=kafka:9092 \
	-d provectuslabs/kafka-ui:latest

```
Then access the web UI at [http://localhost:8080](http://localhost:8080).
Further configuration with environment variables - [see environment variables](KAFKA_UI.md)


## Environment Variables

Переменные находятся в файле [all.yaml](inventory/dev-cluster/group_vars/all.yaml)

| Name                         | Value                                                  |
|------------------------------|--------------------------------------------------------|
| `disable_grub`               | `false`                                                |
| `system_packages`            | `acl, mc, htop, atop, iotop, rsync ,curl, wget, unzip` |
| `kafka_version`              | `3.3.1`                                                |
| `zookeeper_version`          | `3.8.0`                                                |
| `http_proxy`                 | `""`                                                   |
| `https_proxy`                | `""`                                                   |
| `default_replication_factor` | `2`                                                    |
| `num_partitions`             | `16`                                                   |
| `log_retention_hours`        | `48`                                                   |
| `log_dirs`                   | `/var/lib/kafka`                                       |

## Screenshots Kafka UI

![App Screenshot](https://github.com/provectus/kafka-ui/blob/master/documentation/images/Interface.gif?raw=true?text=kafka-ui)


## Tech Stack

**Client:** Ansible

**Server:** Kafka, Zookeeper


## Authors

- Balakin Alex
- Shekurdyaev Pavel

