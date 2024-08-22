_**Simple IPv4 Packet Sniffer
**_

**Overview**

This project implements a simple IPv4 packet sniffer in Python. It captures and analyzes network packets at the IP layer, extracting key information such as source/destination addresses, protocols, and more. The sniffer leverages raw sockets for low-level access to the network traffic and demonstrates core networking and Python programming concepts.

**Features**:

   - Capture IPv4 packets from the network interface.
   - Display IP header information, including source and destination IP addresses.
   - Extract protocol details such as TCP, UDP, ICMP, and more.
   - Simple and efficient code with clear explanations.


**Installation**


_Prerequisites:_

   - Python 3.x
   - Administrator/root privileges (to use raw sockets)


_Clone the Repository:_

    git clone https://github.com/direktorvolkswagena/python-packet-sniffer
    cd python-packet-sniffer


_Install Dependencies:_

This project doesn't require any external libraries, so no dependencies need to be installed


_Running the Sniffer:_

To run the packet sniffer, use the following command:
      
    sudo python3 sniffer.py


The sniffer will print information about captured IPv4 packets directly to the console.

**_Note: Since working with raw sockets on Windows requires different approach, app works only on Linux_
**

**Example:**

For TCP:

    Ethernet frame #n:
             - Destination: AA:BB:CC:DD:EE:FF, Source: 00:11:22:33:44:55, Protocol: 8
             - IPv4 Packet:
                     - Version: 4, Header Length: 20, TTL: 64
                     - Protocol: 6, Source: 127.0.0.1, Target: 127.0.0.2
             - TCP Segment:
                     - Source Port: 1, Destination Port: 443
                     - Sequence: 222, Acknowledgement: 0
                     - Flags: 
                             - URG: 0, ACK: 0, PSH: 0, RST: 0, SYN: 0, FIN: 0
                     - Data: 
                            any data
For UDP :

    Ethernet frame #n:
             - Destination: FF:FF:FF:FF:FF:FF, Source: AA:AA:AA:AA:AA, Protocol: 8
             - IPv4 Packet:
                     - Version: 4, Header Length: 20, TTL: 128
                     - Protocol: 17, Source: 192.168.0.1, Target: 192.168.0.2
             - UDP Segment:
                     - Source Port: 1, Destination Port: 2, Length: 2
                     - Data:
                             any data
