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

## Internet Applications and Transport Protocols :
| **Application**               | **Application Layer Protocol**                                    | **Transport Protocol**   |
|-------------------------------|-------------------------------------------------------------------|---------------------------|
| **File Transfer / Download**  | FTP [RFC 959]                                                    | TCP                       |
| **E-mail**                    | SMTP [RFC 5321]                                                  | TCP                       |
| **Web Documents**             | HTTP [RFC 7230, 9110]                                            | TCP                       |
| **Internet Telephony**        | SIP [RFC 3261], RTP [RFC 3550], or proprietary HTTP [RFC 7230], DASH | TCP or UDP               |
| **Streaming Audio / Video**   | HTTP [RFC 7230], DASH                                            | TCP                       |
| **Interactive Games**         | WOW, FPS (proprietary)                                           | UDP or TCP                |
### Application Layer Protocols :
Application layer protocols are those protocols utilized at the application layer of the OSI (Open Systems Interconnection) and TCP/IP models. They facilitate communication and data sharing between software applications on various network devices. These protocols define the rules and standards that allow applications to interact and communicate quickly and effectively over a network.
<br>


**HTTP (Hypertext Transfer Protocol):** Primarily used for web communications. It's a stateless protocol where a client (browser) requests resources from a server. HTTP/1.1 added persistent connections, and HTTP/2 introduced multiplexing to improve efficiency. HTTPS adds encryption for secure communication.

**Web Protocols (HTTP + HTML):** The Web relies on HTTP for transmitting resources, while HTML (HyperText Markup Language) structures content. Browsers use HTTP to fetch HTML and other resources, providing users with the interface for viewing and interacting with content.

**FTP (File Transfer Protocol):** Used for transferring files between client and server. It uses separate control and data connections, making it efficient for large file transfers.

**SMTP (Simple Mail Transfer Protocol):** The main protocol for sending emails. Works in tandem with POP3 or IMAP, which retrieve emails from the server.

**DNS (Domain Name System):** Translates human-readable domain names to IP addresses, enabling easier access to resources.

**POP3/IMAP:** These protocols allow users to retrieve emails from servers. IMAP supports syncing across multiple devices, while POP3 downloads messages to one device.

**Telnet/SSH:** Protocols for remote login to networked computers, where SSH offers encrypted connections, making it more secure than Telnet.

These protocols illustrate how the application layer facilitates user interaction with network services.  Primarily used for web communications. It's a stateless protocol where a client (browser) requests resources from a server. HTTP/1.1 added persistent connections, and HTTP/2 introduced multiplexing to improve efficiency. HTTPS adds encryption for secure communication.
##  Application Layer Protocol: Web and HTTP
- **HTTP**: `HTTP (HyperText Transfer Protocol)` is the primary application layer protocol of the World Wide Web. It relies on client and server programs that communicate by exchanging HTTP messages. Web pages are composed of objects, which are individual files with unique URLs.
- **Web Page Structure**: A web page typically includes a base HTML file and referenced objects like images, stylesheets, and videos. Objects are identified by URLs, which consist of a `hostname` and a `path name`.
- **HTTP and TCP**: HTTP uses TCP (Transmission Control Protocol) as its underlying transport protocol. Clients initiate TCP connections with servers to exchange HTTP messages.

> The HTTP client first initiates a TCP connection with the server. Once the connection is established, the browser and the server processes access TCP through their socket interfaces. 

> HTTP need not worry about lost data or the details of how TCP recovers from loss or reordering of data within the network. 

- **Stateless Protocol**: HTTP is a stateless protocol, meaning servers `don't store client specific information.` If a client requests the same object multiple times, the server doesn't remember previous requests.
- **HTTP Versions**: `HTTP/1.0` and `HTTP/1.1` are common versions, with HTTP/1.1 supporting persistent connections. Newer versions like HTTP/2 are also emerging.
### 2.3.1 Non Persistent and Persistent Connections 
- Non persistent connections create a new connection for each requested object. Persistent connections allow multiple objects to be sent over the same connection, improving efficiency.

> Although HTTP uses persistent connections in its default mode, HTTP clients and servers can be configured to use non persistent connections instead.

> round trip time (RTT), which is the time it takes for a small packet to travel from client to server and then back to the client. The RTT includes packet propagation delays, packet queuing delays in intermediate routers and switches, and packet processing delays.

<img src="https://lh3.googleusercontent.com/pw/ADCreHcP6O3E33NG7QnDmzX1ZUYsYN4WdmaGZSwLxO79aCwgpc2VRQI5lV8oSDjGyga6BN6nbLTnXzZnfZe49s3o9JvbZT35Z1vqiUG1c97LMJbYwZwMhTgBitpNwl5znilEEFnGID7QpG4z98mGuwdk6xPg=w1456-h1130-s-no" width="520" height="520">

- The three way handshake involves the client and server exchanging messages, taking one round trip time (RTT) for this process.
- After completing the handshake, the client sends an HTTP request message along with an acknowledgment into the TCP connection.
- The server responds by sending the HTML file over the established connection.
- The total response time is approximately two RTTs plus the transmission time for the HTML file.
  
### Difference between Persistent and Non-Persistent Connections
| **Persistent HTTP**                                                                                     | **Non-Persistent HTTP**                                                             |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| The server leaves the connection open after sending a response.                                         | Requires 2 RTTs (Round-Trip Times) per object.                                      |
| Subsequent HTTP messages between the same client and server are sent over an open connection.           | Operating system overhead for each TCP connection is incurred.                      |
| The client sends requests as soon as it encounters a referenced object.                                 | Browsers often open parallel TCP connections to fetch referenced objects.           |
| Only one RTT is needed for all referenced objects after the connection is established.                  | At most one object can be sent over a single TCP connection.                        |
