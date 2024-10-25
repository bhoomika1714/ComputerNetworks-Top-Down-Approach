# Transport Services (TCP & UDP):
**Responsibilities of a Transport Layer**
* The Process to Process Delivery
* End-to-End Connection between Hosts
* Multiplexing and Demultiplexing
* Congestion Control
* Data integrity and Error correction
* Flow control

## What is Transmission Control Protocol (TCP)?
TCP is one of the main protocols of the Internet protocol suite. It lies between the Application and Network Layers which are used in providing reliable delivery services. It is a connection-oriented protocol for communications that helps in the exchange of messages between different devices over a network.
<br>
**Features of TCP**
* TCP keeps track of the segments being transmitted or received by assigning numbers to every single one of them.
* Flow control limits the rate at which a sender transfers data. This is done to ensure reliable delivery.
* TCP implements an error control mechanism for reliable data transfer.
* TCP takes into account the level of congestion in the network.

### Applications of TCP
* World Wide Web (WWW) : When you browse websites, TCP ensures reliable data transfer between your browser and web servers.
* Email : TCP is used for sending and receiving emails. Protocols like SMTP (Simple Mail Transfer Protocol) handle email delivery across servers.
* File Transfer Protocol (FTP) : FTP relies on TCP to transfer large files securely. Whether you’re uploading or downloading files, TCP ensures data integrity.
* Secure Shell (SSH) : SSH sessions, commonly used for remote administration, rely on TCP for encrypted communication between client and server.
* Streaming Media : Services like Netflix, YouTube, and Spotify use TCP to stream videos and music. It ensures smooth playback by managing data segments and retransmissions.
#### Advantages of TCP
* It is reliable for maintaining a connection between Sender and Receiver.
* It is responsible for sending data in a particular sequence.
* Its operations are not dependent on Operating System .
* It allows and supports many routing protocols.
* It can reduce the speed of data based on the speed of the receiver.
#### Disadvantages of TCP
* It is slower than UDP and it takes more bandwidth.
* Slower upon starting of transfer of a file.
* Not suitable for LAN and PAN Networks.
* It does not have a multicast or broadcast category.
* It does not load the whole page if a single data of the page is missing.

##  What is User Datagram Protocol (UDP)?
UDP is a Transport Layer protocol. UDP is a part of the Internet Protocol suite, referred to as the UDP/IP suite. Unlike TCP, it is an unreliable and connectionless protocol. So, there is no need to establish a connection before data transfer. The UDP helps to establish low-latency and loss-tolerating connections establish over the network. The UDP enables process-to-process communication.

**Application of UDP**
* Real-Time Multimedia Streaming : UDP is ideal for streaming audio and video content. Its low-latency nature ensures smooth playback, even if occasional data loss occurs.
* Online Gaming : Many online games rely on UDP for fast communication between players.
* DNS (Domain Name System) Queries : When your device looks up domain names (like converting “www.example.com” to an IP address), UDP handles these requests efficiently .
* Network Monitoring : Tools that monitor network performance often use UDP for lightweight, rapid data exchange.
* Multicasting : UDP supports packet switching, making it suitable for multicasting scenarios where data needs to be sent to multiple recipients simultaneously.
* Routing Update Protocols : Some routing protocols, like RIP (Routing Information Protocol), utilize UDP for exchanging routing information among routers.

 #### Where TCP is Used?
* Sending Emails
* Transferring Files
* Web Browsing
#### Where UDP is Used?
* Gaming
* Video Streaming
* Online Video Chats

  ### Difference Between TCP and UDP :
  
| **Basis**                   | **TCP**                                                                                                                                                          | **UDP**                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Type of Service**         | TCP is a connection-oriented protocol. Connection needs to be established before transmission and closed after data is transmitted.                              | UDP is a datagram-oriented protocol, efficient for broadcast and multicast. No need to establish or close a connection.      |
| **Reliability**             | TCP is reliable as it guarantees data delivery to the destination router.                                                                                         | UDP does not guarantee data delivery to the destination.                                                                     |
| **Error Checking Mechanism**| TCP provides extensive error-checking with flow control and data acknowledgment.                                                                                  | UDP has basic error-checking using checksums only.                                                                           |
| **Acknowledgment**          | An acknowledgment segment is present in TCP.                                                                                                                     | No acknowledgment segment in UDP.                                                                                            |
| **Sequence**                | TCP sequences data so packets arrive in order at the receiver.                                                                                                   | UDP has no sequencing; if order is required, it must be managed by the application layer.                                    |
| **Speed**                   | TCP is comparatively slower than UDP.                                                                                                                            | UDP is faster, simpler, and more efficient than TCP.                                                                         |
| **Retransmission**          | Retransmission of lost packets is possible in TCP.                                                                                                               | No retransmission of lost packets in UDP.                                                                                    |
| **Header Length**           | TCP has a variable-length header (20-60 bytes).                                                                                                                  | UDP has a fixed-length header (8 bytes).                                                                                     |
| **Weight**                  | TCP is considered heavy-weight.                                                                                                                                  | UDP is lightweight.                                                                                                          |
| **Handshaking Techniques**  | TCP uses handshaking methods like SYN, ACK, and SYN-ACK.                                                                                                         | UDP is connectionless and does not use handshakes.                                                                           |
| **Broadcasting**            | TCP does not support broadcasting.                                                                                                                               | UDP supports broadcasting.                                                                                                   |
| **Protocols**               | TCP is used by HTTP, HTTPS, FTP, SMTP, and Telnet.                                                                                                               | UDP is used by DNS, DHCP, TFTP, SNMP, RIP, and VoIP.                                                                         |
| **Stream Type**             | TCP operates as a byte stream.                                                                                                                                   | UDP operates as a message stream.                                                                                            |
| **Overhead**                | TCP has a low overhead, but it’s higher than UDP.                                                                                                                | UDP has very low overhead.                                                                                                   |
| **Applications**            | TCP is suitable for applications requiring reliable and secure communication, such as email, web browsing, and military services.                               | UDP is used where quick communication is needed, and reliability is not critical, such as in VoIP, gaming, and streaming.    |

