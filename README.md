## TCP/IP (Protocols and Networking Basics)

The TCP/IP model is a fundamental framework for computer networking. It stands for Transmission Control Protocol/Internet Protocol, which are the core protocols of the Internet. This model defines how data is transmitted over networks, ensuring reliable communication between devices. It consists of four layers: the Link Layer, the Internet Layer, the Transport Layer, and the Application Layer. Each layer has specific functions that help manage different aspects of network communication, making it essential for understanding and working with modern networks.

TCP/IP was designed and developed by the Department of Defense (DoD) in the 1960s and is based on standard protocols. The TCP/IP model is a concise version of the OSI model. It contains four layers, unlike the seven layers in the OSI model. In this article, we are going to discuss the TCP/IP model in detail.

TCP/IP model was developed alongside the creation of the ARPANET, which later became the foundation of the modern internet. It was designed with a focus on the practical aspects of networking at the time. The lower-level hardware details and physical transmission medium were largely abstracted away in favor of higher-level networking protocols.

### **What Does TCP/IP Do?**

The main work of TCP/IP is to transfer the data of a computer from one device to another. The main condition of this process is to make data reliable and accurate so that the receiver will receive the same information which is sent by the sender. To ensure that, each message reaches its final destination accurately, the TCP/IP model divides its data into packets and combines them at the other end, which helps in maintaining the accuracy of the data while transferring from one end to another end. The TCP/IP model is used in the context of the real-world internet, where a wide range of physical media and network technologies are in use. Rather than specifying a particular Physical Layer, the TCP/IP model allows for flexibility in adapting to different physical implementations.

### **Difference Between TCP and IP**

| Feature | TCP (Transmission Control Protocol) | IP (Internet Protocol) |
| :---: | ----- | ----- |
| **Purpose** | Ensures reliable, ordered, and error-checked delivery of data between applications. | Provides addressing and routing of packets across networks. |
| **Type** | Connection-oriented | Connectionless |
| **Function** | Manages data transmission between devices, ensuring data integrity and order. | Routes packets of data from the source to the destination based on IP addresses. |
| **Error Handling** | Yes, includes error checking and recovery mechanisms. | No, IP itself does not handle errors; relies on upper-layer protocols like TCP. |
| **Flow Control** | Yes, includes flow control mechanisms. | No |
| **Congestion Control** | Yes, manages network congestion. | No |
| **Data Segmentation** | Breaks data into smaller packets and reassembles them at the destination. | Breaks data into packets but does not handle reassembly. |
| **Header Size** | Larger, 20-60 bytes | Smaller, typically 20 bytes |
| **Reliability** | Provides reliable data transfer | Does not guarantee delivery, reliability, or order. |
| **Transmission Acknowledgment** | Yes, acknowledges receipt of data packets. | No |

### 

### **How Does the TCP/IP Model Work?**

Whenever we want to send something over the internet using the TCP/IP Model, the TCP/IP Model divides the data into packets at the sender’s end and the same packets have to be recombined at the receiver’s end to form the same data, and this thing happens to maintain the accuracy of the data. TCP/IP model divides the data into a 4-layer procedure, where the data first go into this layer in one order and again in reverse order to get organized in the same way at the receiver’s end.

The diagrammatic comparison of the TCP/IP and OSI model is as follows:

<img src="TCPIP and OSI.png"> 
*TCP/IP and OSI*

#### **1\. Network Access Layer**

It is a group of applications requiring network communications. This layer is responsible for generating the data and requesting connections. It acts on behalf of the sender and the Network Access layer on the behalf of the receiver. During this article, we will be talking on the behalf of the receiver.

