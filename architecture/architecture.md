## System Architecture

The system consists of:

- Windows Endpoint
  - Generates Security, System, and Application logs
- Splunk Universal Forwarder
  - Collects Windows Event Logs
  - Sends data to Splunk Enterprise
- Splunk Enterprise
  - Indexes logs
  - Performs searches, dashboards, and detections

Data Flow:
Windows → Universal Forwarder → Splunk Enterprise → Dashboards

