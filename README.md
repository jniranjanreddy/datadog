# datadog

## How to install datadog in Linux servers.
```
DD_API_KEY=xxxxxxxxxxxxxxxxxxx DD_SITE="us5.datadoghq.com" bash -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"
```

## How to install datadog in Windows servers, Through Command Prompt
```
start /wait msiexec /qn /i datadog-agent-7-latest.amd64.msi APIKEY="XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" SITE="us5.datadoghq.com"
```
## How to install datadog in Windows servers, Through PowerShell
```
Start-Process -Wait msiexec -ArgumentList '/qn /i datadog-agent-7-latest.amd64.msi APIKEY="XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" SITE="us5.datadoghq.com"'
```
## How enable Network Monitor
```
cat system-probe.yaml | head
To do Network Monitor, need to enable SNMP.
########################################
## System Probe Network Configuration ##
########################################

  network_config:
  ## @param enabled - boolean - optional - default: false
  ## Set to true to enable the Network Module of the System Probe
  #
    enabled: true
```
```
Systemctl restart sshd
```
