![Header](/static/header.png)

# Multi-Tenant OpsGenie Integration with Solarwinds via PowerShell

This project provides a solution for integrating **multiple OpsGenie tenants** (teams) with Solarwinds, which is currently not natively supported in version [Solarwinds HCO 2025.1](https://documentation.solarwinds.com/en/success_center/orionplatform/content/release_notes/hco_2025-1-1_release_notes.htm)

 Using a custom property value (e.g., `opsgenie_key`) to store API keys, this PowerShell script reads the custom property value when an alert is triggered.

---

## Overview 🌟

- **Purpose**: Bridge the gap between Solarwinds and OpsGenie for multi-tenant integrations.
- **Technology**: Utilizes PowerShell scripting for seamless automation.
- **Key Feature**: Supports multiple OpsGenie API keys through custom property values in Solarwinds.

---

## Table of Contents
- [Introduction](#overview-)
- [Prerequisites](#prerequisites-️)
- [Installation](#installation-)
- [Usage](#usage-)
- [Logging](#logging-)
- [Contributing](#contributing)
- [About](#about-)



## Prerequisites 🛠️

### Local Account
A local account with full control over the `opsgenie.ps1` script is required.

### Windows Group Policies
Ensure the newly created account is added to the following Windows Group Policies:
- Create a token object
- Allow log on locally
- Replace a process-level token
- Act as part of the operating system
- Log on as a batch job
- Log on as a service

---

## Installation 📥

1. **Create Custom Property**:
   - In Solarwinds, create a custom property (e.g., `opsgenie_key`) and add all necessary API keys.

2. **Set Up Local Account**:
   - Create a local account with the required permissions and add it to the specified Windows Group Policies.

3. **Deploy Script**:
   - Place the `opsgenie.ps1` script in a directory accessible by the local account.

---

## Usage 🚀

- The script reads the `opsgenie_key` custom property value when an alert triggers.
- All actions performed by the script are logged in `opsgenie.log` located in the same directory as the script.
- Use the log file to verify whether an action was successfully performed to OpsGenie.

---

## Logging 📄

Every action is logged to `opsgenie.log` in the script directory, providing complete transparency for debugging and monitoring purposes.

---

## Contributing 🤝

Contributions are welcome! Feel free to fork the repository, make improvements, and submit pull requests. Together, we can make integration even more seamless.

---

## About 👨‍💻

This project aims to simplify multi-tenant OpsGenie integration with Solarwinds, enabling efficient alert management across diverse teams.

Enjoy exploring this solution and happy automating! 😊

![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![SolarWinds](https://img.shields.io/badge/SolarWinds-orange?style=for-the-badge&logo=solarwinds&logoColor=white)
![OpsGenie](https://img.shields.io/badge/OpsGenie-FF5733?style=for-the-badge&logo=opsgenie&logoColor=white)
