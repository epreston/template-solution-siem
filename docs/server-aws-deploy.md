## AWS Server Deployment

For a more detailed list of commands see:
https://github.com/spujadas/elk-docker/blob/master/Dockerfile

### Prerequisites

A minimum of 4GB RAM assigned to the virtual machine, storage for the virtual machine and expected log files.

### Steps

Install java

```sh
sudo yum -y install java-openjdk java-openjdk-devel
```

Install Elasticsearch

```sh
sudo yum -y install elasticsearch
```

Test the Elasticsearch deployment

```sh
rpm -qi elasticsearch
```

Configure Elasticsearch

```sh
sudo nano /etc/elasticsearch/elasticsearch.yml
```

Enable and Restart the Elasticsearch Service

```sh
sudo systemctl enable --now elasticsearch.service
sudo systemctl restart elasticsearch.service
```

Confirm Elasticsearch Service is Working

```sh
# Confirm service is running
systemctl status elasticsearch.service

# Access JSON interface
curl https://<your-elk-server-ip-here>:9200
```

Install Kibana

```sh
sudo yum -y install kibana
```

Configure Kibana

```sh
sudo nano /etc/kibana/kibana.yml
```

Enable and Restart the Kibana Service

```sh
sudo systemctl enable --now kibana
sudo systemctl restart kibana
```

Confirm Kibana Service is Working

```sh
# Confirm service is running
systemctl status kibana

# Access web interface
curl https://<your-kibana-server-ip-here>:5601
```
