## Linux Client Deployment

Follow the detailed deployment steps listed under the headings "Self-Managed".

https://www.elastic.co/guide/en/beats/filebeat/8.5/filebeat-installation-configuration.html

### Media

Download: https://www.elastic.co/downloads/beats/filebeat

### Create a Secrets Keystore

Create a `Secrets keystore` following the process described here:

https://www.elastic.co/guide/en/beats/winlogbeat/8.5/keystore.html

### Update the Configuration File

Configure the `filebeat.yml` file, including the IP of the ELK server, substituting sensitive setting values for keys in the key store.

### Test and Load the Config

Run the shell command:

```sh
sudo ./filebeat -e -c filebeat.yml
```

### Client Service Management

Start the service

```sh
sudo ./filebeat -e
```

Set the service to start automatically.

```sh
# sudo systemctl enable --now filebeat
```
