# OpsGenie-Solarwinds
Multi-tenant OpsGenie integration with Solarwinds via PowerShell

If you have multiple OpsGenie tentants (multiple teams) you wish to implement in Solarwinds that is natively not possible. 

A solution is to create a custom property value e.g. "opsgenie_key" and add all API-keys, this script will read that custom propery value when the alert triggers. 

In order to make it work, a local account is required which has full control on the opsgenie.ps1 script

Make sure to add the newly created account to all these Windows Group Policies. 
Create a token object
Allow log on locall
Replace a process level token
Act as part of the operation system
Log on as a batch job
Log on as a service
