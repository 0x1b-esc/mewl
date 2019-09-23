McAfee ESM + Winlogbeat + Logstash

## What is MEWL?
MEWL is a project that aims to ingest Windows Events into the McAfee Enterprise Security Manager.  This is accomplished by setting utilizing the following tools:

Windows Server with Windows Event Forwarding. Instructions for setting this up can be found at:</ul>
https://docs.microsoft.com/en-us/windows/security/threat-protection/use-windows-event-forwarding-to-assist-in-intrusion-detection
Elastic's Winlogbeat
Elastic's Logstash
https://www.elastic.co/
McAfee Event Receiver
McAfee Enterprise Security Manager

Basically, the idea is to install Winlogbeat onto your Windows Event Collection Server and send events to a Receiver.  From the receiver, a logstash instance is set up which will take the events and then forward it to itself voa Syslog(a source set up as 127.0.0.1).
