# ELK SIEM Project

Repo Template: elasticsearch, logstash, kibana

## Security Information And Event Management (SIEM)

Security information and event management (SIEM) technology supports threat detection, compliance and security incident management through the collection and analysis (both near real time and historical) of security events, as well as a wide variety of other event and contextual data sources. The core capabilities are a broad scope of log event collection and management, the ability to analyze log events and other data across disparate sources, and operational capabilities (such as incident management, dashboards and reporting).

## Server Deployment

This is the centralised log server and log management web interface. This is composed of Elasticsearch, Logstash, and Kibana, collectively known as ELK. This configuration will be equivalent to the ELK stack image from https://github.com/spujadas/elk-docker using one of the following options.

- [Docker](docs/server-docker-deploy.md)
- [AWS](docs/server-aws-deploy.md)
- [Azure](docs/server-azure-deploy.md)
- [Manual](docs/server-manual-deploy.md)

## Client Deployment

OpenTelemetry defines three flavors of telemetry — distributed traces, metrics, and logs. This component is the log implementation of "instrumentation and observability" for infrastructure.

- [Linux](docs/client-linux-deploy.md)
- [Windows](docs/client-windows-deploy.md)
- [Devices](docs/client-device-deploy.md)

## Getting Started

```sh

```

## References

| Item                      | Reference                                                                     |
| ------------------------- | ----------------------------------------------------------------------------- |
| Elasticsearch             | https://github.com/elastic/elasticsearch                                      |
| Logstash                  | https://github.com/elastic/logstash                                           |
| Kibana                    | https://github.com/elastic/kibana                                             |
| Filebeat and Winlogbeat   | https://www.elastic.co/downloads/beats/                                       |
| Microsoft Security Events | https://www.microsoft.com/en-us/download/details.aspx?id=50034                |
|                           | https://www.ultimatewindowssecurity.com/securitylog/encyclopedia/default.aspx |
| Docker                    | https://www.docker.com/                                                       |
|                           | https://github.com/phusion/baseimage-docker                                   |
| Ubantu                    | https://ubuntu.com/download/server                                            |

## License

See [License](LICENSE).
