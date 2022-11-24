# ELK SIEM Project

Repo Template: elasticsearch, logstash, kibana

## Security Information And Event Management (SIEM)

Security information and event management (SIEM) technology supports threat detection, compliance and security incident management through the collection and analysis (both near real time and historical) of security events, as well as a wide variety of other event and contextual data sources. The core capabilities are a broad scope of log event collection and management, the ability to analyze log events and other data across disparate sources, and operational capabilities (such as incident management, dashboards and reporting).

## Server Deployment

This is the centralised log server and log management web interface. This is composed of Elasticsearch, Logstash, and Kibana, collectively known as ELK. The following subsections list deployment options:

### Docker

The docker configuration uses the ELK stack image from https://github.com/spujadas/elk-docker

```sh
sudo docker-compose up
```

Check the status

```sh
docker ps
```

### AWS or Manual

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
curl https://<your-kibana-server-ip-here>:9200
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

## Client Deployment and Event Forwarding

### Linux

```sh

```

### Windows

```sh

```

### Devices

```sh

```

## Getting Started

```sh

```

## References

Elasticsearch
https://github.com/elastic/elasticsearch

Logstash
https://github.com/elastic/logstash

Kibana
https://github.com/elastic/kibana

Docker
https://www.docker.com/

Filebeat and Winlogbeat
https://www.elastic.co/downloads/beats/

Microsoft Security Events
https://www.microsoft.com/en-us/download/details.aspx?id=50034
https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx

## License

See [License](LICENSE).
