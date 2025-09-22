 Splunk-Lab Analyzing DHCP Log Files Using Splunk SIEM

Introduction 

DHCP (Dynamic Host Configuration Protocol) is the service that automatically assigns IP addresses and other network configuration (like subnet mask, default gateway, DNS servers) to devices on a network. DHCP log files are records maintained by the DHCP server that track events related to IP address allocation Analyzing DHCP logs using Splunk SIEM enables network administrators to monitor IP address usage, detect anomalies, and troubleshoot network issues effectively.

These are DHCPlog files included:

                        IP address assignments – which device got which IP and when(time).
                        Lease times – duration of IP assignment.
                        Device information – MAC addresses, hostnames, or client identifiers.
                        DHCP requests and releases – when devices request or release an IP.
                        Errors – conflicts (e.g., two devices requesting the same IP), failed assignments, or misconfigurations.
                        
Locations of logs depend on the OS and DHCP server:

                        Windows DHCP Server: Usually C:\Windows\System32\dhcp\DhcpSrvLog-*.log
                        Linux (ISC DHCP Server): Often /var/log/syslog or /var/log/dhcpd.log
                                           
  
