## what is DNS Resulution?
DNS resolution, short for Domain Name System resolution, is the process of converting human-readable domain names into IP addresses. When you enter a website's domain name (e.g., www.example.com) into your web browser, the browser needs to know the corresponding IP address of the server hosting that website to establish a connection.

The Domain Name System (DNS) is a hierarchical decentralized naming system that serves as the phonebook of the Internet. It translates easily memorable domain names into numerical IP addresses, allowing computers to locate and connect with each other over the network. This translation process involves several steps:

1. **Local DNS Cache:** Your device first checks its local DNS cache to see if it already has the IP address for the requested domain. If the information is found, the resolution process is complete, and your device can proceed with connecting to the server.

2. **DNS Resolver:** If the IP address is not found in the local cache, your device contacts a DNS resolver (usually provided by your Internet Service Provider or another third-party DNS service). The resolver is responsible for querying the DNS hierarchy to find the IP address associated with the given domain.

3. **Root DNS Servers:** If the resolver doesn't have the IP address information, it contacts the root DNS servers. These servers have information about the top-level domains (TLDs) like .com, .net, .org, etc.

4. **TLD DNS Servers:** The root DNS servers direct the resolver to the TLD DNS servers that are responsible for specific top-level domains. For example, the .com TLD servers know about all domain names ending in .com.

5. **Authoritative DNS Servers:** The TLD DNS servers provide information about the authoritative DNS servers for the specific domain. The authoritative DNS servers hold the actual IP address information for the requested domain.

6. **IP Address Retrieval:** The resolver contacts the authoritative DNS servers, which provide the IP address associated with the requested domain back to the resolver.

7. **Cache Update:** The resolver caches the IP address locally for future use, and your device uses the obtained IP address to establish a connection with the server hosting the website.

DNS resolution is a critical part of the Internet infrastructure, ensuring that users can access websites using human-readable domain names instead of having to remember numerical IP addresses for every site they want to visit.

## what is TCP handshack?

![image](https://github.com/SushantOps/Networking_For_Devops/assets/109059766/f16886a4-099c-4260-9e02-a98971663d77)

The TCP (Transmission Control Protocol) handshake is a three-step process that establishes a reliable communication connection between two devices, typically a client and a server, before they start exchanging data. This process is part of the TCP/IP suite and is essential for ensuring that both ends of the connection are ready to send and receive data. The TCP handshake is also known as the "three-way handshake."

Here are the three steps involved in the TCP handshake:

1. **SYN (Synchronize):**
   - The process begins with the client sending a TCP packet with the SYN (synchronize) flag set to the server.
   - This packet indicates the client's intention to establish a connection and contains an initial sequence number.

2. **SYN-ACK (Synchronize-Acknowledge):**
   - Upon receiving the SYN packet, the server responds with a TCP packet that has both the SYN and ACK (acknowledge) flags set.
   - The server also chooses its own initial sequence number and includes it in the response.

3. **ACK (Acknowledge):**
   - Finally, the client acknowledges the server's response by sending a TCP packet with the ACK flag set.
   - This packet confirms the establishment of the connection and acknowledges the server's chosen initial sequence number.

After this three-step handshake is completed, the TCP connection is considered established, and both the client and server can start exchanging data. The sequence numbers exchanged during the handshake are crucial for tracking the order of transmitted data and ensuring reliable communication.