The packet’s network protocol type, in this case, TCP/IP, is identified by network access layer. Error prevention and “framing” are also provided by this layer. [Point-to-Point Protocol (PPP)](https://www.geeksforgeeks.org/point-to-point-protocol-ppp-frame-format) framing and Ethernet IEEE 802.2 framing are two examples of data-link layer protocols.

#### **2\. Internet or Network Layer**

This layer parallels the functions of OSI’s Network layer. It defines the protocols which are responsible for the logical transmission of data over the entire network. The main protocols residing at this layer are as follows:

* IP:[IP](https://www.geeksforgeeks.org/what-is-an-ip-address) stands for Internet Protocol and it is responsible for delivering packets from the source host to the destination host by looking at the IP addresses in the packet headers. IP has 2 versions: IPv4 and IPv6. IPv4 is the one that most websites are using currently. But IPv6 is growing as the number of IPv4 addresses is limited in number when compared to the number of users.  
* ICMP:[ICMP](https://www.geeksforgeeks.org/difference-between-icmp-and-igmp) stands for Internet Control Message Protocol. It is encapsulated within IP datagrams and is responsible for providing hosts with information about network problems.  
* ARP:[ARP](https://www.geeksforgeeks.org/how-address-resolution-protocol-arp-works) stands for Address Resolution Protocol. Its job is to find the hardware address of a host from a known IP address. ARP has several types: Reverse ARP, Proxy ARP, Gratuitous ARP, and Inverse ARP.

The Internet Layer is a layer in the Internet Protocol (IP) suite, which is the set of protocols that define the Internet. The Internet Layer is responsible for routing packets of data from one device to another across a network. It does this by assigning each device a unique IP address, which is used to identify the device and determine the route that packets should take to reach it.

**Example:** Imagine that you are using a computer to send an email to a friend. When you click “send,” the email is broken down into smaller packets of data, which are then sent to the Internet Layer for routing. The Internet Layer assigns an IP address to each packet and uses routing tables to determine the best route for the packet to take to reach its destination. The packet is then forwarded to the next hop on its route until it reaches its destination. When all of the packets have been delivered, your friend’s computer can reassemble them into the original email message.

In this example, the Internet Layer plays a crucial role in delivering the email from your computer to your friend’s computer. It uses IP addresses and routing tables to determine the best route for the packets to take, and it ensures that the packets are delivered to the correct destination. Without the Internet Layer, it would not be possible to send data across the Internet.

#### **3\. Transport Layer**

The TCP/IP transport layer protocols exchange data receipt acknowledgments and retransmit missing packets to ensure that packets arrive in order and without error. End-to-end communication is referred to as such. Transmission Control Protocol (TCP) and User Datagram Protocol are transport layer protocols at this level (UDP).

* TCP: Applications can interact with one another using [TCP](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp) as though they were physically connected by a circuit. TCP transmits data in a way that resembles character-by-character transmission rather than separate packets. A starting point that establishes the connection, the whole transmission in byte order, and an ending point that closes the connection make up this transmission.  
* UDP: The datagram delivery service is provided by [UDP](https://www.geeksforgeeks.org/user-datagram-protocol-udp) , the other transport layer protocol. Connections between receiving and sending hosts are not verified by UDP. Applications that transport little amounts of data use UDP rather than TCP because it eliminates the processes of establishing and validating connections.

#### **4\. Application Layer**

This layer is analogous to the transport layer of the OSI model. It is responsible for end-to-end communication and error-free delivery of data. It shields the upper-layer applications from the complexities of data. The three main protocols present in this layer are:

* HTTP and HTTPS:[HTTP](https://www.geeksforgeeks.org/difference-between-http-and-https-2) stands for Hypertext transfer protocol. It is used by the World Wide Web to manage communications between web browsers and servers. HTTPS stands for HTTP-Secure. It is a combination of HTTP with SSL(Secure Socket Layer). It is efficient in cases where the browser needs to fill out forms, sign in, authenticate, and carry out bank transactions.  
* SSH:[SSH](https://www.geeksforgeeks.org/introduction-to-sshsecure-shell-keys) stands for Secure Shell. It is a terminal emulations software similar to Telnet. The reason SSH is preferred is because of its ability to maintain the encrypted connection. It sets up a secure session over a TCP/IP connection.  
* NTP:[NTP](https://www.geeksforgeeks.org/network-time-protocol-ntp) stands for Network Time Protocol. It is used to synchronize the clocks on our computer to one standard time source. It is very useful in situations like bank transactions. Assume the following situation without the presence of NTP. Suppose you carry out a transaction, where your computer reads the time at 2:30 PM while the server records it at 2:28 PM. The server can crash very badly if it’s out of sync.

The host-to-host layer is a layer in the OSI (Open Systems Interconnection) model that is responsible for providing communication between hosts (computers or other devices) on a network. It is also known as the transport layer.

Some common use cases for the host-to-host layer include:

* Reliable Data Transfer: The host-to-host layer ensures that data is transferred reliably between hosts by using techniques like error correction and flow control. For example, if a packet of data is lost during transmission, the host-to-host layer can request that the packet be retransmitted to ensure that all data is received correctly.  
* Segmentation and Reassembly: The host-to-host layer is responsible for breaking up large blocks of data into smaller segments that can be transmitted over the network, and then reassembling the data at the destination. This allows data to be transmitted more efficiently and helps to avoid overloading the network.  
* Multiplexing and Demultiplexing: The host-to-host layer is responsible for multiplexing data from multiple sources onto a single network connection, and then demultiplexing the data at the destination. This allows multiple devices to share the same network connection and helps to improve the utilization of the network.  
* End-to-End Communication: The host-to-host layer provides a connection-oriented service that allows hosts to communicate with each other end-to-end, without the need for intermediate devices to be involved in the communication.

**Example:** Consider a network with two hosts, A and B. Host A wants to send a file to host B. The host-to-host layer in host A will break the file into smaller segments, add error correction and flow control information, and then transmit the segments over the network to host B. The host-to-host layer in host B will receive the segments, check for errors, and reassemble the file. Once the file has been transferred successfully, the host-to-host layer in host B will acknowledge receipt of the file to host A.

In this example, the host-to-host layer is responsible for providing a reliable connection between host A and host B, breaking the file into smaller segments, and reassembling the segments at the destination. It is also responsible for multiplexing and demultiplexing the data and providing end-to-end communication between the two hosts.

#### **Why TCP/IP Model Does Not Have Physical Layer**

The physical layer is not covered by the TCP/IP model because the data link layer is considered the point at which the interface occurs between the TCP/IP stock and the underlying network hardware. Also, it is designed to be independent of the underlying physical media. This allows TCP/IP to be flexible and adaptable to different types of physical connections, such as Ethernet, Wi-Fi, fiber optics, or even older technologies like dial-up modems. The physical layer is typically handled by hardware components and standards specific to the physical medium being used, like Ethernet cables or radio waves for Wi-Fi.

#### **Other Common Internet Protocols**

TCP/IP Model covers many Internet Protocols. The main rule of these Internet Protocols is how the data is validated and sent over the Internet. Some Common Internet Protocols include:

* HTTP (Hypertext Transfer Protocol):[HTTP](https://www.geeksforgeeks.org/http-full-form) takes care of Web Browsers and Websites.  
* FTP (File Transfer Protocol):[FTP](https://www.geeksforgeeks.org/file-transfer-protocol-ftp-in-application-layer) takes care of how the file is to be sent over the Internet.  
* SMTP (Simple Mail Transfer Protocol):[SMTP](https://www.geeksforgeeks.org/simple-mail-transfer-protocol-smtp) is used to send and receive data.

#### 

#### **Difference between TCP/IP and OSI Model**

| TCP/IP | OSI |
| ----- | ----- |
| TCP refers to Transmission Control Protocol. | OSI refers to Open Systems Interconnection. |
| TCP/IP uses both the session and presentation layer in the application layer itself. | OSI uses different session and presentation layers. |
| TCP/IP follows connectionless a horizontal approach. | OSI follows a vertical approach. |
| The Transport layer in TCP/IP does not provide assurance delivery of packets. | In the OSI model, the transport layer provides assurance delivery of packets. |
| Protocols cannot be replaced easily in TCP/IP model. | While in the OSI model, Protocols are better covered and are easy to replace with the technology change. |
| TCP/IP model network layer only provides connectionless (IP) services. The transport layer (TCP) provides connections. | Connectionless and connection-oriented services are provided by the network layer in the OSI model. |

#### 

#### **Advantages of TCP/IP Model**

* Interoperability : The TCP/IP model allows different types of computers and networks to communicate with each other, promoting compatibility and cooperation among diverse systems.  
* Scalability : TCP/IP is highly scalable, making it suitable for both small and large networks, from local area networks (LANs) to wide area networks (WANs) like the internet.  
* Standardization : It is based on open standards and protocols, ensuring that different devices and software can work together without compatibility issues.  
* Flexibility : The model supports various routing protocols, data types, and communication methods, making it adaptable to different networking needs.  
* Reliability : TCP/IP includes error-checking and retransmission features that ensure reliable data transfer, even over long distances and through various network conditions.

#### **Disadvantages of TCP/IP Model**

* Complex Configuration : Setting up and managing a TCP/IP network can be complex, especially for large networks with many devices. This complexity can lead to configuration errors.  
* Security Concerns : TCP/IP was not originally designed with security in mind. While there are now many security protocols available (such as SSL/TLS), they have been added on top of the basic TCP/IP model, which can lead to vulnerabilities.  
* Inefficiency for Small Networks : For very small networks, the overhead and complexity of the TCP/IP model may be unnecessary and inefficient compared to simpler networking protocols.  
* Limited by Address Space : Although IPv6 addresses this issue, the older IPv4 system has a limited address space, which can lead to issues with address exhaustion in larger networks.  
* Data Overhead : TCP, the transport protocol, includes a significant amount of overhead to ensure reliable transmission. This can reduce efficiency, especially for small data packets or in networks where speed is crucial.

## OSI (Open Systems Interconnection) Model

The OSI (Open Systems Interconnection) Model is a set of rules that explains how different computer systems communicate over a network. OSI Model was developed by the International Organization for Standardization (ISO). The OSI Model consists of 7 layers and each layer has specific functions and responsibilities. This layered approach makes it easier for different devices and technologies to work together. OSI Model provides a clear structure for data transmission and managing network issues. The OSI Model is widely used as a reference to understand how network systems function.**![OSI-Model][image2]**

OSI Model

### Layers of the OSI Model

There are 7 layers in the OSI Model and each layer has its specific role in handling data. All the layers are mentioned below:

* [Physical Layer](https://www.geeksforgeeks.org/physical-layer-in-osi-model)  
* [Data Link Layer](https://www.geeksforgeeks.org/data-link-layer)  
* [Network Layer](https://www.geeksforgeeks.org/network-layer-in-osi-model/)  
* [Transport Layer](https://www.geeksforgeeks.org/transport-layer-in-osi-model/)  
* [Session Layer](https://www.geeksforgeeks.org/session-layer-in-osi-model)  
* [Presentation Layer](https://www.geeksforgeeks.org/presentation-layer-in-osi-model)  
* [Application Layer](https://www.geeksforgeeks.org/application-layer-in-osi-model)

#### Layer 1 – Physical Layer

The lowest layer of the OSI reference model is the Physical Layer. It is responsible for the actual physical connection between the devices. The physical layer contains information in the form of bits. Physical Layer is responsible for transmitting individual bits from one node to the next. When receiving data, this layer will get the signal received and convert it into 0s and 1s and send them to the Data Link layer, which will put the frame back together. Common physical layer devices are [Hub](https://www.geeksforgeeks.org/what-is-network-hub-and-how-it-works/), [Repeater](https://www.geeksforgeeks.org/repeaters-in-computer-network/), [Modem](https://www.geeksforgeeks.org/difference-between-modem-and-router/), and [Cables](https://www.geeksforgeeks.org/types-of-ethernet-cable/).

Functions of the Physical Layer

* Bit Synchronization: The physical layer provides the synchronization of the bits by providing a clock. This clock controls both sender and receiver thus providing synchronization at the bit level.  
* Bit Rate Control: The Physical layer also defines the transmission rate i.e. the number of bits sent per second.  
* Physical Topologies: Physical layer specifies how the different, devices/nodes are arranged in a network i.e. [bus topology](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-bus-topology/) , [star topology](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-star-topology/) , or [mesh topology](https://www.geeksforgeeks.org/advantage-and-disadvantage-of-mesh-topology/) .  
* Transmission Mode: Physical layer also defines how the data flows between the two connected devices. The various transmission modes possible are [Simplex, half-duplex and full-duplex](https://www.geeksforgeeks.org/difference-between-simplex-half-duplex-and-full-duplex-transmission-modes/) .

#### Layer 2 – Data Link Layer (DLL)

The data link layer is responsible for the node-to-node delivery of the message. The main function of this layer is to make sure data transfer is error-free from one node to another, over the physical layer. When a packet arrives in a network, it is the responsibility of the DLL to transmit it to the Host using its [MAC address](https://www.geeksforgeeks.org/mac-address-in-computer-network). Packet in the Data Link layer is referred to as Frame. [Switches and Bridges](https://www.geeksforgeeks.org/difference-between-switch-and-bridge/) are common Data Link Layer devices.

The Data Link Layer is divided into two sublayers:

* Logical Link Control (LLC)  
* Media Access Control (MAC)

The packet received from the Network layer is further divided into frames depending on the frame size of the [NIC(Network Interface Card)](https://www.geeksforgeeks.org/nic-full-form/). DLL also encapsulates Sender and Receiver’s MAC address in the header.

The Receiver’s MAC address is obtained by placing an [ARP(Address Resolution Protocol)](https://www.geeksforgeeks.org/how-address-resolution-protocol-arp-works) request onto the wire asking “Who has that IP address?” and the destination host will reply with its MAC address.

Functions of the Data Link Layer

* Framing: Framing is a function of the data link layer. It provides a way for a sender to transmit a set of bits that are meaningful to the receiver. This can be accomplished by attaching special bit patterns to the beginning and end of the frame.  
* Physical Addressing: After creating frames, the Data link layer adds physical addresses ( MAC addresses ) of the sender and/or receiver in the header of each frame.  
* Error Control: The data link layer provides the mechanism of error control in which it detects and retransmits damaged or lost frames.  
* Flow Control: The data rate must be constant on both sides else the data may get corrupted thus, flow control coordinates the amount of data that can be sent before receiving an acknowledgment.  
* Access Control: When a single communication channel is shared by multiple devices, the MAC sub-layer of the data link layer helps to determine which device has control over the channel at a given time.

#### Layer 3 – Network Layer

The network layer works for the transmission of data from one host to the other located in different networks. It also takes care of packet routing i.e. selection of the shortest path to transmit the packet, from the number of routes available. The sender and receiver’s [IP address](https://www.geeksforgeeks.org/what-is-an-ip-address) are placed in the header by the network layer. Segment in the Network layer is referred to as Packet. Network layer is implemented by networking devices such as [routers and switches](https://www.geeksforgeeks.org/difference-between-router-and-switch/).

Functions of the Network Layer

* Routing: The network layer protocols determine which route is suitable from source to destination. This function of the network layer is known as routing.  
* Logical Addressing: To identify each device inter-network uniquely, the network layer defines an addressing scheme. The sender and receiver’s IP addresses are placed in the header by the network layer. Such an address distinguishes each device uniquely and universally.

#### Layer 4 – Transport Layer

The transport layer provides services to the application layer and takes services from the network layer. The data in the transport layer is referred to as Segments. It is responsible for the end-to-end delivery of the complete message. The transport layer also provides the acknowledgment of the successful data transmission and re-transmits the data if an error is found. Protocols used in Transport Layer are [TCP](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp/), [UDP](https://www.geeksforgeeks.org/user-datagram-protocol-udp/)  [NetBIOS](https://www.geeksforgeeks.org/what-is-netbios-enumeration/), [PPTP](https://www.geeksforgeeks.org/pptp-full-form/).

At the sender’s side, the transport layer receives the formatted data from the upper layers, performs Segmentation, and also implements Flow and error control to ensure proper data transmission. It also adds Source and Destination [port number](https://www.geeksforgeeks.org/what-is-ports-in-networking) in its header and forwards the segmented data to the Network Layer.

* Generally, this destination port number is configured, either by default or manually. For example, when a web application requests a web server, it typically uses port number 80, because this is the default port assigned to web applications. Many applications have default ports assigned.

At the Receiver’s side, Transport Layer reads the port number from its header and forwards the Data which it has received to the respective application. It also performs sequencing and reassembling of the segmented data.

Functions of the Transport Layer

* Segmentation and Reassembly: This layer accepts the message from the (session) layer, and breaks the message into smaller units. Each of the segments produced has a header associated with it. The transport layer at the destination station reassembles the message.  
* Service Point Addressing: To deliver the message to the correct process, the transport layer header includes a type of address called service point address or port address. Thus by specifying this address, the transport layer makes sure that the message is delivered to the correct process.

Services Provided by Transport Layer

* [Connection-Oriented Service](https://www.geeksforgeeks.org/connection-oriented-service)  
* [Connectionless Service](https://www.geeksforgeeks.org/connection-less-service)

#### Layer 5 – Session Layer

Session Layer in the OSI Model is responsible for the establishment of connections, management of connections, terminations of sessions between two devices. It also provides authentication and security. Protocols used in the Session Layer are NetBIOS, PPTP.

Functions of the Session Layer

* Session Establishment, Maintenance, and Termination: The layer allows the two processes to establish, use, and terminate a connection.  
* Synchronization: This layer allows a process to add checkpoints that are considered synchronization points in the data. These synchronization points help to identify the error so that the data is re-synchronized properly, and ends of the messages are not cut prematurely and data loss is avoided.  
* Dialog Controller: The session layer allows two systems to start communication with each other in half-duplex or full-duplex.

Example

Let us consider a scenario where a user wants to send a message through some Messenger application running in their browser. The “Messenger” here acts as the application layer which provides the user with an interface to create the data. This message or so-called Data is compressed, optionally encrypted (if the data is sensitive), and converted into bits (0’s and 1’s) so that it can be transmitted.

#### Layer 6 – Presentation Layer

The presentation layer is also called the Translation layer. The data from the application layer is extracted here and manipulated as per the required format to transmit over the network. Protocols used in the Presentation Layer are [JPEG](https://www.geeksforgeeks.org/difference-between-jpeg-and-png/), [MPEG](https://www.geeksforgeeks.org/mpeg-full-form/), [GIF](https://www.geeksforgeeks.org/what-is-a-gif-file/), [TLS/SSL](https://www.geeksforgeeks.org/difference-between-secure-socket-layer-ssl-and-transport-layer-security-tls/), etc.

Functions of the Presentation Layer

* Translation: For example, [ASCII to EBCDIC](https://www.geeksforgeeks.org/difference-between-ascii-and-ebcdic) .  
* Encryption/ Decryption: Data encryption translates the data into another form or code. The encrypted data is known as the ciphertext and the decrypted data is known as plain text. A key value is used for encrypting as well as decrypting data.  
* Compression: Reduces the number of bits that need to be transmitted on the network.

#### Layer 7 – Application Layer

At the very top of the OSI Reference Model stack of layers, we find the Application layer which is implemented by the network applications. These applications produce the data to be transferred over the network. This layer also serves as a window for the application services to access the network and for displaying the received information to the user. Protocols used in the Application layer are [SMTP](https://www.geeksforgeeks.org/simple-mail-transfer-protocol-smtp/), [FTP](https://www.geeksforgeeks.org/file-transfer-protocol-ftp-in-application-layer/), [DNS](https://www.geeksforgeeks.org/domain-name-system-dns-in-application-layer/), etc.

Functions of the Application Layer

The main functions of the application layer are given below.

* Network Virtual Terminal(NVT): It allows a user to log on to a remote host.  
* File Transfer Access and Management(FTAM): This application allows a user to access files in a remote host, retrieve files in a remote host, and manage or control files from a remote computer.  
* Mail Services: Provide email service.  
* Directory Services: This application provides distributed database sources and access for global information about various objects and services.

### How Data Flows in the OSI Model?

When we transfer information from one device to another, it travels through 7 layers of OSI model. First data travels down through 7 layers from the sender’s end and then climbs back 7 layers on the receiver’s end.

Data flows through the OSI model in a step-by-step process:

* Application Layer: Applications create the data.  
* Presentation Layer: Data is formatted and encrypted.  
* Session Layer: Connections are established and managed.  
* Transport Layer: Data is broken into segments for reliable delivery.  
* Network Layer : Segments are packaged into packets and routed.  
* Data Link Layer: Packets are framed and sent to the next device.  
* Physical Layer: Frames are converted into bits and transmitted physically.

Each layer adds specific information to ensure the data reaches its destination correctly, and these steps are reversed upon arrival.

<img src="OSI Model.png">

We can understand how data flows through OSI Model with the help of an example mentioned below.

Let us suppose, Person A sends an e-mail to his friend Person B.

Step 1: Person A interacts with e-mail application like Gmail, outlook, etc. Writes his email to send. (This happens at Application Layer).

Step 2: At Presentation Layer, Mail application prepares for data transmission like encrypting data and formatting it for transmission.

Step 3: At Session Layer, There is a connection established between the sender and receiver on the internet.

Step 4: At Transport Layer, Email data is broken into smaller segments. It adds sequence number and error-checking information to maintain the reliability of the information.

Step 5: At Network Layer, Addressing of packets is done in order to find the best route for transfer.

Step 6: At Data Link Layer, data packets are encapsulated into frames, then MAC address is added for local devices and then it checks for error using error detection.

Step 7: At Physical Layer, Frames are transmitted in the form of electrical/ optical signals over a physical network medium like ethernet cable or WiFi.

After the email reaches the receiver i.e. Person B, the process will reverse and decrypt the e-mail content. At last, the email will be shown on Person B email client.

### Protocols Used in the OSI Layers

| Layer | Working | Protocol Data Unit | Protocols |
| :---- | :---- | :---- | :---- |
| 1 – Physical Layer | Establishing Physical Connections between Devices. | Bits | [USB](https://www.geeksforgeeks.org/universal-serial-bus-usb/), [SONET/SDH](https://www.geeksforgeeks.org/difference-between-sonet-and-sdh/), etc. |
| 2 – Data Link Layer | Node to Node Delivery of Message. | Frames | [Ethernet](https://www.geeksforgeeks.org/what-is-ethernet/), PPP, etc. |
| 3 – Network Layer | Transmission of data from one host to another, located in different networks. | Packets | IP, [ICMP](https://www.geeksforgeeks.org/internet-control-message-protocol-icmp/), [IGMP](https://www.geeksforgeeks.org/what-is-igmpinternet-group-management-protocol/), [OSPF](https://www.geeksforgeeks.org/open-shortest-path-first-ospf-protocol-states/), etc. |
| 4 – Transport Layer | Take Service from Network Layer and provide it to the Application Layer. | Segments (for TCP) or Datagrams (for UDP) | [TCP](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp/), [UDP](https://www.geeksforgeeks.org/user-datagram-protocol-udp/), [SCTP,](https://www.geeksforgeeks.org/stream-control-transmission-protocol/) etc. |
| 5 – Session Layer | Establishes Connection, Maintenance, Ensures Authentication and Ensures security. | Data | [NetBIOS](https://www.geeksforgeeks.org/what-is-netbios-enumeration/), [RPC](https://www.geeksforgeeks.org/remote-procedure-call-rpc-in-operating-system/), [PPTP](https://www.geeksforgeeks.org/pptp-full-form/), etc. |
| 6 – Presentation Layer | Data from the application layer is extracted and manipulated in the required format for transmission. | Data | [TLS/SSL](https://www.geeksforgeeks.org/what-is-ssl-tls-handshake/), [MIME](https://www.geeksforgeeks.org/multipurpose-internet-mail-extension-mime-protocol/), JPEG, PNG, ASCII, etc. |
| 7 – Application Layer | Helps in identifying the client and synchronizing communication. | Data | [FTP](https://www.geeksforgeeks.org/file-transfer-protocol-ftp-in-application-layer/), [SMTP](https://www.geeksforgeeks.org/simple-mail-transfer-protocol-smtp/), [DNS](https://www.geeksforgeeks.org/domain-name-system-dns-in-application-layer/), [DHCP](https://www.geeksforgeeks.org/dynamic-host-configuration-protocol-dhcp/), etc. |

### 

### Why Does The OSI Model Matter?

The OSI Model matters because it provides the user a clear structure of “how the data moves in the network?”. As the OSI Model consists of 7 layers, each layer has its specific role, and due to which it helps in understanding, identifying and solving the complex network problems easily by focusing on one of the layers not the entire network.

As the modern Internet does not prefer the OSI Model, but still, the OSI Model is still very helpful for solving network problems. It helps people understanding network concepts very easily.

### Difference Between OSI and TCP/IP Model

| OSI Model | TCP/IP Model |
| :---- | :---- |
| OSI stands for Open Systems Interconnection. | TCP/IP stands for Transmission Control Protocol/Internet Protocol. |
| OSI model has 7 layers. | TCP/IP model consists of 4 layers. |
| Package delivery is guaranteed in OSI Model. | Package delivery is not guaranteed in the TCP/IP Model. |
| In the OSI model, Only layers 1,2 and 3 are necessary for data transmission. | All layers of the TCP/IP model are needed for data transmission. |
| Protocols at each layer is independent of the other layer. | Layers are integrated, some layers are required by other layers of TCP/IP model. |
| OSI Model is a conceptual framework, less used in practical applications. | Widely used in actual networks like Internet and Communication Systems. |

### Advantages of OSI Model

The OSI Model defines the communication of a computing system into 7 different layers. Its advantages include:

* It divides network communication into 7 layers which makes it easier to understand and troubleshoot.  
* It standardizes network communications, as each layer has fixed functions and protocols.  
* Diagnosing network problems is easier with the OSI model.  
* It is easier to improve with advancements as each layer can get updates separately.

### Disadvantages of OSI Model

* The OSI Model has seven layers, which can be complicated and hard to understand for beginners.  
* In real-life networking, most systems use a simpler model called the Internet protocol suite (TCP/IP), so the OSI Model is not always directly applicable.  
* Each layer in the OSI Model adds its own set of rules and operations, which can make the process more time-consuming and less efficient.  
* The OSI Model is more of a theoretical framework, meaning it’s great for understanding concepts but not always practical for implementation.

###### 

## Network Discovery Protocols

### What is IPv4?

IPv4, or Internet Protocol version 4, is the original addressing system of the Internet, introduced in 1983\. It uses a 32-bit address scheme, which theoretically allows for over 4 billion unique addresses (2^32). IPv4 addresses are typically displayed in decimal format, divided into four octets separated by dots. For example, 192.168.1.1 is a common IPv4 address you might find in a home network.

#### IPv4 Address Format

IPv4 Address Format is a 32-bit Address that comprises binary digits separated by a dot (.).

### **Characteristics of IPv4**

* 32-bit address length: Allows for approximately 4.3 billion unique addresses.  
* Dot-decimal notation: IP addresses are written in a format of four decimal numbers separated by dots, such as 192.168.1.1.  
* Packet structure: Includes a header and payload; the header contains information essential for routing and delivery.  
* Checksum fields: Uses checksums in the header for error-checking the header integrity.  
* Fragmentation: Allows packets to be fragmented at routers along the route if the packet size exceeds the maximum transmission unit (MTU).  
* Address Resolution Protocol (ARP): Used for mapping IP network addresses to the hardware addresses used by a data link protocol.  
* Manual and DHCP configuration: Supports both manual configuration of IP addresses and dynamic configuration through DHCP (Dynamic Host Configuration Protocol).  
* Limited address space: The main limitation which has led to the development of IPv6 to cater to more devices.  
* Network Address Translation (NAT): Used to allow multiple devices on a private network to share a single public IP address.  
* Security: Lacks inherent security features, requiring additional protocols such as IPSec for secure communications.

### Drawbacks of IPv4

* Limited Address Space : IPv4 has a limited number of addresses, which is not enough for the growing number of devices connecting to the internet.  
* Complex Configuration : IPv4 often requires manual configuration or DHCP to assign addresses, which can be time-consuming and prone to errors.  
* Less Efficient Routing : The IPv4 header is more complex, which can slow down data processing and routing.  
* Security Issues : IPv4 does not have built-in security features, making it more vulnerable to attacks unless extra security measures are added.  
* Limited Support for Quality of Service (QoS) : IPv4 has limited capabilities for prioritizing certain types of data, which can affect the performance of real-time applications like video streaming and VoIP.  
* Fragmentation : IPv4 allows routers to fragment packets, which can lead to inefficiencies and increased chances of data being lost or corrupted.  
* Broadcasting Overhead : IPv4 uses broadcasting to communicate with multiple devices on a network, which can create unnecessary network traffic and reduce performance.

<img src="IPv4 x IPv6.png">

### What is IPv6?

Another most common version of the Internet Protocol currently is IPv6. The well-known IPv6 protocol is being used and deployed more often, especially in mobile phone markets. IPv6 was designed by the Internet Engineering Task Force (IETF) in December 1998 with the purpose of superseding IPv4 due to the global exponentially growing internet of users.

IPv6 stands for Internet Protocol version 6\. IPv6 is the new version of Internet Protocol, which is way better than IPv4 in terms of complexity and efficiency. IPv6 is written as a group of 8 hexadecimal numbers separated by colon (:). It can be written as 128 bits of 0s and 1s.

### IPv6 Address Format

IPv6 Address Format is a 128-bit IP Address, which is written in a group of 8 hexadecimal numbers separated by colon (:).

To switch from IPv4 to IPv6, there are several strategies:

* Dual Stacking : Devices can use both IPv4 and IPv6 at the same time. This way, they can talk to networks and devices using either version.  
* Tunneling : This method allows IPv6 users to send data through an IPv4 network to reach other IPv6 users. Think of it as creating a “tunnel” for IPv6 traffic through the older IPv4 system.  
* Network Address Translation (NAT) : NAT helps devices using different versions of IP addresses (IPv4 and IPv6) to communicate with each other by translating the addresses so they understand each other.

Characteristics of IPv6

IPv6 uses 128-bit addresses, offering a much larger address space than IPv4’s 32-bit system.

IPv6 addresses use a combination of numbers and letters separated by colons, allowing for more unique addresses.

The IPv6 header has fewer fields, making it more efficient for routers to process.

IPv6 supports Unicast, Multicast, and Anycast, but no Broadcast, reducing network traffic.

IPv6 allows flexible subnetting (VLSM) to divide networks based on specific needs.

IPv6 uses Neighbor Discovery for MAC address resolution instead of ARP.

IPv6 uses advanced routing protocols like OSPFv3 and RIPng for better address handling.

IPv6 devices can self-assign IP addresses using SLAAC, or use DHCPv6 for more control.

IPv6 handles fragmentation at the sender side, not by routers, improving speed.

Difference Between IPv4 and IPv6

| IPv4 | IPv6 |
| ----- | ----- |
| IPv4 has a 32-bit address length | IPv6 has a 128-bit address length |
| It Supports Manual and [DHCP](https://www.geeksforgeeks.org/dynamic-host-configuration-protocol-dhcp/) address configuration | It supports Auto and renumbering address configuration |
| In IPv4 end to end, connection integrity is Unachievable | In IPv6 end-to-end, connection integrity is Achievable |
| It can generate 4.29×10 9 address space | The address space of IPv6 is quite large it can produce 3.4×10 38 address space |
| The Security feature is dependent on the application | IPSEC is an inbuilt security feature in the IPv6 protocol |
| Address representation of IPv4 is in decimal | Address representation of IPv6 is in hexadecimal |
| [Fragmentation](https://www.geeksforgeeks.org/what-is-fragmentation-in-operating-system/) performed by Sender and forwarding routers | In IPv6 fragmentation is performed only by the sender |
| In IPv4 Packet flow identification is not available | In IPv6 packet flow identification are Available and uses the flow label field in the header |
| In IPv4 checksum field is available | In IPv6 [checksum](https://www.geeksforgeeks.org/difference-between-checksum-and-crc/) field is not available |
| It has a broadcast Message Transmission Scheme | In IPv6 multicast and anycast message transmission scheme is available |
| In IPv4 Encryption and Authentication facility not provided | In IPv6 [Encryption](https://www.geeksforgeeks.org/what-is-data-encryption/) and Authentication are provided |
| IPv4 has a header of 20-60 bytes. | IPv6 has a header of 40 bytes fixed |
| IPv4 can be converted to IPv6 | Not all IPv6 can be converted to IPv4 |
| IPv4 consists of 4 fields which are separated by addresses dot (.) | IPv6 consists of 8 fields, which are separated by a colon (:) |
| IPv4’s  IP addresses are divided into five different classes. Class A , Class B, Class C, Class D , Class E. | IPv6 does not have any classes of the IP address. |
| IPv4 supports VLSM( [Variable Length subnet mask](https://www.geeksforgeeks.org/introduction-of-variable-length-subnet-mask-vlsm/) ). | IPv6 does not support VLSM. |
| Example of IPv4:  66.94.29.13 | Example of IPv6: 2001:0000:3238:DFE1:0063:0000:0000:FEFB |

### Benefits of IPv6 over IPv4

The recent Version of IP IPv6 has a greater advantage over IPv4. Here are some of the mentioned benefits:

* Larger Address Space: IPv6 has a greater address space than IPv4, which is required for expanding the IP Connected Devices. IPv6 has 128 bit IP Address rather and IPv4 has a 32-bit Address.  
* Improved Security: IPv6 has some improved security which is built in with it. IPv6 offers security like Data Authentication, Data Encryption, etc. Here, an Internet Connection is more Secure.  
* Simplified Header Format: As compared to IPv4, IPv6 has a simpler and more effective header Structure, which is more cost-effective and also increases the speed of Internet Connection.  
* Prioritize: IPv6 contains stronger and more reliable support for QoS features, which helps in increasing traffic over websites and increases audio and video quality on pages.  
* Improved Support for Mobile Devices: IPv6 has increased and better support for Mobile Devices. It helps in making quick connections over other Mobile Devices and in a safer way than IPv4.

### 

### Why IPv4 is Still in Use?

* Infrastructure Compatibility Many systems and devices are built for IPv4 and require significant updates to support IPv6, including routers, switches, and computers.  
* Cost of Transition – Switching to IPv6 can be expensive and complex, involving hardware updates, software upgrades, and training for personnel.  
* Lack of Immediate Need – Techniques like NAT (Network Address Translation) help extend the life of IPv4 by allowing multiple devices to share a single public IP address, reducing the urgency to switch to IPv6.  
* Coexistence Strategies – Technologies that allow IPv4 and IPv6 to run simultaneously make it easier for organizations to adopt IPv6 gradually while maintaining their existing IPv4 systems.  
* Slow Global Adoption – The adoption of IPv6 varies significantly around the world, which necessitates the continued support of IPv4 for global connectivity.  
* Lack of Visible Benefits – Many users and organizations don’t see immediate improvements with IPv6 if they don’t face an IP address shortage, reducing the incentive to upgrade.

## 

## Router, Switch and Hub

In computer network it is very important to understand the difference between devices like hubs, switches, and routers. These devices play an important role in how data is transferred across networks, affecting everything from speed and efficiency to security. In this article we will see basic differences between these devices, how they work within the OSI model, and where their use cases are applicable.

<img src="Router Hub Switch.png">

## **What is Hub?**

A [Hub](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-hub/) is just a connector that connects the wires coming from different sides. There is no signal processing or regeneration. It is an electronic device that operates only on physical layers of the [OSI model](https://www.geeksforgeeks.org/open-systems-interconnection-model-osi/).

It is also known as a repeater as it transmits signal to every port except the port from where signal is received. Also, hubs are not that intelligent in communication and processing information for 2nd and 3rd layer.

## 

## **What is Switch?**

Switch is a point to point communication device. It operates at the [data link layer](https://www.geeksforgeeks.org/data-link-layer/) of OSI model. It uses switching table to find out the correct destination.

Basically, it is a kind of [bridge](https://www.geeksforgeeks.org/what-is-bridge-in-computer-network-types-uses-functions-differences/) that provides better connections. It is a kind of device that set up and stop the connections according to the requirements  needed at that time. It comes up with many features such as flooding, filtering and frame transmission.

## **What is Router?**

Routers are the multiport devices and more sophisticated as compared to repeaters and bridges. It contains a routing table that enables it to make decision about the route i.e. to determine which of several possible paths between the source and destination is the best for a particular transmission.

It works on the network layer 3 and used in LANs, MANs and WANs. It stores [IP address](https://www.geeksforgeeks.org/what-is-an-ip-address/) and maintains address on its own.

## **Difference between Hub, Switch and Router**

| Hub | Switch | Router |
| ----- | ----- | ----- |
| Hub is a physical layer device i.e. layer 1\.  | Switch is a data link layer device i.e. layer 2\.  | Router is a network layer device i.e. layer 3\.   |
| A Hub works on the basis of broadcasting. | Switch works on the basis of MAC address. | A router works on the basis of IP address. |
| A Hub is a multiport repeater in which a signal introduced at the input of any port appears at the output of the all available ports. | A Switch is  a tele-communication  device which receives a message from any device connected to it and then transmits the message only to the device for which the message is intended. | A router reads the header of incoming packet and forward it to the port for which it is intended there by determines the route. It can also perform filtering and encapsulation. |
| Hub is not an intelligent device that may include amplifier on repeater. | A Switch is an intelligent device as it passes on the message to the selective device by inspecting the address. | A route is more sophisticated and intelligent device as it can read IP address and direct the packets to another network with specified IP address. Moreover routers can built address tables that helps in routing decisions. |
| At least single network is required to connect. | At least single network is required to connect. | Router needs at least two networks to connect.  |
| Hub is cheaper as compared to switch and router.  | Switch is an expensive device than hub. | Router is a relatively much more expensive device than hub and switch. |
| Speed of original hub 10Mbps and modern internet hub is 100Mbps. | maximum speed is 10Mbps to 100Mbps. | maximum speed for wireless is 1-10 Mbps and maximum speed for wired connections is 100 Mbps. |
| Hubs are used in LANs. | Switch is used in LANs. | Routers are used in LANs, MANs and WANs. |

## 

## Network Architectures, Mapping and Target Identification

### Network Architectures

Common Architectures:

* Hub-and-Spoke: A central hub (often a router) connects to multiple spoke devices (clients or other smaller networks). Simple but can become a single point of failure.  
* Mesh: Every device is connected to every other device. Highly redundant but complex to manage.  
* Star: Similar to Hub-and-Spoke, but with a more centralized control device.  
* Bus: All devices are connected to a single shared communication line.  
* Ring: Devices are connected in a closed loop.  
* Cloud Architectures: Understand cloud models (IaaS, PaaS, SaaS) and their security implications.  
* Virtualization: How virtualization technologies (e.g., VMware, VirtualBox) impact network architecture and security.

### Network Mapping and Discovery

Network Mapping is the process of identifying and documenting all devices and their connections within a network. This includes:

* Discovering devices: Identifying all active devices on the network, such as computers, servers, printers, and network devices (routers, switches).  
* Mapping connections: Determining how these devices are interconnected, including physical and logical connections.  
* Identifying services: Determining the services running on each device (e.g., web servers, databases, email servers).  
* Gathering information: Collecting information about the operating systems, software versions, and security configurations of each device.

Network Discovery Techniques:

* Passive:  
  * Monitoring network traffic: Analyzing network traffic to identify devices and their communication patterns. Tools like Wireshark can be used for this.  
  * Analyzing log files: Examining system and network logs for information about devices on the network.  
* Active:  
  * Ping sweeps: Sending ICMP echo requests (ping) to a range of IP addresses to determine which hosts are reachable.  
  * Port scanning: Scanning ports on target devices to identify open services. Nmap is a powerful tool for this.  
  * Service fingerprinting: Identifying the version and type of service running on a specific port.

Tools for Network Mapping and Discovery

* Nmap (Network Mapper): A versatile open-source tool for network discovery, port scanning, and service version detection.  
* Wireshark: A powerful network protocol analyzer for capturing and analyzing network traffic.  
* Zenmap: The graphical user interface for Nmap, providing a more user-friendly interface.  
* Nessus: A commercial vulnerability scanner that also includes network discovery capabilities.  
* OpenVAS: An open-source vulnerability assessment scanner with network discovery features.

Importance of Network Mapping and Discovery

* Security assessments: Identifying vulnerabilities and potential attack vectors.  
* Network planning and design: Understanding the current network topology to make informed decisions about network upgrades and expansions.  
* Troubleshooting network problems: Isolating and diagnosing network issues.  
* Compliance: Meeting regulatory and compliance requirements that require network inventories.

Ethical Considerations:

* Obtain proper authorization: Always obtain proper authorization before conducting network scans on any network that you do not own or have explicit permission to scan.  
* Minimize disruption: Avoid excessive scanning that could impact network performance.  
* Respect privacy: Be mindful of privacy concerns and avoid scanning devices that you are not authorized to scan.

By understanding network mapping and discovery techniques and utilizing the appropriate tools, you can gain valuable insights into your network environment, identify potential vulnerabilities, and improve the overall security posture of your organization.

### Target Identification

* Prioritization: Identifying critical assets (e.g., servers, databases, network devices) and prioritizing them for security measures.  
* Vulnerability Assessment: Identifying and assessing vulnerabilities in systems and applications on the network.  
* Threat Modeling: Identifying potential threats and their impact on the organization.  
* Intelligence Gathering: Collecting information about potential threats and adversaries.

Target Identification in cybersecurity is the crucial initial step in understanding and mitigating potential threats. It involves identifying the specific systems, applications, and data within an organization that are most valuable to attackers and therefore require the strongest security measures.

#### Key Aspects of Target Identification:

Asset Inventory:

* Identify all critical assets: This includes servers, workstations, databases, network devices, applications, data stores, and any other valuable resource.  
* Categorize assets: Classify assets based on their criticality (e.g., high, medium, low) and sensitivity (e.g., confidential, sensitive, public).  
* Document asset information: Gather detailed information about each asset, such as its location, owner, purpose, and associated vulnerabilities.

Threat Modeling:

* Identify potential threats: Analyze the organization's environment and identify potential threats, such as malware attacks, phishing scams, data breaches, and denial-of-service attacks.  
* Assess vulnerabilities: Evaluate the potential impact of these threats on critical assets.  
* Determine attack vectors: Identify the possible entry points for attackers, such as internet-facing systems, employee devices, and third-party vendors.

Prioritization:

* Focus on high-value targets: Prioritize the protection of assets that are most critical to the organization's operations and that contain the most sensitive data.  
* Allocate resources effectively: Focus security resources on the most critical assets to maximize the return on investment.

Continuous Monitoring:

* Regularly review and update asset inventories: As the organization evolves, new assets are added and existing assets may change.  
* Monitor for new threats: Stay informed about the latest threats and vulnerabilities to adjust security measures accordingly.

Tools and Techniques

* Vulnerability scanning tools: Tools like Nmap, Nessus, and OpenVAS can be used to identify vulnerabilities in systems and applications.  
* Threat intelligence feeds: Subscribe to threat intelligence feeds from reputable sources to stay informed about the latest threats and vulnerabilities.  
* Risk assessments: Conduct regular risk assessments to identify and prioritize potential threats and vulnerabilities.  
* Security information and event management (SIEM) systems: Collect and analyze security logs to identify suspicious activity.

#### Importance of Target Identification:

* Improved security posture: By focusing on the most critical assets, organizations can allocate their security resources more effectively.  
* Reduced risk of breaches: Proactive identification and mitigation of vulnerabilities can significantly reduce the risk of successful cyberattacks.  
* Compliance with regulations: Many regulations (e.g., GDPR, HIPAA) require organizations to identify and protect sensitive data.  
* Enhanced decision-making: Informed decisions about security investments can be made based on a clear understanding of the organization's most critical assets.

By effectively identifying and prioritizing targets, organizations can significantly improve their overall security posture and better protect themselves against cyber threats.

## 

## 

## Network Scanning & Fingerprinting

### **Network Scanning** 

Técnica fundamental em segurança da informação que envolve a varredura de uma rede para identificar dispositivos, serviços e vulnerabilidades. É como fazer um censo da sua rede para entender o que está conectado e como está configurado.  
Por que realizar network scanning?

* Inventário de ativos: Identificar todos os dispositivos conectados à rede, incluindo servidores, workstations, dispositivos IoT, etc.  
* Descoberta de serviços: Identificar os serviços em execução em cada dispositivo (HTTP, SSH, FTP, etc.).  
* Identificação de vulnerabilidades: Encontrar vulnerabilidades conhecidas nos sistemas e serviços.  
* Mapeamento da topologia da rede: Visualizar a estrutura da rede e as conexões entre os dispositivos.

Ferramentas Comuns para Network Scanning:

* Nmap: Uma das ferramentas mais populares e versáteis para varredura de redes. Permite realizar diversas tarefas, como varredura de portas, detecção de sistemas operacionais e identificação de serviços.  
* Nessus: Uma ferramenta comercial focada em vulnerabilidades, mas que também possui recursos de descoberta de redes.  
* OpenVAS: Uma alternativa open-source ao Nessus, oferecendo funcionalidades similares.  
* Wireshark: Embora seja um analisador de pacotes, o Wireshark pode ser usado para descobrir dispositivos na rede capturando o tráfego.

Tipos de Varredura:

* Varredura de hosts: Identifica dispositivos ativos na rede.  
* Varredura de portas: Identifica as portas abertas em cada dispositivo, indicando os serviços em execução.  
* Varredura de vulnerabilidades: Identifica vulnerabilidades conhecidas nos sistemas e serviços.  
* Varredura de serviços: Identifica o tipo de serviço em execução em cada porta aberta.

Considerações Importantes:

* Permissões: Certifique-se de ter as permissões necessárias para realizar varreduras em uma rede.  
* Alcance: Defina o escopo da varredura para evitar impactar negativamente a rede.  
* Velocidade: Varreduras completas podem levar tempo, especialmente em redes grandes.  
* Legalidade: Verifique as leis e regulamentos locais antes de realizar varreduras em redes que não sejam suas.

Exemplo de comando Nmap:

Bash  
nmap \-sS \-sV 192.168.1.0/24

* \-sS: Realiza uma varredura TCP SYN (half-open) para identificar hosts ativos e portas abertas.  
* \-sV: Tenta identificar a versão dos serviços em execução nas portas abertas.  
* 192.168.1.0/24: Especifica a faixa de IP a ser varrida.

Por que a Network Scanning é importante para a segurança?

* Identificação de vulnerabilidades: Permite identificar sistemas vulneráveis antes que sejam explorados por atacantes.  
* Mapeamento da infraestrutura: Auxilia na criação de inventários de ativos e na visualização da topologia da rede.  
* Detecção de dispositivos não autorizados: Permite identificar dispositivos não autorizados conectados à rede.  
* Monitoramento contínuo: A realização de varreduras regulares pode ajudar a detectar mudanças não autorizadas na rede.

Em resumo, a network scanning é uma ferramenta essencial para qualquer profissional de segurança da informação. Ao entender os princípios e as ferramentas de network scanning, você estará melhor preparado para proteger sua organização contra ameaças cibernéticas.

### Fingerprinting

What exactly is cybersecurity fingerprinting? It’s a cutting-edge technique that detects cyber threats by analyzing the unique digital ‘fingerprints’ of systems and network traffic. Without the fluff, this article will guide you through the core of cybersecurity fingerprinting and its significance in the modern cybersecurity landscape.

Key Takeaways

* Cybersecurity fingerprinting, a key step in cybersecurity [information gathering](https://www.recordedfuture.com/threat-intelligence-101/intelligence-sources-collection/information-gathering), is a critical process for gathering detailed profiles of systems to identify potential threats, weaknesses, and the presence of malicious activities by analyzing network traffic, and probing targeted systems.  
* Different fingerprinting techniques, including active, passive, and hybrid, are utilized for identifying systems, software, and vulnerabilities, with each having unique approaches such as traffic analysis, system probing, and encrypted protocol handling to [enhance threat detection](https://www.recordedfuture.com/products/threat-intelligence) and network security.  
* The effectiveness of cybersecurity fingerprinting is amplified by a variety of tools and methods, including Nmap, p0f, and XProbe2, while it must be used under strict legal and ethical guidelines to prevent unauthorized fingerprinting and protect user privacy.

Demystifying Cybersecurity Fingerprinting

Cybersecurity fingerprinting can be compared to a digital Sherlock Holmes, as it meticulously collects clues to build a comprehensive profile of a system. The process involves scanning network traffic, launching specifically crafted packets, or analyzing outgoing packets from a target system.

However, it's worth noting that the network layer of the Open Systems Interconnection (OSI) model, as [highlighted](https://louis.uah.edu/cgi/viewcontent.cgi?article=1011&context=cyber-summit) by Adrian Ordorica and Dale R. Thompson from the Science and Computer Engineering Department at the University of Arkansas, does not inherently provide explicit information about the operating system of the network device generating traffic. Despite this limitation, cybersecurity professionals leverage fingerprinting techniques to gather crucial details, including operating system, protocols, and other system attributes. These insights are invaluable for accurately identifying and mitigating potential threats.

The key objective of cybersecurity fingerprinting mirrors that of a seasoned detective \- exposing potential weaknesses and countering advanced cyber threats. Just as a detective constructs a profile of a potential suspect, cybersecurity fingerprinting creates server profiles capable of recognizing distinct identifiers and characteristics of potential cyber threats, making it an essential tool for network security experts.

## 

## Testing Network Services

Many businesses will test their network to make sure it’s functioning properly and providing the right level of service for users. It therefore serves to guarantee working efficiency for internal processes and, where products and services are sold online, ensure a smooth customer experience. However, network testing is also important for business cyber security.  

In this blog, we’ll be delving into network security testing – what it means, why it matters, and the types of tests available today. 

###  **Why test a network?**

A network can pose a significant security risk to businesses due to the amount of software and devices it interacts with. Vulnerabilities arise when a network has weaknesses that can be exploited by cyber attackers. These weak points can be found in a variety of places, such as servers, firewalls, routers, modems, physical connection ports, operating systems, and software updates. Any one of these could serve as a way for criminals to gain access to the network and cause damage to the business’s systems. 

Networks can face a range of threats. As such, it’s not possible to recognise a network cyber attack by only monitoring a certain piece of the infrastructure or a particular type of data. On top of this, networks often face multiple attacks employing different techniques at the same time. Potential network security threats include: 

* Malware   
* Viruses   
* Botnets   
* Keyloggers   
* Ransomware   
* SQL injection attacks   
* Man-in-the-middle attacks   
* Phishing attacks and social engineering   
* Physical surveillance and sabotage 

Network security is important as it protects personal data of employees and customers, as well as other information that can used to damage the business. Securing this data is vital, as it is often essential to everyday operations. In addition, if user data becomes compromised it can damage the integrity of the organisation, possibly leading to customers going to other providers. 

###  **The process of a network test** 

The purpose of the test is to simulate how an attacker would go about gaining access to the network. In this, it aims to reveal any potential weaknesses that could be used as entry points. The information provided by the network test can then be used to devise targeted reinforcement plans. This will strengthen security in specific areas and implement targeted measures. 

When you run a test on your network with the help cyber security professionals, it will typically follow these steps: 

1. Planning  

We’ll first discuss with you what methods will be used in the test and how the results will be measured. Both these aspects will vary depending on the scope and goals of the test. At this stage, an ethical hacker will also identify the critical areas of your network that could contain vulnerabilities.  

      2\. Probing 

The ethical hacker then starts using testing solutions to examine how the network responds to cyber attacks. For example, if there is an endpoint threat detection system the tester will become aware of it. This allows them to gain an understanding of how various parts of the network communicate, along with the nature of the response. The result is the ethical hacker now knows to operate in the way that’s most likely to bypass any automated defences. 

      3\. Mock attacks 

Following the appropriate network research, an ethical hacker will simulate a range of attacks. This can include any of the types of network threats already discussed. If a network vulnerability is found, they will then take actions to exploit the weakness such as attempting to disrupt traffic, increase privileges, and stealing data.  

The tester can then measure the vulnerability by how much theoretical damage they would be able to inflict. Time can be a factor here too. After gaining access, testers can try and make changes that lock internal administrators out of the network.  

      4\. Analysing the results  

The test concludes once the tester is confident there isn’t any more information that can be gleaned about the network’s security. Following this, a report will be created to show their findings to the business owner. Testing reports contain insights into the vulnerabilities found, details of recommended remedial action, and the likely timeframe for solving any network problems.

###  **Different types of network testing** 

All network tests will follow the general structure outlined above. However, there are variations based on the approach of the tester and the aspects focused on. These are: 

* White box testing – testers have an intimate knowledge of the network and how its infrastructure has been constructed. They’re therefore primarily concerned with examining code implementation, control flow, data flow, error handling, and other technical features.   
* Black box testing – the tester lacks any prior knowledge of the organisation’s network or systems. As such, this method is the most effective at simulating the effects of an actual cyber attack.    
* Grey box testing – unsurprisingly, this combines elements of both white and black box testing. The ethical hacker is given a select amount of information about the network. Grey box tests are ideal for assessing the risk privileged users pose to the business.

### **Best network security practices** 

Oftentimes, a network test report will recommend the following practices to ensure you security is kept up to standard. The first is to keep your software and operating systems up-to-date. Many network vulnerabilities are solved through system updates. Therefore, it’s possible that old versions of pieces of software will still contain weaknesses. For the same reason, care should be taken to ensure old disused devices are not still connected to your network. 

Next, keep a record of the business’s most valuable assets and how they can be accessed. This should be an indicator of where your security should be targeted, as a breach in these areas brings a more significant risk. These records should then be used to create a response plan in the event that your network is breached. 

Finally, your cyber security policies and procedures should be reviewed regularly. The threat landscape is constantly shifting, so it’s important your resources are being allocated efficiently.

## Cryptography

Cryptography is a technique of securing communication by converting plain text into ciphertext. It involves various algorithms and protocols to ensure data confidentiality, integrity, authentication, and non-repudiation. In this article, we will discuss cryptography and its types.

### What is Cryptography?

Cryptography is a technique of securing information and communications through the use of codes so that only those persons for whom the information is intended can understand and process it. Thus preventing unauthorized access to information. The prefix “crypt” means “hidden” and the suffix “graphy” means “writing”. In Cryptography, the techniques that are used to protect information are obtained from mathematical concepts and a set of rule-based calculations known as algorithms to convert messages in ways that make it hard to decode them. These algorithms are used for cryptographic key generation, digital signing, and verification to protect data privacy, web browsing on the internet and to protect confidential transactions such as credit card and debit card transactions.

<img src="Cryptography.png">

### Features Of Cryptography

* Confidentiality: Information can only be accessed by the person for whom it is intended and no other person except him can access it.  
* Integrity: Information cannot be modified in storage or transition between sender and intended receiver without any addition to information being detected.  
* Non-repudiation: The creator/sender of information cannot deny his intention to send information at a later stage.  
* Authentication: The identities of the sender and receiver are confirmed. As well destination/origin of the information is confirmed.  
* Interoperability: Cryptography allows for secure communication between different systems and platforms.  
* Adaptability: Cryptography continuously evolves to stay ahead of security threats and technological advancements.

### Types Of Cryptography

#### 1\. Symmetric Key Cryptography

It is an encryption system where the sender and receiver of a message use a single common key to encrypt and decrypt messages. [Symmetric Key cryptography](https://www.geeksforgeeks.org/what-is-a-symmetric-encryption/) is faster and simpler but the problem is that the sender and receiver have to somehow exchange keys securely. The most popular symmetric key cryptography systems are [Data Encryption Systems (DES)](https://www.geeksforgeeks.org/data-encryption-standard-des-set-1/) and [Advanced Encryption Systems (AES)](https://www.geeksforgeeks.org/advanced-encryption-standard-aes/) .

<img src="Symmetric Key Cryptography.png">  
Symmetric Key Cryptography

#### 2\. Hash Functions

There is no usage of any key in this algorithm. A hash value with a fixed length is calculated as per the plain text which makes it impossible for the contents of plain text to be recovered. Many operating systems use hash functions to encrypt passwords.

#### 3\. Asymmetric Key Cryptography

In [Asymmetric Key Cryptography,](https://www.geeksforgeeks.org/asymmetric-key-cryptography/) a pair of keys is used to encrypt and decrypt information. A sender’s public key is used for encryption and a receiver’s private key is used for decryption. Public keys and Private keys are different. Even if the public key is known by everyone the intended receiver can only decode it because he alone knows his private key. The most popular asymmetric key cryptography algorithm is the RSA algorithm.

## <img src="Asymmetric Key Cryptography.png">

Asymmetric Key Cryptography

#### Applications of Cryptography

* Computer passwords: Cryptography is widely utilized in computer security, particularly when creating and maintaining passwords. When a user logs in, their password is hashed and compared to the hash that was previously stored. Passwords are hashed and encrypted before being stored. In this technique, the passwords are encrypted so that even if a hacker gains access to the password database, they cannot read the passwords.  
* Digital Currencies: To protect transactions and prevent fraud, digital currencies like Bitcoin also use cryptography. Complex algorithms and cryptographic keys are used to safeguard transactions, making it nearly hard to tamper with or forge the transactions.  
* Secure web browsing: Online browsing security is provided by the use of cryptography, which shields users from eavesdropping and man-in-the-middle assaults. Public key cryptography is used by the [Secure Sockets Layer (SSL)](https://www.geeksforgeeks.org/secure-socket-layer-ssl/) and [Transport Layer Security (TLS)](https://www.geeksforgeeks.org/transport-layer-security-tls/) protocols to encrypt data sent between the web server and the client, establishing a secure channel for communication.  
* Electronic Signatures: Electronic signatures serve as the digital equivalent of a handwritten signature and are used to sign documents. Digital signatures are created using cryptography and can be validated using public key cryptography. In many nations, electronic signatures are enforceable by law, and their use is expanding quickly.  
* Authentication: Cryptography is used for authentication in many different situations, such as when accessing a bank account, logging into a computer, or using a secure network. Cryptographic methods are employed by authentication protocols to confirm the user’s identity and confirm that they have the required access rights to the resource.  
* Cryptocurrencies: Cryptography is heavily used by cryptocurrencies like Bitcoin and Ethereum to protect transactions, thwart fraud, and maintain the network’s integrity. Complex algorithms and cryptographic keys are used to safeguard transactions, making it nearly hard to tamper with or forge the transactions.  
* End-to-end Internet Encryption: End-to-end encryption is used to protect two-way communications like video conversations, instant messages, and email. Even if the message is encrypted, it assures that only the intended receivers can read the message.  End-to-end encryption is widely used in communication apps like WhatsApp and Signal, and it provides a high level of security and privacy for users.

## Types of Cryptography Algorithm

* Advanced Encryption Standard (AES): [AES (Advanced Encryption Standard)](https://www.geeksforgeeks.org/advanced-encryption-standard-aes/) is a popular encryption algorithm which uses the same key for encryption and decryption It is a symmetric block cipher algorithm with block size of 128 bits, 192 bits or 256 bits. AES algorithm is widely regarded as the replacement of DES (Data encryption standard) algorithm.  
* Data Encryption Standard (DES): [DES (Data encryption standard)](https://www.geeksforgeeks.org/data-encryption-standard-des-set-1/) is an older encryption algorithm that is used to convert 64-bit plaintext data into 48-bit encrypted ciphertext. It uses symmetric keys (which means same key for encryption and decryption). It is kind of old by today’s standard but can be used as a basic building block for learning newer encryption algorithms.  
* RSA: [RSA](https://www.geeksforgeeks.org/rsa-algorithm-cryptography/) is an basic asymmetric cryptographic algorithm which uses two different keys for encryption. The RSA algorithm works on a block cipher concept that converts plain text into cipher text and vice versa.  
* Secure Hash Algorithm (SHA): [SHA](https://www.geeksforgeeks.org/sha-1-hash-in-java/) is used to generate unique fixed-length digital fingerprints of input data known as hashes. SHA variations such as SHA-2 and SHA-3 are commonly used to ensure data integrity and authenticity. The tiniest change in input data drastically modifies the hash output, indicating a loss of integrity. Hashing is the process of storing key value pairs with the help of a hash function into a hash table.

## Advantages of Cryptography

* Access Control: Cryptography can be used for access control to ensure that only parties with the proper permissions have access to a resource. Only those with the correct decryption key can access the resource thanks to encryption.  
* Secure Communication: For secure online communication, cryptography is crucial. It offers secure mechanisms for transmitting private information like passwords, bank account numbers, and other sensitive data over the Internet.  
* Protection against attacks: Cryptography aids in the defense against various types of assaults, including replay and [man-in-the-middle attacks](https://www.geeksforgeeks.org/how-to-prevent-man-in-the-middle-attack/) . It offers strategies for spotting and stopping these assaults.  
* Compliance with legal requirements: Cryptography can assist firms in meeting a variety of legal requirements, including data protection and privacy legislation.

### Active Directory Security Basics

Active Directory (AD) is a critical component of many Windows-based organizations, providing centralized management of users, computers, and other network resources. Securing AD is paramount to protect your entire network. Here's a breakdown of key security concepts:

#### 1\. Account Security

* Strong Passwords:  
  * Complexity: Enforce strong password policies (length, character types, complexity).  
  * History: Prevent the reuse of old passwords.  
  * Account Lockout: Lock accounts after multiple failed login attempts to prevent brute-force attacks.  
* Privileged Accounts:  
  * Least Privilege: Grant only the necessary permissions to each user account.  
  * Service Accounts: Use dedicated service accounts for applications and services instead of domain user accounts.  
  * Multi-Factor Authentication (MFA): Implement MFA for all privileged accounts (e.g., domain administrators).  
* Account Disablement: Promptly disable inactive or compromised accounts.

#### 2\. Group Policy

* Centralized Control: Utilize Group Policy to enforce security settings across the domain, such as password policies, software restrictions, and security configurations.  
* Security Templates: Leverage pre-built security templates for common configurations and compliance requirements.  
* Regular Auditing: Regularly review and audit Group Policy settings to ensure they are effective and up-to-date.

#### 3\. Domain Controller Security

* Physical Security: Ensure physical security of domain controllers by placing them in secure locations, using physical locks, and implementing proper environmental controls.  
* Virtualization: Consider virtualizing domain controllers for enhanced security and disaster recovery.  
* Regular Patching and Updates: Keep domain controllers up-to-date with the latest security patches and updates from Microsoft.

#### 4\. Active Directory Auditing

* Event Logs: Regularly review security event logs for suspicious activity, such as failed login attempts, account modifications, and security policy violations.  
* Security Information and Event Management (SIEM) systems: Utilize SIEM tools to collect, analyze, and correlate security events from various sources, including Active Directory.

#### 5\. Other Security Measures

* Regular backups: Perform regular backups of the Active Directory database to ensure data recovery in case of a disaster.  
* Security audits: Conduct regular security audits to identify and address potential vulnerabilities.  
* Implement security best practices: Follow best practices for network security, such as using firewalls, intrusion detection systems (IDS), and antivirus software.

### Key Security Principles:

* Principle of Least Privilege: Grant users only the minimum necessary privileges to perform their job duties.  
* Defense in Depth: Implement multiple layers of security controls to provide a robust defense.  
* Regular Monitoring and Auditing: Continuously monitor and audit your Active Directory environment for suspicious activity.  
* Stay Informed: Keep up-to-date with the latest threats and vulnerabilities related to Active Directory.

By implementing these security measures, you can significantly enhance the security of your Active Directory environment and protect your organization's valuable data and systems.

## Linux and Windows Security Basics

Compared to other [operating systems](https://phoenixnap.com/glossary/operating-system) like Windows and macOS, Linux has fewer vulnerabilities. However, Linux is not immune to all [types of cyberattacks](https://phoenixnap.com/blog/types-of-cyber-attacks). The most common vulnerabilities in Linux systems are privilege escalation, memory corruption, and information disclosure. Cyber attackers use these vulnerabilities to gain unauthorized access to a Linux system and steal data.

Reports from sources such as [The National Vulnerability Database (NVD)](https://nvd.nist.gov/) and [Crowdstrike](https://www.crowdstrike.com/) show an increase in Linux vulnerabilities each year. For example, there were 1,958 Linux vulnerabilities reported in 2020\. In 2021, there was a 35% rise in malware targeting Linux systems compared to 2020\. And in 2022, the number of new Linux malwares reached nearly 1.7 million, a 650% increase from the previous year.

Significant [Linux ransomwares](https://phoenixnap.com/blog/linux-ransomware) and vulnerabilities over the years are:

1. Shellshock (2014 \- active). A vulnerability in the [Bash shell](https://phoenixnap.com/kb/linux-shells) that lets attackers run random code by running a specially prepared environment variable.  
2. Ghost (2015 \- resolved). A vulnerability in the [GNU](https://phoenixnap.com/glossary/what-is-gnu) C Library (glibc) that allowed attackers to run arbitrary code by sending a specific [DNS response](https://phoenixnap.com/kb/what-is-domain-name-system-works).  
3. Dirty COW (2016 \- resolved). This vulnerability affected the [Linux kernel](https://phoenixnap.com/glossary/what-is-a-kernel) and gave attackers [root access](https://phoenixnap.com/glossary/what-is-root-access) by exploiting a race condition in the [memory management](https://phoenixnap.com/kb/memory-management) system.  
4. BlueBorne (2017 \- resolved). This vulnerability affected Bluetooth implementations on Windows, Linux, and Android. BlueBorne would run the code remotely, allowing the attackers to steal sensitive information.  
5. SACK Panic (2019 \- resolved). A vulnerability in the [TCP](https://phoenixnap.com/glossary/transmission-control-protocol-tcp) stack of the Linux kernel caused a denial of service by sending TCP Selective Acknowledgment (SACK) packets.  
6. Ghostcat (2020 \- active). This vulnerability affects the [Apache Tomcat](https://phoenixnap.com/kb/install-tomcat-ubuntu) web server and allows attackers to gain unauthorized access to sensitive information.  
7. SUDO (2021 \- active). This vulnerability affected the [sudo](https://phoenixnap.com/kb/linux-sudo-command) command-line utility and allowed attackers to execute commands as root without a password.  
8. Text4Shell or ACT4Shell (2022 \- active). A critical [remote code execution (RCE)](https://phoenixnap.com/glossary/remote-code-execution-rce) vulnerability that abuses the Apache Commons Text interpolation functionality in [string substitution](https://phoenixnap.com/kb/sed-replace).  
9. Linux Kernel Vulnerability (2023 \- active). A security issue was found in the Linux kernel's NVMe functionality, specifically in the nvmet\_setup\_auth() function, which can result in a pre-auth [denial of service (DoS) attack](https://phoenixnap.com/blog/prevent-ddos-attacks) on a remote machine.  
10. Signal Desktop Vulnerability (2023 \- active). A vulnerability in the Signal Desktop software allows attackers access to sensitive message attachments.

### Linux Security Tips and Best Practices

As the use of Linux systems continues to grow, it's crucial to implement adequate security measures to protect a system from potential threats. The sections below offer a range of practical tips and best practices for enhancing the security of a Linux system.

#### 1\. Use Strong Passwords

**(Basic security mechanism)**

Use [strong passwords](https://phoenixnap.com/blog/strong-great-password-ideas) and change them regularly as a basic step to securing your Linux system. Strong passwords prevent unauthorized access to the system and reduce the risk of identity theft, [data loss](https://phoenixnap.com/blog/data-loss-prevention-best-practices), and other security incidents.

A strong password is at least 12 characters long and includes a mixture of upper and lowercase letters, numbers, and special characters. That makes [brute-force attacks](https://phoenixnap.com/blog/brute-force-attack) extremely more difficult.

Regularly changing passwords also improves security. The process reduces the risk of password reuse and exposure, giving a potential attacker a limited time frame to exploit the password if it becomes compromised.

#### 2\. Verify All Accounts Have Passwords

(Basic security mechanism)

Accounts with no passwords allow anyone to log into the system without any authentication, compromising the system's data security and confidentiality. Therefore, make sure to verify that no accounts have empty passwords.

Run the [awk command](https://phoenixnap.com/kb/awk-command-in-linux) with the following options:

sudo awk \-F: '($2 \== "") {print $1}' /etc/shadow

![sudo awk -f terminal output][image15]

This command searches the /etc/shadow file, which contains information about user account passwords, and prints the names of any accounts with an empty password field.

Since accounts with empty passwords are a serious security risk, consider the following actions:

* Set a password. For instance, assign a new password to a user with the [passwd command](https://phoenixnap.com/kb/passwd-command-in-linux):  
  * sudo passwd \[username\]  
* Disable the account. Prevent users from logging into the account by disabling it entirely. To lock a Linux user account, run the [usermod command](https://phoenixnap.com/kb/usermod-linux) with the \-L option (which prints no output):  
  * sudo usermod \-L \[username\]

Alternatively, use the passwd command with the \-l option:

sudo passwd \-l \[username\]

![passwd -l to lock a user.][image16]

The user is now unable to log in using their password.

Delete the account. Remove unnecessary accounts with:

sudo userdel \[username\]

The command shows no output if executed correctly.

#### 3\. Set Up Password Aging

(Basic security mechanism)

Password aging is the practice of requiring users to change passwords regularly. Regular password changes reduce the chance of users reusing previous passwords. The practice also prevents password cracking attacks, which often succeed because of weak passwords that are not changed frequently.

There are several ways to set up password aging for a Linux user:

* Use the chage command. For instance, enable a password aging process that ensures the password expires in 60 days, the system warns the user 10 days before the expiration date, and the user has to change the password within 14 days. To do so, run:

sudo change \-M 60 \-m 10 \-W 14 \[username\]

* Alternatively, use the passwd command:

sudo passwd \-x 60 \[username\]  
![sudo passwd -x 60 NewUser terminal output][image17]

The command sets the password expiration date for NewUser at 60 days.

#### 

#### 4\. Restrict the Use of Previous Passwords on Linux

(Basic security mechanism)

Prevent all users from reusing old passwords. Old passwords might have been compromised and attackers might be actively trying to take advantage of that to hack into the system.

To prevent password reuse attacks:

1. Enforce password history with PAM, a unique Linux library with the pam\_unix module feature. This feature keeps track of users' passwords and disallows the reuse of any previously used ones.   
2. Enforce rules for password complexity, including minimum length and a mix of characters, with pam\_cracklib. Requiring users to create complex passwords makes it more difficult for attackers to guess or crack passwords.  
3. Regularly check system logs for any suspicious activity, such as repeated failed login attempts, to detect potential password-related security threats.  
4. Store hashed passwords using a strong cryptographic hash function such as Message-Digest Algorithm (MDA), Secure Hash Algorithm (SHA), or [NTLM](https://phoenixnap.com/glossary/ntlm).  
5. Use an [enterprise password manager](https://phoenixnap.com/blog/enterprise-password-management-solutions) to generate and store unique, secure passwords for each account.

#### 

#### 5\. Ensure OpenSSH Server Security

(Intermediate security mechanism)

OpenSSH is a widely used and secure implementation of [SSH](https://phoenixnap.com/kb/what-is-ssh) for Linux systems. It provides [encryption for data in transit](https://phoenixnap.com/blog/data-in-transit-encryption), robust [authentication](https://phoenixnap.com/glossary/what-is-authentication) methods, and a secure way to administer systems and transfer files remotely. To ensure the security of OpenSSH, minimize the tool's vulnerabilities.

Secure the OpenSSH server by following these tips:

* Use [non-standard SSH ports](https://phoenixnap.com/kb/change-ssh-port).  
* Limit user access and disable root login.  
* Use [SSH key](https://phoenixnap.com/kb/generate-setup-ssh-key-ubuntu) pairs for authentication.  
* Disable root login and password-based logins on the server.  
* Keep OpenSSH updated regularly.  
* Use strong authentication methods.  
* Limit the number of authentication attempts.  
* Disable unused protocols and features.  
* Implement a firewall.  
* Monitor logs regularly.

#### 6\. Disable Root Login via SSH

(Intermediate security mechanism)

Linux machines have external root access enabled by default. That leaves an open [SSH security](https://phoenixnap.com/kb/linux-ssh-security) vulnerability which hackers can exploit with brute-force attacks. Disabling server SSH root login prevents unauthorized individuals from gaining control over the system. An active root account allows attackers to obtain or guess the root password with full administrative privileges.

To disable root login in Linux, change the SSH configuration file:

1\. Open the file in a [text editor of your choice](https://phoenixnap.com/kb/best-linux-text-editors-for-coding). To access the config file in Vim, run:

sudo vim /etc/ssh/sshd\_config

2\. Find the PermitRootLogin line.

![locate the PermitRootLogin line i Vim][image18]

3\. Change the value from yes to no.

![Change PermitRootLogin to no][image19]

4\. [Save the changes and exit the file](https://phoenixnap.com/kb/how-to-vim-save-quit-exit).

5\. Restart the SSH service to apply the changes.

Note: Disabling root login can prevent legitimate users from performing administrative tasks on the system. Ensure that authorized users have the necessary permissions by creating a regular user account with administrative privileges and [add the user to the sudo group](https://phoenixnap.com/kb/how-to-create-sudo-user-on-ubuntu).

#### 7\. Limit the Use of sudo

(Intermediate security mechanism)

Unrestricted use of sudo leads to privilege escalation and allows attackers to gain control of the system. Limiting sudo permissions reduces the number of potential [attack vectors](https://phoenixnap.com/blog/attack-vector-vs-attack-surface). If an attacker gains access to a user account, they will only be able to run a limited set of [Linux commands](https://phoenixnap.com/kb/linux-commands), making it harder to cause damage.

However, limiting the use of sudo requires [modifying the sudoers file](https://phoenixnap.com/kb/how-to-create-sudo-user-on-ubuntu). While it's possible to do it correctly, making mistakes could result in security vulnerabilities.

#### 8\. Ensure Only Root Has User ID Set to 0

(Basic security mechanism)

The root account controls the system, including installing and removing software, modifying system configuration files, and accessing all user data. Root is also the only account with a User ID (UID) set to 0\.

A non-root account with a UID of 0 is effectively equivalent to the root account, creating a significant security risk.

To ensure that no non-root accounts have a UID of 0, run:

sudo awk \-F: '($3 \== "0") {print}

![sudo awk -F terminal output][image20]

The command prints root as the only user with a UID of 0\. If the output shows any non-root accounts with a UID of 0, delete them or change the UID to a non-zero value with usermod. 

#### 9\. Lock User Accounts After Login Failures

(Intermediate security mechanism)

Locking user accounts after several login failures makes it harder for an attacker to guess or brute-force a password.

The system works by setting the maximum number of login attempts per user. Once that number is reached, the account locks for a specified period. Another option is to install a system for unlocking the account, either automatically after a set time has elapsed or manually by an administrator.

To achieve this, use different [Identity Access Management (IAM) systems](https://phoenixnap.com/glossary/identity-and-access-management). These tools block incoming traffic from IP addresses with failed login attempts, helping mitigate brute-force attacks or monitor log files and ban IP addresses with repeated failed login attempts.

Writing custom scripts to parse log files, keep track of failed login attempts, and lock user accounts is also an option.

#### 10\. Enable Two-Factor Authentication

(Intermediate security mechanism)

Two-factor authentication (2FA) is a security measure that adds an extra layer of protection. By requiring a secondary verification method, such as a one-time code sent to the user's mobile device, 2FA makes it much more difficult for unauthorized users to access sensitive information or systems.

There are various ways to enable 2FA on Linux systems. Common methods include using [TOTP (Time-based One-Time Password)](https://phoenixnap.com/glossary/totp-time-based-one-time-password) apps like Google Authenticator or a hardware token like a Yubikey. Certain Linux systems have built-in 2FA capabilities, such as PAM (Pluggable Authentication Modules), that work with various authentication methods.

#### 11\. Keep Linux Up to Date

(Basic security mechanism)

Hackers exploit outdated software. To maintain Linux server security, keep the Linux kernel and software up to date. Different [Linux distributions](https://phoenixnap.com/glossary/what-is-a-linux-distribution) offer various package managers to update packages manually, with [yum and apt](https://phoenixnap.com/kb/yum-vs-apt) being the most popular.

Another method includes automatic updates. Automatic updates are installed in the background without requiring any action from the user, making updating software easier and more convenient. However, these types of updates are also risky.

Important: Automatic updates cause compatibility issues with other packages or result in unexpected changes to the system. In general, it is not recommended to run automatic updates on production servers.

#### 12\. Use Linux Security Extensions

(Intermediate security mechanism)

Linux security extensions are tools and features that provide additional security measures to a Linux operating system. These extensions help protect against misconfigured or compromised programs, defend against potential attacks, and enforce limitations on networks and programs.

Popular Linux security extensions are:

* [SELinux (Security-Enhanced Linux)](https://phoenixnap.com/kb/selinux) is a security feature integrated into the Linux kernel that uses [Mandatory Access Control](https://phoenixnap.com/glossary/mandatory-access-control-mac) (MAC) system. It allows administrators to control access to system resources by only allowing authorized users and processes. This ensures that only trusted parties access and modify important system information. SELinux is more common in RHEL and CentOS systems.  
* [AppArmor](https://phoenixnap.com/kb/apparmor-vs-selinux) is a mandatory access control system that allows administrators to specify the permissions required by applications to access system resources. It's been a default feature of Ubuntu since version 7.10.   
* TCP Wrappers are a security tool that provides basic access control for network services by checking the client's IP address against a list of allowed or denied addresses. The request is granted if the client's IP address is found in the allow list, and if it is found in the deny list, the request is rejected.  
* PAM (Pluggable Authentication Modules) provides a flexible and centralized system for managing authentication on a Linux system. PAM allows administrators to configure the authentication system and choose the best methods for their security needs. Moreover, PAM makes it easier to enforce strong authentication policies and ensures that all applications and services use the same authentication system.

#### 13\. Configure Linux Firewall 

(Basic security mechanism)

A [firewall](https://phoenixnap.com/glossary/what-is-a-firewall) on a Linux system acts as the first line of defense against malicious network traffic. The firewall defines rules that govern what traffic is allowed and what is blocked. Sysadmins apply those rules to control incoming and outgoing network traffic, blocking unauthorized access and only allowing necessary services.

The default Linux firewall is [iptables](https://phoenixnap.com/kb/iptables-tutorial-linux-firewall), a popular tool that provides packet filtering and manipulation capabilities for IPv4 and IPv6 network traffic. It filters network traffic, [forwards traffic](https://phoenixnap.com/kb/iptables-port-forwarding) between network interfaces, and implements [network address translation (NAT)](https://phoenixnap.com/glossary/nat-network-address-translation).

#### 14\. Reduce Network Service Vulnerabilities by Isolation

(Intermediate security mechanism)

To enhance the security of network services, run each service on a separate server or virtual instance. The process limits the number of vulnerable services, making managing [security patches](https://phoenixnap.com/glossary/what-is-security-patch), updates, and configurations easier.

There are several ways to implement this method:

* Use virtualization tools like [VirtualBox](https://phoenixnap.com/kb/install-virtualbox-on-ubuntu) to create individual [virtual machines (VMs)](https://phoenixnap.com/glossary/what-is-a-virtual-machine) for each network service. Or, create isolated containers with [Docker](https://phoenixnap.com/kb/what-is-docker) or [Kubernetes](https://phoenixnap.com/kb/what-is-kubernetes) for each network service.  
* Use firewall rules to control incoming and outgoing network traffic, only allowing the necessary services.  
* [Segment the network](https://phoenixnap.com/blog/network-segmentation-security) into separate subnets to isolate different services and minimize the risk of attacks.  
* Regularly [monitor network traffic](https://phoenixnap.com/glossary/what-is-network-monitoring) and logs for suspicious activity and take appropriate action.

#### 15\. Secure Web Servers

(Intermediate security mechanism)

Web servers like [Apache](https://phoenixnap.com/glossary/what-is-apache) and [Nginx](https://phoenixnap.com/kb/how-to-install-nginx-on-ubuntu-20-04) are prime cyberattack targets as they often deal with sensitive data. Securing these servers is critical to prevent unauthorized access and [data breaches](https://phoenixnap.com/blog/what-is-a-data-breach).

Top tips for securing Apache and Nginx web servers are:

* Regularly update the software to apply the latest security patches and fixes.  
* Configure access control to limit access to sensitive information and prevent unauthorized access.  
* Disable unneeded modules and features to reduce the attack surface and minimize security vulnerabilities.  
* Use strong passwords to secure the administration interface and prevent unauthorized access.  
* Use SSL certificates to encrypt data transmitted over the network and secure sensitive information such as passwords and financial data.  
* Regularly monitor logs for suspicious activity or unauthorized access attempts.  
* Run web servers as a non-root user with limited privileges to prevent unauthorized access and data breaches.

#### 16\. Detect Listening Network Ports

(Intermediate security mechanism)

In a Linux system, [ports](https://phoenixnap.com/glossary/what-is-a-port) are used when a program, such as a server or a network service, opens a [network socket](https://phoenixnap.com/glossary/what-is-a-socket) to receive incoming client connections. Open ports listen for those incoming connections.

However, listening ports are a weakness attackers exploit. A vulnerable listening port provides access to the system or sensitive information.

By detecting all listening ports, sysadmins identify and secure them by applying updates, limiting access, or disabling unnecessary ones. Furthermore, identifying listening ports helps detect rogue or unauthorized applications that pose a security risk.

Identify listening ports in a Linux system with [netstat](https://phoenixnap.com/kb/netstat-command), [ss](https://phoenixnap.com/kb/ss-command), or [lsof](https://phoenixnap.com/kb/lsof-command).

#### 17\. Disable Unwanted Linux Services

(Basic security mechanism)

Unneeded services in Linux are a security vulnerability and consume resources like memory and [CPU](https://phoenixnap.com/glossary/cpu-definition). To improve security and performance on a Linux operating system server, keep a minimal installation with only the necessary packages.

To manage system services, Linux uses [systemd](https://phoenixnap.com/kb/journalctl-systemd-logs) with the systemctl command.

1\. To check if a service is active, run:

sudo systemctl status \[service\_name\]

For instance, check the status for [snap](https://phoenixnap.com/kb/snap-packages) with:

sudo systemctl status snapd

![sudo systemctl status snapd terminal output][image21]

2\. To stop an active service, run:

sudo systemctl stop \[service\_name\]

To stop snap, execute:

sudo systemctl stop snapd

![sudo systemctl stop snapd terminal output][image22]

3\. To prevent the service from starting at boot, use:

sudo systemctl disable \[service\_name\]

For instance, apply this command on snap:

sudo systemctl disable snapd

![sudo systemctl disable snapd terminal output][image23]

When working with older systems that use System V or Upstart, run the [chkconfig](https://phoenixnap.com/kb/chkconfig) command to manage services.

It is also important to check dependencies before installing software and inspect auto-started dependencies to ensure they are needed.

#### 18\. Use Centralized Authentication Service

(Intermediate security mechanism)

A Centralized Authentication Service (CAS) is a [single sign-on](https://phoenixnap.com/glossary/single-sign-on-sso) protocol that allows web applications that may not be trusted to authenticate users through a centralized, trusted server. The CAS server handles all authentication, so the user's credentials are not revealed to the applications.

A centralized authentication service is crucial for Linux security as it allows sysadmins to enforce password policies and manage user accounts in a secure and scalable way. It makes monitoring and auditing authentication easier, reduces the risk of lost login credentials, and ensures consistent user data.

Common Linux Central Authentication Services are [Kerberos](https://phoenixnap.com/blog/kerberos-authentication), [Samba](https://phoenixnap.com/kb/ubuntu-samba), and Winbind.

#### 19\. Set Up an Intrusion Detection System

(Advanced security mechanism)

An [intrusion detection system](https://phoenixnap.com/blog/intrusion-detection-system) (IDS) monitors processes running on the server. It detects potential threats such as denial-of service attacks, port scans, or attempts to crack into computers by monitoring network traffic.

Popular IDS options include:

* Sophos. A cloud-based management platform that integrates multiple security products and uses machine learning to trigger automatic threat responses. It also uses advanced techniques like sandboxing and SSL inspection to identify and isolate compromised systems.  
* SolarWinds \- NetFlow Traffic Analyzer. [A network monitoring utility](https://phoenixnap.com/kb/linux-network-bandwidth-monitor-traffic) that inspects network traffic using intrusion detection. It is configured with over 700 event correlation rules, allowing it to automatically detect suspicious activities and implement remediation actions.  
* [Fail2Ban](https://phoenixnap.com/kb/fail2ban). A lightweight host-based intrusion detection software system designed to protect against brute force attacks. It monitors server logs and detects any suspicious activity, providing an extra layer of security for the server.

#### 20\. Manage Linux File Permissions

(Basic security mechanism)

Managing [file permissions in Linux](https://phoenixnap.com/kb/linux-file-permissions) protects sensitive files and directories from unauthorized access. Limiting access to files and directories reduces the risk of data breaches, theft of sensitive information, and unauthorized modifications to the system.

Several tools manage file permissions in Linux, including the chmod command, which allows sysadmins to change [file permission recursively](https://phoenixnap.com/kb/chmod-recursive) and configure multiple files and subdirectories using a single command.

The [ls command](https://phoenixnap.com/kb/linux-ls-commands) lists file permissions, and the [chown command](https://phoenixnap.com/kb/linux-chown-command-with-examples) changes file ownership.

#### 21\. Use Access Control Lists (ACLs)

(Intermediate security mechanism)

Compared to traditional file permissions systems, [ACLs](https://phoenixnap.com/kb/acl-network) are a more advanced way of controlling access to files and directories in Linux systems. The traditional system only allows three basic permissions (read, write, and execute) to be assigned to three permission classes (file owner, group owner, and others). However, ACLs allow for more fine-grained control.

Sysadmins use ACLs to define different permissions for specific users and groups on a per-file or per-directory basis. This allows for implementing more complex access control policies, like granting certain users read-only access to sensitive files or allowing certain groups write access to specific [directories](https://phoenixnap.com/glossary/what-is-a-directory).

#### 22\. Monitor Suspicious Server Logs 

(Intermediate security mechanism)

To improve Linux system security and [prevent brute force attacks](https://phoenixnap.com/kb/prevent-brute-force-attacks), analyze server logs with [log management](https://phoenixnap.com/glossary/log-management) applications such as Logwatch or logcheck. 

Both tools allow sysadmins to regularly monitor the logs for unusual activity and provide a summarized report.

Logwatch parses log files from services and applications running on the system and generates a daily report of error messages, security alerts, and system warnings. The command has numerous options and settings. For instance, to see a detailed report in the terminal, run:

sudo logwatch \--detail high

![sudo logwatch --detail high terminal output][image24]

Logcheck focuses on log files related to system security, such as authentication logs and firewall logs. Logcheck summarizes the events in these logs and sends a daily report via email to the sysadmin.

The logcheck command also has a lot of options. To output everything, run:

sudo \-u logcheck logcheck \-o \-t

![sudo -u logcheck logcheck -o -t terminal output][image25]

Note: Neither Logwatch nor logcheck come preinstalled in Linux. Use the apt command to install them.

#### 23\. Restrict World-Writable Files

(Intermediate security mechanism)

World-writable files, directories, and devices on a Linux server pose a significant security risk. Any user is able to modify these files, potentially leading to unauthorized changes, data tampering, or malicious actions.

Locate and remove these files following these steps:

1\. Identify world-writable files or directories with the [find command](https://phoenixnap.com/kb/guide-linux-find-command):

sudo find /. \-xdev \-type d \\( \-perm \-0002 \-a \! \-perm \-1000 \\) \-print

![Identify world-writable files or directories with the find command][image26]

2\. In this case, the output prints one directory. If there are more, Investigate each one.

3\. Use chmod to update the permissions or remove unnecessary files or directories. For instance, set file permissions to 600 to ensure the owner has full read and write access to the directory, while no other user has access.

sudo chmod 600 \[directory\]

The command has no output.

#### 24\. Configure Logging and Auditing Processes

(Intermediate security mechanism)

Logging and auditing provide valuable information about the system and network events, aiding administrators in detecting and addressing malicious threats. To increase security:

1. Centralize log data from different sources to a single [repository](https://phoenixnap.com/glossary/what-is-a-repository) making it easier to search, analyze, and store logs.  
2. Rotate logs regularly to keep only a limited number of logs and reduce the storage space.  
3. Enforce a retention policy to save space and prevent log data from becoming too large to handle.  
4. Use SELinux or another auditing framework to track and record specific events, such as access to sensitive files, user logins, and system changes.  
5. Implement real-time [syslog server](https://phoenixnap.com/kb/syslog-server) monitoring tools, such as log analyzers or security information and [event management (SIEM) systems](https://phoenixnap.com/blog/siem-security-information-event-management-tools), to get alerts for potential security incidents.  
6. Restrict privileges to log files, allowing access to only necessary users to prevent unauthorized modification or tampering of log data.  
7. Encrypt log data before any network transmission s to maintain data confidentiality. 

#### 25\. Disable Unwanted SUID and SGID Binaries

(Intermediate security mechanism)

SUID and SGID are file permissions allowing a file to be executed with owner or group privileges. Still, they pose security risks if not adequately secured. The main risk is a privilege escalation attack. Privilege escalation attacks occur when an attacker gains access to a system with limited privileges and then uses a vulnerability to elevate their privileges to the binary owner or group level.

To disable these files:

1\. Identify SUID and SGID files with the find command.

sudo find / \-perm \+u+s \-type f

![sudo find / -perm +u+s -type f terminal output][image27]

2\. To locate all SGID files, execute:

sudo find / \-perm \+g+s \-type f

![sudo find / -perm +g+s -type f terminal output][image28]

Note: An alternative way to locate all SUID and SGID files is the find / \-perm \+6000 \-type f command. However, the command prints an error on some systems that do not support the \+6000 option, in which case the command returns an error message.

3\. Evaluate the output and decide what to keep or discard.

4\. Use the chmod command to change the permissions or remove unnecessary files.

5\. Regularly monitor the SUID and SGID files to ensure the permissions have not changed.

#### 26\. Encrypt Data Communication

(Intermediate security mechanism)

Linux provides various methods for encrypting data communication:

1. [Secure File Transfer Protocol (SFTP)](https://phoenixnap.com/kb/what-is-sftp) transfers files between systems securely. With SFTP, users choose the level of authentication for transferring files. To use SFTP, users must install an SFTP server on one system and an SFTP client on the other. However, SFTP only protects files during transfer, and the data is no longer encrypted after reaching the server.  
2. [Secure Socket Layer (SSL)](https://phoenixnap.com/kb/tls-vs-ssl) guards information passed between two systems via the internet and is used in server-client and server-server communication. SSL encrypts the transmitted data, making it difficult for an attacker to intercept or alter the information. To use SSL, users must obtain an SSL certificate and install it on both the client and the server systems.  
3. Apache SSL (Secure Server Layer) is a component for Apache web server that provides secure communication between a client and a server. It implements the SSL (Secure Socket Layer) or TLS (Transport Layer Security) protocols, which provide encryption and authentication for secure communication.  
4. [SSL/TLS:](https://phoenixnap.com/kb/tls-vs-ssl) SSL (Secure Sockets Layer) and its successor, TLS (Transport Layer Security), are widely used protocols for encrypting data communication over the internet. TLS (Transport Layer Security) is more secure and provides better encryption. 

#### 27\. Use Encryption Tools to Protect Sensitive Data

(Intermediate security mechanism)

Encryption allows users to protect confidential information from unauthorized access, even during a data breach. Encrypting files before transmitting them with SFTP, for instance, ensures additional protection. The following tools allow users to encrypt files before transmitting:

* LUKS (Linux Unified Key Setup). The most widely used method for encrypting partitions on Linux systems. LUKS allows users to encrypt the entire partition file system, protecting all the data.  
* Node.js. An open-source [JavaScript (JS)](https://phoenixnap.com/glossary/what-is-javascript) runtime environment that works as an encryption tool. Node.js has an extensive cryptography library, such as crypto, node-forge, or sodium-native, which provide functions for encrypting and decrypting data, generating encryption keys, and managing cryptographic operations.  
* CryFS. A cryptographic file system that encrypts users' files and stores the encrypted data on cloud storage services like Dropbox or Google Drive. CryFS works by transparently encrypting a user's files before they are uploaded to the cloud and then decrypting them when accessed. The files remain encrypted and protected from unauthorized access, even when stored in the cloud.  
* SecureDoc for Linux. A security solution for Linux endpoints, providing enterprise-class full disk encryption. It separates encryption into two components, encryption, and [key management](https://phoenixnap.com/blog/encryption-key-management-best-practices). SecureDoc for Linux adopts a [Zero Trust](https://phoenixnap.com/blog/zero-trust-security) approach to security but allows live disk conversion during encryption.

#### 28\. Use a VPN

(Basic security mechanism)

[Virtual Private Networks](https://phoenixnap.com/glossary/vpn-definition) (VPNs) are crucial in ensuring communication security over public networks on Linux systems. A VPN uses encryption and authentication to protect sensitive information from interception or tampering during transmission.

Unlike open networks, private and virtual private networks limit access to only authorized users. Private networks use a unique [IP address](https://phoenixnap.com/glossary/what-is-an-ip-address) to set up isolated communication channels between servers within the same IP range, allowing data exchange without exposure to a public space.

With a VPN, data is encrypted at the source, transmitted over a public network, and decrypted at the destination. This helps to secure communication between the two points, even over an insecure network. VPNs are useful when connecting to a remote server as if directly connected to a private network.

In Linux, a popular VPN is OpenVPN. This open-source VPN solution provides robust security and high performance. It supports various encryption protocols, including SSL/TLS and PPTP. OpenVPN is known for its ease of use, flexible configuration options, and compatibility with most Linux distributions.

#### 29\. Harden the Linux Kernel

(Intermediate security mechanism)

The Linux kernel plays a crucial role in the overall security of a system. The /etc/sysctl.conf file [configures kernel parameters](https://www.cyberciti.biz/faq/linux-kernel-etcsysctl-conf-security-hardening/) at runtime and hardens the Linux kernel. Hardening the Linux kernel prevents attacks and limits the damage from potential attacks.

To harden the Linux kernel, configure settings in the /etc/sysctl.conf file:

* Disable IP forwarding to reduce the risk of the system being used as a pivot point in an attack.  
* Enable source address verification to prevent IP spoofing attacks by verifying that incoming packets have a valid source IP address.  
* Disable ICMP redirect acceptance to stop attackers from altering the system's routing tables through ICMP redirect messages.  
* Disable IP source routing to prevent IP packet routing manipulation.  
* Increase the connection tracking table size to limit the memory used by the connection tracking system, reducing the risk of a denial-of-service attack.

#### 30\. Separate Disk Partitions for Improved Linux Security

(Intermediate security mechanism)

Separating disk partitions in a Linux system improves its security by isolating sensitive data and system files from each other. This allows for implementing different security measures for each partition, making it more difficult for an attacker to compromise the entire system.

Critical filesystems to be mounted on separate partitions include: 

* /usr  
* /home  
* /tmp   
* /var  
* /var/tmp

[Creating separate partitions](https://phoenixnap.com/kb/linux-create-partition) for Apache and FTP server roots is also recommended. Mounting the partitions with different file permissions and mount options, such as the noexec option, prevents the execution of programs in a partition. This helps prevent attackers from exploiting vulnerabilities in the software installed on the system and limits the potential damage.

Having separate partitions also makes it easier to back up, restore, upgrade, or replace individual parts without affecting the rest of the system. In the event of a security breach, this allows for restoring the compromised partition without affecting the entire system.

#### 31\. Enable Disk Quotas

(Basic security mechanism)

Enabling disk quotas in Linux prevents the system from running out of disk space. Limited disk space makes it easier for attackers to exploit vulnerabilities or cause a denial-of-service (DoS) attack by filling up the disk. Setting disk quotas limits the disk space that each user or group takes, preventing attackers from using up all available disk space.

#### 32\. Manage "Noowner" Files

(Basic security mechanism)

Managing "noowner" files is essential for Linux security because files not owned by a valid user or group are easily manipulated by an attacker and used to hide malicious files or activities.

To manage "noowner" files:

1. Use the find command to locate files that do not belong to a valid user or group.  
2. Investigate each reported file to determine its purpose and usage.  
3. Assign the file to an appropriate user and group, or remove it if unnecessary.

#### 33\. Backup Linux System

(Intermediate security mechanism)

Backing up a Linux system is crucial for security, allowing users to recover from a system compromise or data loss. A data backup copy helps restore the system to a secure state in case of a security breach, hardware failure, or another disaster.

To back up a Linux system, use traditional UNIX backup programs such as dump and restore or a cloud-based service such as AWS. Ensure the backups' security by encrypting and storing them in a secure location, such as an external storage device or a [NAS server](https://phoenixnap.com/glossary/nas-network-attached-storage).

Most Linux distributions have built-in backup tools. To start with backup on Linux, search for backup tools in the system menu.

#### 34\. Install an Antivirus Program

(Basic security mechanism)

An antivirus program protects the system from viruses, trojans, and spyware. Antivirus scans the system, detects potential threats, and prevents damage.

Several antivirus options are available for Linux systems, including free and paid options. Popular free antivirus programs are ClamAV and AVG, and paid options include McAfee and Symantec. Also, regularly update and run the antivirus program to ensure that it provides the most up-to-date protection.

#### 35\. Prevent Ransomware Attacks

(Advanced security mechanism)

[Ransomware](https://phoenixnap.com/blog/what-is-ransomware) is malware that encrypts user files and demands payment for the decryption key. If a Linux system is infected with ransomware, the loss of important data, files, and sensitive information is possible.

[Preventing ransomware](https://phoenixnap.com/blog/how-to-prevent-ransomware) attacks requires a combination of security measures, such as:

* Setting up a firewall.  
* Setting up ad blockers.  
* Implementing strong passwords.  
* Keeping software up-to-date.  
* Using reliable antivirus software.  
* Running regular security tests.  
* Whitelisting applications.  
* Setting up a [sandbox](https://phoenixnap.com/glossary/what-is-sandbox).  
* Improving [email security.](https://phoenixnap.com/blog/email-security-best-practices)  
* Employing the zero-thrust policy.

#### 36\. Regularly Perform Vulnerability Assessments

(Advanced security mechanism)

Performing regular [vulnerability assessments](https://phoenixnap.com/blog/vulnerability-assessment) in Linux helps identify any potential security risks and weaknesses in the system.

The process enables sysadmins to proactively mitigate the risks and improve the system's overall security.

Several tools and techniques perform vulnerability assessments in Linux, including:

* Network scanning tools scan the network for open ports and services and identify potential vulnerabilities in the system.  
* [Penetration testing](https://phoenixnap.com/blog/penetration-testing) tools simulate an attack on the system to identify weaknesses an attacker could exploit.  
* Code review tools analyze the source code of applications and system components, looking for potential security vulnerabilities.  
* Vulnerability databases provide information about known vulnerabilities in specific software and operating systems, including patches and workarounds.

#### 37\. Invest in Disaster Recovery

(Advanced security mechanism)

A disaster recovery plan outlines the steps to be taken in case of a system failure, data loss, or security breach. A well-designed disaster recovery minimizes a disaster's impact, reduces downtime, and increases the Linux system's security.

To create a [disaster recovery plan](https://phoenixnap.com/blog/disaster-recovery-plan-checklist), follow this checklist:

* Identify critical systems and data that must be recovered in a disaster.  
* Choose a backup and recovery solution that meets your needs and budget.  
* Test the backup and recovery plan regularly to ensure it works as expected.  
* Train all personnel on the disaster recovery plan and procedures.  
* Document the plan and keep it up-to-date.

#### 38\. Upgrade Security Incident Response Plan (CSIRP)

(Advanced security mechanism)

An effective [security incident response plan (CSIRP)](https://phoenixnap.com/phoenixnap.com/blog/cyber-security-incident-response-plan) is critical to a robust security program. It provides a clear and organized plan for responding to various security incidents, such as data breaches, cyber-attacks, and other security-related events. It is essential to periodically update the CSIRP to keep up with new security threats and be able to detect and respond to security incidents to minimize damage and data loss.

When upgrading the CRISP, make sure to:

* Review the current plan and identify areas for improvement.  
* Evaluate contemporary security threats and assess the impact.  
* Revise incident response procedures to align with current security best practices.  
* Update incident categorization and prioritization criteria.  
* Review and update communication plans for internal and external stakeholders.  
* Test and refine the updated CSIRP through simulations and tabletop exercises.

#### 39\. Use a Security-Focused Web Browser

(Basic security mechanism)

Using a security-focused web browser and configuring it to block malicious sites on Linux protects against malware attacks by blocking access to known malicious websites and warning users about potentially dangerous sites.

Certain security-focused web browsers like Tor encrypt internet connections to protect against eavesdropping and tampering. The process creates a secure internet connection and reduces the risk of hacking or other cyber attacks.

By blocking malicious sites, security-focused web browsers reduce the risk of data breaches when users inadvertently access sites that contain malware or steal personal information.

#### 40\. Ensure Linux Server Physical Security

(Intermediate/Advanced security mechanism)

To ensure the physical security of Linux servers, organizations must implement several measures to prevent unauthorized access. Here are the key steps to consider:

* Secure physical console access. Configure the BIOS to disable booting from external devices such as CDs, DVDs, or [USB](https://phoenixnap.com/glossary/what-is-a-usb-port) pens. Set BIOS and GRUB boot loader passwords to protect these settings.  
* Implement multi-layered security. Use physical locks on server room doors, install security cameras to monitor the area, implement access control systems to restrict access to unauthorized personnel and regularly check the servers for signs of tampering or theft.  
* Implement environmental controls. Consider installing air conditioning to prevent server damage due to heat or other environmental factors.  
* Perform regular security audits. Ensure that the physical security measures are up to date and effective in preventing unauthorized server access.  
* Lock servers in IDCs. Make sure to lock all production servers in IDCs (Internet Data Centers) and perform security checks on all personnel accessing the server.

## 

## Common vulnerabilities affecting Windows Services

Windows Services are essential components of the operating system, providing various functionalities. However, like any software, they can be vulnerable to exploits. Here are some common vulnerabilities that can affect Windows Services:

* Misconfigurations:  
  * Weak or Default Credentials: Services often run under system accounts with elevated privileges. If these accounts use weak default passwords or are not properly secured, attackers can exploit them for unauthorized access.  
  * Unnecessary Services: Running unnecessary services increases the attack surface. Disable or uninstall any services that are not required.  
  * Improper Service Accounts: Using domain user accounts instead of dedicated service accounts can increase the risk of compromise.  
* Vulnerabilities in Service Code:  
  * Buffer overflows: Exploiting memory management errors in the service code to execute arbitrary code.  
  * Remote Procedure Call (RPC) vulnerabilities: Exploiting weaknesses in RPC interfaces to gain unauthorized access.  
* Denial of Service (DoS) vulnerabilities: Attackers can exploit vulnerabilities to crash the service or prevent it from functioning correctly.  
* Insufficient Logging and Monitoring:  
  * Lack of adequate logging and monitoring can make it difficult to detect and respond to attacks targeting Windows Services.  
* Privilege Escalation:  
  * Attackers may exploit vulnerabilities in a lower-privileged service to gain higher-level privileges on the system.

Examples of Specific Vulnerabilities:

* EternalBlue: A well-known exploit that leveraged vulnerabilities in the Server Message Block (SMB) protocol, impacting many Windows services.  
* WannaCry: A ransomware attack that exploited the EternalBlue exploit to rapidly spread across networks.  
* Zerologon: A critical vulnerability affecting the Netlogon protocol in Active Directory, allowing attackers to gain domain administrator privileges.

Mitigating Vulnerabilities in Windows Services:

* Regular Patching: Apply all critical security updates and patches from Microsoft promptly.  
* Strong Authentication: Use strong passwords, multi-factor authentication, and least privilege principles for service accounts.  
* Regular Auditing and Monitoring: Monitor service logs for suspicious activity and conduct regular security audits.  
* Implement Security Best Practices: Follow security best practices, such as disabling unnecessary services, using firewalls, and implementing intrusion detection systems.  
* Regular Security Assessments: Conduct regular security assessments to identify and address vulnerabilities.

## 

## Testing Web Servers and Frameworks

Common Vulnerabilities

* Injection Flaws:  
  * SQL Injection: Injecting malicious SQL commands into web forms to manipulate databases.  
  * Cross-Site Scripting (XSS): Injecting malicious scripts into web pages to steal user data or hijack sessions.  
  * OS Command Injection: Injecting operating system commands into web applications.  
* Broken Authentication and Session Management:  
  * Weak passwords: Enforcing weak password policies.  
  * Session hijacking: Stealing or manipulating user sessions.  
  * Insufficient session management: Lack of proper session handling and timeout mechanisms.  
* Cross-Site Request Forgery (CSRF): Tricking users into performing unintended actions on a web application.  
* Security Misconfiguration:  
  * Insecure default configurations: Using default configurations for web servers, databases, and applications.  
  * Missing or weak security controls: Inadequate access controls, encryption, or input validation.  
* Sensitive Data Exposure:  
  * Exposing sensitive data such as credit card numbers, social security numbers, and personal information without proper encryption or authorization.  
* Broken Access Control:  
  * Insufficient authorization mechanisms, allowing unauthorized access to sensitive data or functionalities.  
* Denial of Service (DoS) Attacks:  
  * Attacks that aim to overload a web server or application, making it unavailable to legitimate users.

2\. Testing Techniques

* Manual Testing:  
  * Black-box testing: Testing the application without prior knowledge of its internal structure.  
  * White-box testing: Testing with knowledge of the application's source code.  
  * Gray-box testing: Testing with limited knowledge of the application's internal structure.  
* Automated Testing:  
  * Vulnerability scanners: Tools like OWASP ZAP, Burp Suite, and Kali Linux provide automated tools for identifying vulnerabilities.  
  * Fuzzing: Techniques for automatically finding software bugs by providing unexpected inputs.  
  * Static Application Security Testing (SAST): Analyzing source code for security vulnerabilities.  
  * Dynamic Application Security Testing (DAST): Testing running applications to identify vulnerabilities.

3\. Web Server Hardening

* Secure configurations:  
  * Disable unnecessary services.  
  * Restrict access to administrative interfaces.  
  * Implement strong authentication and authorization mechanisms.  
* Configure firewalls to block unauthorized traffic.  
* Regular patching:  
  * Keep the web server and all installed software updated with the latest security patches.  
* Intrusion Detection and Prevention Systems (IDS/IPS):  
* Deploy IDS/IPS systems to monitor web server traffic for malicious activity.

4\. Web Application Frameworks

* Security considerations: Understand the security implications of using different web application frameworks (e.g., Django, Ruby on Rails, Node.js).  
* Built-in security features: Utilize built-in security features of the framework, such as input validation, output encoding, and authentication mechanisms.

Key Takeaways for CNSP

* Understand the OWASP Top 10: Familiarize yourself with the OWASP Top 10, a list of the most critical web application security risks.  
* Practice vulnerability scanning: Use tools like Nmap and OWASP ZAP to gain hands-on experience with web application security testing.  
* Stay updated: Keep up-to-date with the latest web application security threats and vulnerabilities.

## 

## Basic Malware Analysis

Malware analysis is a crucial skill for any cybersecurity professional. It involves investigating malicious software to understand its behavior, identify its origin, and determine its impact. Here's a breakdown of key concepts for the CNSP exam:

1\. Types of Malware

* Viruses: Self-replicating code that attaches itself to other programs.  
* Worms: Self-replicating malware that spreads across networks without human interaction.  
* Trojans: Malicious software disguised as legitimate software.  
* Ransomware: Malware that encrypts files and demands a ransom for their release.  
* Rootkits: Malware that hides itself deeply within the operating system.  
* Spyware: Software that collects information about a user without their knowledge or consent.  
* Adware: Software that displays unwanted advertisements.

2\. Malware Analysis Techniques

* Static Analysis:  
  * File analysis: Examining the malware file itself, including its file headers, strings, and code.  
  * Disassembly: Disassembling the malware code to understand its functionality.  
  * Sandbox analysis: Analyzing the malware in a controlled environment to observe its behavior without affecting the host system.  
* Dynamic Analysis:  
  * Running the malware in a controlled environment: Observing the malware's behavior in action, such as network connections, file system modifications, and system resource usage.  
  * Debugging: Using debugging tools to step through the malware's code and understand its execution flow.  
  * Network traffic analysis: Monitoring network traffic generated by the malware.

3\. Tools for Malware Analysis

* Sandbox environments: Virtual machines or isolated environments for safely analyzing malware.  
* Disassemblers: Tools like IDA Pro, Ghidra, and Hopper for disassembling malware code.  
* Debuggers: Tools like GDB and WinDbg for debugging malware.  
* Packet analyzers: Tools like Wireshark for analyzing network traffic generated by malware.  
* Antivirus and anti-malware software: Can provide initial insights into the nature of the malware.

4\. Indicators of Compromise (IOCs)

* Hashes: Unique identifiers for files (MD5, SHA1, SHA256).  
* IP addresses: IP addresses of command-and-control servers.  
* Domain names: Domains associated with the malware.  
* URLs: URLs used by the malware to download or communicate.  
* File names: Names of malicious files.

5\. Malware Analysis in a Security Operations Center (SOC)

* Incident Response: Malware analysis plays a crucial role in incident response investigations, helping to identify the source of the attack, the scope of the infection, and the best course of action for remediation.  
* Threat Hunting: Malware analysis can be used to proactively hunt for threats within an organization's network.

Key Takeaways for CNSP

* Understand the different types of malware and their behavior.  
* Be familiar with basic malware analysis techniques.  
* Know how to use common malware analysis tools.  
* Understand the importance of IOCs in threat intelligence.  
* Recognize the role of malware analysis in incident response and threat hunting.

## 

## Social Engineering attacks

Social engineering is a dangerous weapon many cybercriminals use to achieve their nefarious goals. It leverages psychological manipulation to deceive individuals into divulging confidential or personal information. Unlike traditional hacking, which relies on exploiting software vulnerabilities, social engineering targets human vulnerabilities.

Here are the most common types of social engineering attacks in 2024 and real-world examples to highlight their impact.

### Phishing: Hook, Line, and Sinker

[Phishing](https://www.terranovasecurity.com/solutions/security-awareness-training/what-is-phishing) is one of the most common social engineering attacks. It involves sending fraudulent communications, usually emails, that appear to come from a legitimate source. The goal is to trick recipients into providing sensitive information, such as login credentials or financial details.

Example: In 2022, [a sophisticated phishing attack](https://www.bleepingcomputer.com/news/security/office-365-phishing-attack-impersonates-the-us-department-of-labor/) aimed at stealing Office 365 credentials, where attackers impersonated the US Department of Labor (DoL). This scam exemplifies the increasing sophistication and convincing nature of modern phishing attempts.

### Spear Phishing: Precision Social Engineering

Spear phishing is a more targeted version of phishing. While phishing attacks are often sent to many recipients with a “mud-against-the-wall” approach, spear phishing targets specific individuals or firms. The malicious actor customizes the message based on information about the target, making it more convincing.

Example: As world leaders deliberated on the best response to the escalating tensions between Russia and Ukraine, Microsoft issued a warning in February 2022 about a new [spear phishing campaign](https://thehackernews.com/2022/02/microsoft-uncovers-new-details-of.html) by a Russian hacking group targeting Ukrainian public sector entities and NGOs.

The group, known as Gamaredon and tracked by Microsoft as ACTINIUM, had reportedly targeted “organizations critical to emergency response and ensuring the security of Ukrainian territory” since 2021\.

### Pretexting: Mastering the Art of Social Engineering

Pretexting is another form of social engineering involving creating a fabricated scenario to steal information. These scams use the same social engineering techniques that con artists have used for centuries to manipulate their victims, such as deception, validation, flattery, and intimidation. The attacker pretends to need the information to confirm the victim’s identity or to help with a supposed emergency.

At the organizational level, a pretexting actor may take extensive measures to impersonate trusted figures such as managers, coworkers, or customers. This could involve fabricating identities through fraudulent email addresses, websites, or social media profiles.

In more elaborate scenarios, the attacker might arrange face-to-face meetings with targets. For instance, a hacker masquerading as a vendor representative might schedule a meeting to gain access to confidential customer data. The attacker aims to appear credible during these encounters and build rapport with the target. By establishing trust, the attacker increases the likelihood that the target will comply with requests for sensitive information, believing them to be legitimate.

### Deepfakes: Seeing Isn’t Believing

Deepfakes, which use artificial intelligence (AI) to create realistic but fake audio, video, or images that impersonate real people, are increasingly used in various social engineering attacks to create compelling but fraudulent scenarios. They leverage manipulated audio and video to deceive targets into disclosing sensitive information or performing actions they otherwise would not.

Example: In 2019, a [deepfake attack](https://www.forbes.com/sites/jessedamiani/2019/09/03/a-voice-deepfake-was-used-to-scam-a-ceo-out-of-243000/) targeted a UK-based energy firm. Bad actors used AI-generated audio to impersonate the voice of the parent company's chief executive. They called the target company’s CEO, instructing him to transfer around $243,000 to a Hungarian supplier urgently. The voice was so convincing that the executive complied with the request.

### Not So Quid Pro Quo

Another type of social engineering is quid pro quo attacks, which involve offering a service or benefit in exchange for information. Attackers may promise tech support, free software, or other services to persuade victims to reveal confidential information.

Examples: One of the most prevalent quid pro quo attacks involves fraudsters posing as representatives of the US Social Security Administration (SSA). These fraudsters contact individuals randomly, requesting confirmation of their Social Security Numbers under false pretenses, enabling identity theft.

Alternatively, malicious actors identified by the Federal Trade Commission (FTC) create counterfeit SSA websites to obtain personal information illicitly. Frighteningly, attackers don’t need to be that cunning, as previous incidents have demonstrated that office employees are willing to divulge their passwords in exchange for inexpensive items like pens or chocolate bars.

### Honeytraps: Love, Lies, and Larceny

Honeytraps involve creating fake online personas to establish romantic relationships with victims. The goal is to gain and exploit the victim’s trust for financial gain or access to sensitive information.

Example: According to police reports, a man from Vancouver Island lost $150,000 in [a romance scam](https://vancouversun.com/news/local-news/vancouver-island-man-loses-150000-romance-scam). Over several months, the scammer requested money for plane tickets, medical bills, and various other expenses.

### Piggybacking: Hitching a Ride

Two other widespread threats are tailgating and piggybacking. Tailgating, in essence, is unauthorized access to secured spaces, which malefactors gain by exploiting the trust of real users. It involves gaining physical access to a restricted area by following someone with legitimate access and exploiting the courtesy of others to gain entry without proper authorization. It can also involve badge cloning, using unattended devices, or impersonation. Piggybacking happens when someone attempts to piggyback onto a hacker's attempted extortion.

Example: In 2018, an individual admitted guilt in England's Reading Crown Court for [unauthorized computer access and blackmail](https://www.bankinfosecurity.com/employee-admits-piggybacking-hackers-extortion-attempt-a-22142) while working at Oxford Biomedica, a gene therapy company. There was an incident where the company faced a ransom demand of $370,000 in Bitcoin after an attack.

An employee (ironically part of the response team) altered ransom notes to redirect payments to his cryptocurrency wallet, effectively launching a separate attack against his employer.

### Business Email Compromise: The Impersonation Game

Business email compromise (BEC) is a sophisticated cyberattack where criminals meticulously gather information about an organization's structure and key executives. Using this knowledge, they exploit the trust associated with high-ranking positions, like the CFO, to [manipulate employees](https://www.tripwire.com/state-of-security/watch-out-cisa-warns-it-being-impersonated-scammers) into transferring funds or divulging sensitive information.

By gaining access to an executive's email account, attackers [impersonate them](https://www.tripwire.com/state-of-security/watch-out-cisa-warns-it-being-impersonated-scammers) to request urgent financial transactions, such as paying fraudulent invoices. They exploit the time-sensitive nature of these transactions to minimize the chances of detection.

BEC is one of the most common attacks and one of the most costly types of cybercrime. Between 2013 and 2022, the FBI says BEC attacks caused roughly $50.8 billion in losses worldwide.

### Fighting the Exploitation

Social engineering attacks are a growing scourge in today's digital landscape. They exploit human psychology rather than technological weaknesses, making them particularly challenging to defend against. Awareness and education are crucial in combating these attacks.

Companies should integrate the following recommendations into their security awareness training:

* Exercise caution with emails from unfamiliar sources. If you receive a suspicious email, verify its legitimacy by contacting the sender directly via phone or in person.  
* Be skeptical of unsolicited offers. If something appears too good to be true, it likely is.  
* Always lock your laptop when stepping away from your workstation to prevent unauthorized access.  
* Invest in antivirus software. While no antivirus solution offers foolproof protection, it can significantly bolster defenses against social engineering tactics.  
* Familiarize yourself with your company’s privacy policy to understand protocols regarding access permissions for external individuals.  
* Validate urgent requests from internal contacts before taking action, primarily involving financial transactions or sensitive information.  
* Foster a culture of risk awareness to keep employees vigilant. Social engineering thrives on [human error](https://www.terranovasecurity.com/solutions/security-awareness-training/what-is-social-engineering#human-error), so embedding security awareness into the organizational mindset is crucial. Employees should know how to recognize and report potential incidents promptly.

By understanding the common types of social engineering attacks and recognizing their real-world implications, individuals and organizations can better protect themselves from these pervasive threats.

## 

## Network Security Tools and Frameworks (such as Nmap, Wireshark etc)

This area of the CNSP exam focuses on the practical tools and frameworks used by cybersecurity professionals. Here's a breakdown of key tools and their significance:

1\. Network Scanning & Discovery

* Nmap:  
  * Key Features: Powerful and versatile for host discovery, port scanning, service detection, OS fingerprinting, and vulnerability scanning.  
  * CNSP Relevance: Essential for network mapping, identifying open ports and services, and discovering potential vulnerabilities.  
* Wireshark:  
  * Key Features: Network protocol analyzer for capturing and analyzing network traffic.  
  * CNSP Relevance: Used for traffic analysis, identifying suspicious activity, troubleshooting network issues, and understanding network protocols.  
* Zenmap:  
  * Key Features: Graphical user interface for Nmap, providing a more user-friendly experience.

2\. Vulnerability Scanning

* Nessus:  
  * Key Features: Comprehensive vulnerability scanner that identifies and prioritizes vulnerabilities in systems and applications.  
  * CNSP Relevance: Essential for identifying and assessing vulnerabilities across various systems and applications.  
* OpenVAS:  
  * Key Features: Open-source vulnerability scanner with a robust feature set, including vulnerability checks, compliance testing, and reporting.  
* Metasploit:  
  * Key Features: A penetration testing framework with a wide range of tools for exploitation, vulnerability analysis, and social engineering.  
* CNSP Relevance: Provides hands-on experience with penetration testing techniques and exploitation methods.

3\. Intrusion Detection and Prevention Systems (IDS/IPS)

* Snort:  
  * Key Features: Open-source network intrusion detection system (IDS) that can also be configured as an intrusion prevention system (IPS).  
  * CNSP Relevance: Understands how IDS/IPS work, their role in detecting and preventing attacks, and how to configure and tune them.  
* Suricata:  
  * Key Features: High-performance network security monitoring engine that can be used for IDS, IPS, and network security monitoring.

4\. Security Information and Event Management (SIEM)

* Splunk:  
  * Key Features: A popular SIEM platform for collecting, analyzing, and correlating security logs from various sources.  
  * CNSP Relevance: Understanding how SIEM systems work, their role in threat detection and incident response, and how to configure and use SIEM rules.  
* Elasticsearch, Logstash, Kibana (ELK Stack):  
  * Key Features: An open-source platform for collecting, analyzing, and visualizing log data.  
  * CNSP Relevance: Provides a foundation for building custom SIEM solutions and analyzing security events.

5\. Other Important Tools

* Sysinternals Suite: A collection of utilities for Windows systems that can be used for troubleshooting, system administration, and security analysis.  
* Wireshark: While primarily a network protocol analyzer, it can also be used for basic security analysis.

## 

## Open-Source Intelligence Gathering (OSINT)

Open Source Intelligence (OSINT) is a method of gathering information from public or other open sources, which can be used by [security experts](https://www.imperva.com/learn/application-security/ethical-hacking/), national intelligence agencies, or cybercriminals. When used by cyber defenders, the goal is to discover publicly available information related to their organization that could be used by attackers, and take steps to prevent those future attacks.

OSINT leverages advanced technology to discover and analyze massive amounts of data, obtained by scanning public networks, from publicly available sources like social media networks, and from the deep web—content that is not crawled by search engines, but is still publicly accessible.

OSINT tools may be open source or proprietary: the distinction should be made between open source code and open source content. Even if the tool itself is not open source, as an OSINT tool, it provides [access to openly available content](https://www.imperva.com/learn/application-security/broken-object-level-authorization-bola/), known as open source intelligence.

### History of OSINT

The term OSINT was originally used by the military and intelligence community, to denote intelligence activities that gather strategically important, publicly available information on national security issues.

In the cold war era, espionage focused on obtaining information via human sources (HUMINT) or electronic signals (SIGINT), and in the 1980s OSINT gained prominence as an additional method of gathering intelligence.

With the advent of the Internet, social media, and digital services, open source intelligence grants access to numerous resources to gather intelligence about every aspect of an organization’s IT infrastructure and employees. Security organizations are realizing that they must collect this publicly available information, to stay one step ahead of attackers.

A CISO’s primary goal is to find information that could pose a risk to the organization. This allows CISOs to reduce risk before an attacker exploits a threat. OSINT should be used in combination with regular [penetration testing](https://www.imperva.com/learn/application-security/penetration-testing/), in which information discovered via OSINT is used to simulate a breach of organizational systems.

### How Attackers and Defenders Use OSINT

There are three common uses of OSINT: by cybercriminals, by cyber defenders, and by those seeking to monitor and shape public opinion.

### How Security Teams Use OSINT

For penetration testers and security teams, OSINT aims to reveal public information about internal assets and other information accessible outside the organization. Metadata accidentally published by your organization may contain sensitive information.

For example, useful information that can be revealed through OSINT includes open ports; unpatched software with known [vulnerabilities](https://www.imperva.com/learn/application-security/cve-cvss-vulnerability/); publicly available IT information such as device names, IP addresses and configurations; and other leaked information belonging to the organization.

Websites outside of your organization, especially social media, contain huge amounts of relevant information, especially information about employees. Vendors and partners may also be sharing specific details about an organization’s IT environment. When a company acquires other companies, their publicly available information becomes relevant as well.

### How Threat Actors Use OSINT

A common use of OSINT by attackers is to retrieve personal and professional information about employees on social media. This can be used to craft [spear-phishing](https://www.imperva.com/learn/application-security/spear-phishing/) campaigns, targeted at individuals who have privileged access to company resources.

LinkedIn is a great resource for this type of open source intelligence, because it reveals job titles and organizational structure. Other social networking sites are also highly valuable for attackers, because they disclose information such as dates of birth, names of family members and pets, all of which can be used in [phishing](https://www.imperva.com/learn/application-security/phishing-attack-scam/) and to guess passwords.

Another common tactic is to use cloud resources to scan public networks for unpatched assets, open ports, and misconfigured cloud datastores. If an attacker knows what they are looking for, they can also retrieve credentials and other leaked information from sites like GitHub. Developers who are not security conscious can embed passwords and encryption keys in their code, and attackers can identify these secrets through specialized searches.

### Other Uses of OSINT

In addition to [cybersecurity](https://www.imperva.com/learn/application-security/cyber-security/), OSINT is also frequently used by organizations or governments seeking to monitor and influence public opinion. OSINT can be used for marketing, political campaigns, and disaster management.

### OSINT Gathering Techniques

Here are three methods commonly used to gain open intelligence data.

Passive Collection

This is the most commonly used way to gather OSINT intelligence. It involves scraping publicly available websites, retrieving data from open APIs such as the Twitter API, or pulling data from deep web information sources. The data is then parsed and organized for consumption.

Semi-Passive

This type of collection requires more expertise. It directs traffic to a target server to obtain information about the server. Scanner traffic must be similar to normal Internet traffic to avoid detection.

Active Collection

This type of information collection interacts directly with a system to gather information about it. Active collection systems use advanced technologies to access open ports, and scan servers or web applications for vulnerabilities.

This type of data collection can be detected by the target and reveals the reconnaissance process. It leaves a trail in the target’s firewall, [Intrusion Detection System (IDS), or Intrusion Prevention System (IPS)](https://www.imperva.com/learn/application-security/intrusion-detection-prevention/). [Social engineering attacks](https://www.imperva.com/learn/application-security/social-engineering-attack/) on targets are also considered a form of active intelligence gathering.

### Artificial Intelligence: The Future of OSINT?

OSINT technology is advancing, and many are proposing the use of artificial intelligence and machine learning (AI/ML) to assist OSINT research.

According to public reports, government agencies and intelligence agencies are already using artificial intelligence to gather and analyze data from social media. Military organizations are using AI/ML to identify and combat terrorism, organized cybercrime, false propaganda, and other national security concerns on social media channels.

As AI/ML techniques become available to the private sector, they can help with:

* Improving the data collection phase—filtering out noise and prioritizing data  
* Improving the data analysis phase—correlating relevant information and identifying useful structures  
* Improving actionable insights—AI/ML analysis can be used to review far more raw data than human analysts can, deriving more actionable insights from the available data.

### OSINT Tools

Here are some of the most popular OSINT tools.

#### Maltego

Maltego is part of the Kali Linux operating system, commonly used by network penetration testers and hackers. It is open source, but requires registration with Paterva, the solution vendor. Users can run a “machine”, a type of scripting mechanism, against a target, configuring it according to the information they want to collect.

Main features include:

* Built-in data transformations.  
* Ability to write custom transformations.  
* Built-in footprints that can collect information from sources and create a visualization of data about a target.

#### Spiderfoot

Spiderfoot is a free OSINT tool available on Github. It integrates with multiple data sources, and can be used to gather information about an organization including network addresses, contact details, and credentials.

Main features include:

* Gathers and analyzes network data including IP addresses, classless inter-domain routing (CIDR) ranges, domains and subdomains.  
* Gathers email addresses, phone numbers, and other contact details.  
* Collects usernames for accounts operated by an organization.  
* Collects Bitcoin addresses.

#### Spyse

Spyse is an “Internet assets search engine”, designed for security professionals. It collects data from publicly available sources, analyzes them, and identifies security risks.

Main features include:

* Collects data from websites, website owners, and the infrastructure they are running on  
* Collects data from publicly exposed IoT devices  
* Identifies connections between entities  
* Reports on publicly exposed data that represents a security risk

#### Intelligence X

Intelligence X is an archival service that preserves historical versions of web pages that were removed for legal reasons or due to content censorship. It preserves any type of content, no matter how dark or controversial. This includes not only data censored from the public Internet but also data from the dark web, wikileaks, government sites of nations known to engage in [cyber attacks](https://www.imperva.com/learn/application-security/cyber-attack/), and many other data leaks.

Main features include:

* Search on email addresses or other contact details.  
* Advanced search on domains and URLs.  
* Search for IPs and CIDR ranges, with support for IPv4 and IPv6.  
* Search for MAC addresses and IPFS Hashes.  
* Search for financial data such as account numbers and credit card numbers  
* Search for personally identifiable information  
* Darknet: Tor and I2P  
* Wikileaks & Cryptome  
* Government sites of North Korea and Russia  
* Public and Private Data Leaks  
* Whois Data  
* Dumpster: Everything else  
* Public Web

#### BuiltWith

BuiltWith maintains a large database of websites, which includes information on the technology stacks used by each site. You can combine BuiltWith with security scanners to identify specific vulnerabilities affecting a website.

Main features include:

* Reporting on the content management system (CMS) in use by a website, its version, and plugins currently in use.  
* Reporting on other infrastructure components used by a website, such as a [CDN](https://www.imperva.com/learn/performance/what-is-cdn-how-it-works/).  
* Providing a list of JavaScript and CSS libraries used by the website.  
* Providing information about the web server running the website.  
* Providing details of analytics and tracking tools deployed by a website.

#### Shodan

Shodan is a security monitoring solution that makes it possible to search the deep web and IoT networks. It makes it possible to discover any type of device connected to a network, including servers, smart electronics devices, and webcams.

Main features include:

* Easy to use search engine interface.  
* Provides information on devices operating on protocols like HTTP, SSH, FTP, SNMP, Telnet, RTSP, and IMAP.  
* Results can be filtered and ordered by protocol, network ports, region, and operating system.  
* Access to a huge range of connected devices, including home appliances and public utilities such as traffic lights and water control systems.

#### HaveIbeenPwned

HaveIbeenPwned is a service that can be used directly by consumers who were impacted by [data breaches](https://www.imperva.com/learn/data-security/data-breach/). It was developed by security researcher Troy Hunt.

Main features include:

* Identifying if an individual email address was compromised in any historical breach.  
* Checking accounts on popular services like LastFM, Kickstarter, WordPress.com, and LinkedIn for exposure to past data breaches.

#### Google Dorking

[Google dorking](https://www.imperva.com/learn/application-security/google-hacking/) is not exactly a tool – it is a technique commonly used by security professionals and hackers to identify exposed private data or security vulnerabilities via the Google search engine.

Google has the world’s largest database of Internet content, and it provides a range of advanced search operators. Using these search operators it is possible to identify content that can be useful to attackers.

Here are operators commonly used to perform Google Dorking:

* Filetype – enables finding exposed files with a file type that can be exploited  
* Ext – similarly, finds exposed files with specific extensions that can be useful in attack (for example .log)  
* Intitle/inurl – looks for sensitive information in a document title or URL. For example, any URL containing the term “admin” could be useful to an attacker.  
* Quotes – the quote operator enables searching for a specific string. Attackers can search for a variety of strings that indicate common server issues or other vulnerabilities.

#### Open Source Investigation Best Practices

Here are best practices that can help you use OSINT more effectively for cyber defense.

Distinguish Between Data and Intelligence

Open source data (OSD) is raw, unfiltered information available from public sources. This is the input of OSINT, but in itself, it is not useful. Open source intelligence (OSINT) is a structured, packaged form of OSD which can be used for security activity.

To successfully practice OSINT, you should not focus on collecting as much data as possible. Focus on identifying the data needed for a specific investigation, and refine your search to retrieve only the relevant information. This will let you derive useful insights at lower cost and with less effort.

Consider Compliance Requirements

Most organizations are covered by the [General Data Protection Regulation](https://www.imperva.com/learn/data-security/general-data-protection-regulation-gdpr/) (GDPR) or other privacy regulations. OSINT very commonly collects personal data, which can be defined as [personally identifiable information](https://www.imperva.com/learn/data-security/personally-identifiable-information-pii/) (PII). Collecting, storing, and processing this data can create a compliance risk for your organization.

In addition, if you discover criminal intent in an OSINT investigation, there may be specific legal requirements for exposing this data. For example, in the UK, exposing information that can tip off an individual under investigation for money laundering can lead to unlimited fines and prison time.

Be Ethical

OSINT relies on publicly accessible data, but the use of this data can impact people, both in your organization and outside it. When you collect data, do not only consider your investigative needs, but also the ethical and regulatory impact of the data. Limit data collection to a minimum that can help you meet your goals without violating the rights of employees or others.

Letting technology collect data or scan systems “on autopilot” will often result in unethical or illegal data collection. A key part of ethical OSINT is to ensure data collection is controlled by humans, with effective collaboration between all stakeholders. Everyone involved in the OSINT project should understand ethical and legal constraints, and should work together to avoid privacy issues and other ethical concerns.

## 

## Database Security Basics

## 

Database security is crucial for any organization that relies on data. Here are some key concepts for the CNSP exam:

1\. Access Control

* Least Privilege: Grant users only the minimum necessary privileges to perform their job functions.  
* This minimizes the impact of a compromised account.  
* Role-Based Access Control (RBAC): Assign permissions based on user roles and responsibilities within the organization.  
* Authentication and Authorization: Implement strong authentication methods (e.g., passwords, multi-factor authentication) and authorization mechanisms to control access to sensitive data.

2\. Data Encryption

* Data at Rest: Encrypt data stored on the database server (e.g., using Transparent Data Encryption \- TDE).  
* Data in Transit: Encrypt data transmitted between the database server and applications (e.g., using SSL/TLS).

3\. Vulnerability Management

* Regular Patching: Keep the database software and related components up-to-date with the latest security patches and updates.  
* Vulnerability Scanning: Regularly scan the database server and applications for known vulnerabilities.  
* Penetration Testing: Conduct penetration tests to identify and exploit potential vulnerabilities.

4\. Data Loss Prevention (DLP)

* Data Classification: Classify data based on sensitivity (e.g., confidential, sensitive, public).  
* Data Masking: Replace sensitive data with fake or masked data for testing and development purposes.  
* Data Discovery: Identify and locate sensitive data within the database.

5\. Auditing and Monitoring

* Database Activity Monitoring: Monitor database activity for suspicious behavior, such as unusual login attempts, excessive data access, and SQL injection attempts.  
* Log Analysis: Analyze database logs to identify and investigate security incidents.

6\. Separation of Duties:

* Ensure that different individuals are responsible for different aspects of database administration (e.g., database administrators, security administrators).

7\. Physical Security:

* Protect the physical security of the database server by implementing appropriate physical access controls.

Common Vulnerabilities:

* SQL Injection: Attackers inject malicious SQL code into database queries to gain unauthorized access or manipulate data.  
* Cross-Site Scripting (XSS): Attackers inject malicious scripts into web applications, which can then be executed by other users.  
* Denial of Service (DoS) attacks: Attacks that aim to overload the database server, making it unavailable to legitimate users.

Key Takeaways for CNSP

* Understand the importance of data security within a database context.  
* Be familiar with common database security vulnerabilities and threats.  
* Implement strong access controls and authentication mechanisms.  
* Regularly audit and monitor database activity.  
* Stay informed about the latest database security best practices.

## 

## TLS Security Basics

## 

TLS is a cryptographic protocol designed to ensure privacy and data integrity over computer networks. It's crucial for secure communication, especially over the internet. Here's a breakdown of key concepts:

1\. Core Functions:

* Encryption: Encrypts data transmitted between two parties, making it unreadable to eavesdroppers.  
* Authentication: Verifies the identity of the communicating parties (e.g., website server, client).  
* Data Integrity: Ensures that data transmitted between parties has not been tampered with.

2\. Key Concepts:

* Asymmetric Encryption: Uses a pair of keys: a public key (shared with everyone) and a private key (kept secret). Data encrypted with the public key can only be decrypted with the corresponding private key.  
* Symmetric Encryption: Uses a single, shared secret key for both encryption and decryption. Symmetric encryption is faster than asymmetric encryption.  
* Digital Certificates: Electronic documents that bind a public key to an entity (e.g., a website server). Issued by Certificate Authorities (CAs).  
* Handshake: The initial negotiation phase of a TLS connection, where the server and client establish a secure communication channel.

3\. TLS Handshake (Simplified)

1. Client Hello: The client initiates the handshake, sending a list of supported cipher suites and TLS versions.  
2. Server Hello: The server selects a cipher suite and sends its certificate to the client.  
3. Client Key Exchange: The client generates a pre-master secret and encrypts it using the server's public key.  
4. Server Hello Done: The server acknowledges receipt of the client's message.  
5. Client Change Cipher Spec: The client notifies the server that it will now use the negotiated cipher suite.  
6. Encrypted Handshake Messages: The client and server exchange encrypted messages to establish the shared session key.  
7. Application Data: After the handshake is complete, encrypted data can be exchanged between the client and server.

4\. Importance of TLS

* Securing online transactions: Protects sensitive information like credit card numbers and personal data during online purchases.  
* Ensuring data privacy: Prevents eavesdropping on online communications, such as emails and web browsing.  
* Building trust: Verifies the identity of websites and other online services.

5\. TLS Versions and Vulnerabilities

* TLS 1.0, 1.1: Older versions with known vulnerabilities.  
* TLS 1.2: A more secure version, but still vulnerable to some attacks.  
* TLS 1.3: The latest version, offering improved security, performance, and privacy.

## 

## Password Storage

Securely storing passwords is critical for individual users and organizations alike. Here's a breakdown of key concepts and best practices for Windows and Linux environments:

1\. Risks of Storing Passwords Insecurely:

* Data Breaches: If passwords are stored in plain text or easily accessible files, a successful breach can compromise numerous accounts.  
* Identity Theft: Stolen passwords can be used for identity theft, financial fraud, and other malicious activities.  
* Account Compromise: Compromised passwords can grant attackers access to sensitive systems and data.

2\. Secure Password Storage Methods:

* Password Managers:  
  * Strong Encryption: Utilize password managers like LastPass, 1Password, or KeePass, which encrypt passwords using strong algorithms.  
  * Centralized Storage: Store all your passwords securely in a single, encrypted vault.  
  * Cross-Platform Compatibility: Access your passwords across different devices (computers, smartphones, tablets).  
* Operating System Features:  
  * Windows: Utilize the built-in Credential Manager to store credentials for websites and applications.  
  * Linux: Utilize tools like gpg (GNU Privacy Guard) to encrypt and store passwords securely.  
* Hardware Security Modules (HSMs):  
  * High-security devices that can generate, store, and manage cryptographic keys.  
  * Primarily used in enterprise environments for high-security needs.

3\. Best Practices for Password Storage:

* Strong Passwords: Use strong, unique passwords for each account.  
* Regular Password Changes: Regularly change passwords for critical accounts.  
* Multi-Factor Authentication (MFA): Implement MFA wherever possible to add an extra layer of security.  
* Avoid storing passwords in plain text: Never store passwords in plain text files or in easily accessible locations.  
* Use a reputable password manager: Choose a password manager with a strong security track record.  
* Regularly review and update security settings: Ensure that your password manager and other security tools are up-to-date with the latest security patches.
