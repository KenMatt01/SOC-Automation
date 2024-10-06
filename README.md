# SOC Automation Project

### Description
This SOC Automation project aims to streamline and enhance Security Operations Center (SOC) efficiency by integrating security monitoring tools and automating key incident response tasks. The project uses Wazuh for threat detection and log analysis, TheHive for case management and incident tracking, and Shuffle for orchestrating and automating workflows.

Key Achievements:
- *Streamlined Threat Detection and Response*<br>
  Automated the integration between Wazuh and TheHive through Shuffle SOAR to enhance real-time threat detection, incident alerting, and response management across the SOC.

- *Efficient Case Management*<br>
  Developed an automated workflow to generate alerts in TheHive based on suspicious activity detected by Wazuh, improving the efficiency of case creation and incident management for security teams.

- *Automated Mimikatz Detection*<br>
  Built a custom detection and alerting mechanism to automatically identify Mimikatz usage on endpoints, incorporating key details like the host, user, process ID, and severity into the alerts.

- *Customized SOAR Workflows*<br>
  Created and deployed multiple Shuffle workflows for automated incident response, including tasks like enriching alerts with threat intelligence, assigning cases to analysts, and responding to incidents in real-time.

- *Seamless Integration of On-Premise SOC Tools*<br>
  Successfully integrated on-premise Wazuh and TheHive instances with Shuffle, enabling security automation without relying on cloud services while maintaining the scalability and security of the environment.

- *Reduction in Incident Response Time*<br>
  Achieved significant reduction in incident response times by leveraging automated workflows for detecting, triaging, and responding to security events, reducing manual intervention and improving SOC efficiency.

- *Comprehensive Log Analysis and Threat Monitoring*<br>
  Enhanced the ability to monitor and analyze large volumes of logs for threat detection, leveraging Wazuh’s SIEM capabilities to automate log analysis and send meaningful alerts to TheHive for case management.

- *Secure and Scalable Deployment*<br>
  Deployed the entire SOC automation stack, including Shuffle, Wazuh, and TheHive, on individual Linux server VMs, ensuring a secure and scalable environment for ongoing SOC operations.

### Enviornments
- Windows 10
- Linux Ubuntu Servers LTS 20.0.4

### Language & Utilities
- Sysmon
- Wazuh
- TheHive
- Shuffle
- SMTP EMAIL

### System Methodology

![Screenshot 2024-10-06 203950](https://github.com/user-attachments/assets/1cfead1b-4bdc-445c-a9d0-3e9f9abb2fb8)

