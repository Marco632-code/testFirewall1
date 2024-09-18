# testFirewall1
This is a sample firewall for a website.This is written in shell script. run this file in linux terminal and it creates a firewall with specific requirements. 
#Tools used:
The tools iptables is used for the making of this tool. The shell script contains of linux commands to setup iptables and to setup the firewall with requirements like the open ports which is 80 and 443 in this case. You can change them if you need in the script. 
#changes
you can make furthur changes to the script by using nano firewall1.sh and change the values of the script as desired. The default values are the ports are in default set as 80 and 443. The default configurations are HTTP, TCP, UDP you can add more if you need.
#Logs:
By default, iptables logs are often sent to the system log files, which are commonly located in:

/var/log/syslog (Debian/Ubuntu)
/var/log/messages (CentOS/RHEL)

To monitor the logs in real-time, you can use the tail command with the -f option. This is useful for watching logs as new entries are added.

bash
Copy code
# For Debian/Ubuntu
sudo tail -f /var/log/syslog | grep "iptables dropped"

# For CentOS/RHEL
sudo tail -f /var/log/messages | grep "iptables dropped"
Step 3: Check Existing Logs
If you want to view existing logs rather than monitoring in real-time, you can use the following commands:

bash
Copy code
# For Debian/Ubuntu
sudo grep "iptables dropped" /var/log/syslog

# For CentOS/RHEL
sudo grep "iptables dropped" /var/log/messages

The log entries will typically show details about the dropped packets, including:

Date and Time: When the log entry was created.
Source IP Address: The IP address from which the packet originated.
Destination IP Address: The address of your server.
Protocol: The protocol used (TCP, UDP, etc.).
Port: The port number associated with the traffic

#NOTE:
this tool is not yet completed and tested new updates may come. The tool will be updated soon.
