# Security Challenge 3 (60 pts.)
## Description
In this security challenge, you are to develop a user space Host-based Data Leak Prevention System (HDLPS) in C programming language. This is a software filter that runs within a host and captures all incoming and outgoing packets. Captured packets are then inspected based on well-defined criteria. An alert is fired each time these criteria are met. For simplicity, we will be considering UDP traffic only.

The criteria are expressed in terms of:
- Remote IP@: The IP@ of the host from/to which DLP is to be ensured
- Remote UDP port: The UDP port of the remote process from/to which DLP is to be ensured
- Keyword: This is an indication of leaked data
- The number of leaking-data packets to be detected: The programm shall terminate once this number is reached

The HDLPS shall output each alert on the console. The alert shall show the whole leaked content (containing the keyword)

## Running HDLPS
HDLPS requires a Linux box (use a container or a VM if needed), with root/sudo privileges. It shall take the criteria as command line arguments:

sudo ./hdlps [Remote IP@] [Remote UDP Port] [Keyword] [Number of Leaking Packets To Be Detected]

## Developing HDLPS
You shall use [netfilter.org](https://www.netfilter.org/) meta project. More specifically, you will use netfilter.org [iptables](https://www.netfilter.org/projects/iptables/index.html) project, as well as its companion [libnetfilter_queue](https://www.netfilter.org/projects/libnetfilter_queue/index.html) project.
