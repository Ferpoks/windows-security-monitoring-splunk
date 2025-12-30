## Windows Event Logs Collection

The following logs are collected using Splunk Universal Forwarder:

- Security
- System
- Application

Configuration:
- inputs.conf
- Logs are indexed into: wineventlog
- Data collection verified using:
  index=wineventlog | head 20

