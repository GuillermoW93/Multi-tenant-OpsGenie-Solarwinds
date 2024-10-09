# Multi-tenant OpsGenie Integration with Solarwinds via PowerShell

## Overview

This project provides a solution for integrating multiple OpsGenie tenants (teams) with Solarwinds, which is not natively supported. By using a custom property value (e.g., `opsgenie_key`) to store API keys, this PowerShell script reads the custom property value when an alert triggers.

## Prerequisites

- **Local Account**: A local account with full control over the `opsgenie.ps1` script is required.
- **Windows Group Policies**: Ensure the newly created account is added to the following Windows Group Policies:
  - Create a token object
  - Allow log on locally
  - Replace a process level token
  - Act as part of the operating system
  - Log on as a batch job
  - Log on as a service

## Installation

1. **Create Custom Property**: In Solarwinds, create a custom property (e.g., `opsgenie_key`) and add all necessary API keys.
2. **Set Up Local Account**: Create a local account with the required permissions and add it to the specified Windows Group Policies.
3. **Deploy Script**: Place the `opsgenie.ps1` script in a directory accessible by the local account.

## Usage

- The script will read the `opsgenie_key` custom property value when an alert triggers.
- All actions performed by the script are logged in `opsgenie.log` located in the same directory as the script. This log file can be used to verify if an action was called to OpsGenie.

## Logging

The script writes every action to `opsgenie.log` in the same directory, allowing you to verify if an action was called to OpsGenie or not.

## Support

For any issues or questions, please contact [Your Support Contact Information].

## License

[Include your license information here]

