# This script will be started from a Solarwinds alert trigger "Request for external program".
# This script will run a HTTP Rest API Request to OpsGenie for routing a standby call.
# The parameters required for opsgenie are passed as parameters in the Solarwinds alert trigger.

# Turn on highest version of TLS
[Net.ServicePointManager]::SecurityProtocol = "tls12, tls11, tls"

# OpsGenie URL
$opsgenie_url = "https://api.opsgenie.com/v2/json/solarwinds?apiKey="

# Default logfile
$Logfile = "C:\opsgenie\opsgenie.log"

# split the apikey from the name (the name is only used in Solarwinds and 
# logging for clarification, this is not used for opsgenie)
if ($args[0]) {
  if ($args[0].Contains("_")) {
    $opsgenie_url = $opsgenie_url + $args[0].Split("_")[0]
    $opsgenie_group = $args[0].Split("_")[1]
  } else {
    $opsgenie_url = $opsgenie_url + $args[0]
    $opsgenie_group = "no opsgenie group name passed as parameter (no comma seperator found in the string)"
  }
} else {
  $opsgenie_url = "no api key passed from Solarwinds as parameter"
}

$body = @{
    ActionType='Create'
    alias=$args[1]
    ObjectID=$args[2]
    NodeName=$args[3]
    AlertID=$args[4]
    AlertDefID=$args[5]
    AlertName=$args[6]
    AlertMessage=$args[7]
    AlertDescription=$args[8]
    AlertDetailsUrl=$args[9]
    DownTime=$args[10]
    AcknowledgeUrl=$args[11]
    Acknowledged=$args[12]
    AcknowledgedBy=$args[13]
    AcknowledgedTime=$args[14]
    AlertTriggerCount=$args[15]
    AlertTriggerTime=$args[16]
    LastEdit=$args[17]
    ObjectType=$args[18]
    Severity=$args[19]
    TimeOfDay=$args[20]
    DateTime=$args[21]
    responders=$args[22]
    tags=$args[23]
}

if (($args[0])) {
    # API Request
    $response = Invoke-RestMethod -Uri $opsgenie_url -Method "Post" -Body ($body | ConvertTo-Json)  -Proxy 'http://[ip]:[port]' -ContentType "application/json"
} else {
    $opsgenie_url = "No REST Request executed (APIKey parameter is empty)"
}


# Log the request to the logfile
write-Output "------------------------------------------------">> $Logfile
write-Output "Opsgenie group : $opsgenie_group" >> $Logfile
write-Output "Uri            : $opsgenie_url" >> $Logfile
write-Output "Date           : $($body.DateTime)" >> $Logfile
write-Output "Nodename       : $($body.NodeName)" >> $Logfile
write-Output "AlertMessage   : $($body.AlertMessage)" >> $Logfile
write-Output "Solarwinds args: $($body | ConvertTo-Json)" >> $Logfile
write-Output "Response       :" >> $Logfile
write-Output $response | ConvertTo-Json >> $Logfile
write-Output " " >> $Logfile

Write-Host "Rest API Request to OpsGenie executed."
