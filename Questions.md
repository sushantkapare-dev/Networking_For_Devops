# what is IP Address?
An IP address, or Internet Protocol address, is a numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. It serves two main purposes: host or network interface identification and location addressing. 

There are two types of IP addresses: IPv4 (Internet Protocol version 4) and IPv6 (Internet Protocol version 6). IPv4 addresses are written as a series of four decimal numbers separated by periods, such as 192.168.1.1. However, due to the limited number of available IPv4 addresses, IPv6 was introduced, which uses a longer hexadecimal format, like 2001:0db8:85a3:0000:0000:8a2e:0370:7334.

IP addresses are essential for the proper functioning of the Internet, as they enable devices to find and communicate with each other over a network. Every device connected to the Internet, including computers, smartphones, and servers, is assigned a unique IP address to identify it on the network.

# what is IPv4 and IPv6 address?
IPv4 (Internet Protocol version 4) and IPv6 (Internet Protocol version 6) are two versions of the Internet Protocol, which is the set of rules governing how data is sent and received over the Internet. Both versions are used to assign unique numerical addresses to devices on a network so that they can communicate with each other.

### IPv4 (Internet Protocol version 4):

- **Address Format:** IPv4 addresses are 32-bit numerical labels, typically expressed as four sets of decimal numbers separated by periods (dots). Each decimal number represents 8 bits of the 32-bit address. For example: 192.168.1.1.

- **Address Space:** IPv4 has a finite address space of 2^32 addresses, which is approximately 4.3 billion unique addresses. This limitation has led to the exhaustion of available IPv4 addresses.

- **Usage:** Despite the depletion of IPv4 addresses, it is still widely used and the predominant version of the Internet Protocol.

### IPv6 (Internet Protocol version 6):

- **Address Format:** IPv6 addresses are 128-bit numerical labels, expressed as eight groups of hexadecimal digits separated by colons. For example: 2001:0db8:85a3:0000:0000:8a2e:0370:7334.

- **Address Space:** IPv6 provides an immensely larger address space compared to IPv4, with 2^128 unique addresses. This vast address space is intended to accommodate the growing number of devices connected to the Internet.

- **Usage:** IPv6 has been developed to address the limitations of IPv4 and to ensure the continued growth of the Internet. While its adoption has been slower than anticipated, it is becoming increasingly important as IPv4 addresses become scarce.

# How to calculate CIDR Range?
CIDR (Classless Inter-Domain Routing) notation is a way of representing IP addresses and their associated routing prefix. The CIDR range is expressed as a combination of an IP address and a prefix length, separated by a forward slash (/). The prefix length indicates the number of bits set to "1" in the subnet mask.

Here's a general guide on how to calculate the CIDR range:

1. **Determine the Network Address:**
   - Given an IP address and its subnet mask, find the network address. The network address is obtained by performing a bitwise AND operation between the IP address and the subnet mask.

   Example:
   ```
   IP Address:    192.168.1.25
   Subnet Mask:   255.255.255.0
   Network Address: 192.168.1.0
   ```

2. **Count the Number of Host Bits:**
   - Subtract the prefix length from the total number of bits in an IP address to determine the number of host bits. For IPv4, there are 32 bits, and for IPv6, there are 128 bits.

   Example:
   ```
   Prefix Length:  24 (in IPv4)
   Number of Host Bits: 32 - 24 = 8
   ```

3. **Calculate the Number of Hosts:**
   - The number of hosts in a subnet is calculated as 2 to the power of the number of host bits, minus 2 (subtracting 2 to account for the network and broadcast addresses).

   Example:
   ```
   Number of Hosts: 2^8 - 2 = 254
   ```

4. **Determine the CIDR Notation:**
   - Combine the network address with the prefix length to express the CIDR range.

   Example:
   ```
   CIDR Notation: 192.168.1.0/24
   ```

Here's a brief overview using an IPv6 example:

1. **Determine the Network Address:**
   ```
   IP Address:    2001:0db8:85a3::1
   Prefix Length: 64
   Network Address: 2001:0db8:85a3::/64
   ```

2. **Count the Number of Host Bits:**
   ```
   Number of Host Bits: 128 - 64 = 64
   ```

3. **Calculate the Number of Hosts:**
   ```
   Number of Hosts: 2^64 - 2 (subtracting 2 to account for network and broadcast addresses)
   ```

4. **Determine the CIDR Notation:**
   ```
   CIDR Notation: 2001:0db8:85a3::/64
   ```

Calculating CIDR ranges is crucial for IP address management and efficient routing in networks. It allows for the aggregation of IP addresses into larger blocks, reducing the size of routing tables and improving overall network efficiency.

# what is subnetting?

# Diff between Public and Private Subnet?

# What is the purpose of Ports in Networking?

# what is OSI Model ?

# what is TCP/IP Model?

# Diff between OSI and TCP/IP model?
