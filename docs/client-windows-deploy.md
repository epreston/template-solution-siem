## Windows Client Deployment

Follow the detailed deployment steps listed under the headings "Self-Managed".

https://www.elastic.co/guide/en/beats/winlogbeat/current/winlogbeat-installation-configuration.html

### Media

Download: https://www.elastic.co/downloads/beats/winlogbeat

### Create a Secrets Keystore

Create a `Secrets keystore` following the process described here:

https://www.elastic.co/guide/en/beats/winlogbeat/8.5/keystore.html

### Update the Configuration File

Configure the `winlogbeat.yml` file, including the IP of the ELK server, substituting sensitive setting values for keys in the key store.

### Test and Load the Config

Run the powershell command:

```PowerShell
.\winlogbeat.exe test config -c .\winlogbeat.yml -e
```

### Client Service Management

Start the service

```PowerShell
Start-Service winlogbeat
```

Set the service to start automatically.

```PowerShell
Set-Service -Name winlogbeat -StartupType Automatic
```
