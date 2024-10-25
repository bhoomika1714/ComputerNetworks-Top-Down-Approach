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

# HTTP Messages: Requests and Responses

HTTP (Hypertext Transfer Protocol) enables communication between clients (e.g., web browsers) and servers, exchanging data across the web. HTTP messages are divided into **requests** (sent by the client to the server) and **responses** (sent by the server to the client).

---

## 1. HTTP Message Structure

HTTP messages contain three main parts:
- **Request Line / Status Line**
- **Headers**
- **Body** (optional)

Each HTTP request and response follows this structure, though not all parts are required for every message.

---

## 2. HTTP Request

An HTTP request initiates an action from the client to the server. It includes:

### a. Request Line
- **Method**: Specifies the action, e.g., `GET`, `POST`, `PUT`, `DELETE`.
- **URL**: Specifies the location or endpoint of the resource.
- **HTTP Version**: Indicates the HTTP version used (e.g., HTTP/1.1 or HTTP/2).

   **Example**:


### b. Headers
Headers provide additional information about the request or client in key-value pairs.

**Common Headers**:
- **Host**: Specifies the server domain (e.g., `Host: www.example.com`).
- **User-Agent**: Identifies the client (e.g., browser).
- **Accept**: Lists acceptable MIME types (e.g., `Accept: text/html`).
- **Content-Type**: Specifies the body format for data (e.g., `Content-Type: application/json` for POST requests).

**Example**:

### c. Body
The body contains data sent to the server, present in requests like `POST`, `PUT`, or `PATCH`.

**Example (POST form data)**:

---

## 3. HTTP Response

HTTP responses are server replies to client requests, containing:

### a. Status Line
- **HTTP Version**: Version used by the server (e.g., HTTP/1.1).
- **Status Code**: Indicates the request result.
- **Status Message**: Brief message describing the status code.

**Common Status Codes**:
- **200 OK**: Successful request.
- **301 Moved Permanently** :requested object moved, new location specified later in this message (in Location: field)
-**400 Bad Request** :request msg not understood by server
- **404 Not Found**: Resource could not be found.
- **500 Internal Server Error**: Server error.
- **505 HTTP Version Not Supported**:

**Example**:

### c. Body
Contains the requested content (e.g., HTML, JSON, XML, images).

---

## 4. HTTP Methods

HTTP provides several methods, each with a specific purpose. Here are the most commonly used ones:

| **Method** | **Description** |
|------------|-----------------|
| **GET**    | Requests data from the server at the specified URL. |
| **POST**   | Sends data to the server, often for form submissions or uploads. |
| **PUT**    | Updates a resource on the server at a specified URL. |
| **DELETE** | Deletes the specified resource. |
| **HEAD**   | Similar to GET, but retrieves headers only (not the body). |
| **OPTIONS**| Describes the communication options for the target resource. |

---

## 5. HTTP Versions

- **HTTP/1.0**: Opens a new TCP connection for each request, inefficient for multiple requests.
- **HTTP/1.1**: Supports persistent connections, allowing multiple requests over a single connection.
- **HTTP/2**: Introduces multiplexing (multiple requests over a single connection simultaneously) for better performance.
- **HTTP/3**: Uses QUIC instead of TCP, reducing latency and enhancing reliability.

---

## 6. Persistent vs. Non-Persistent HTTP

| **Persistent HTTP**                                                                                     | **Non-Persistent HTTP**                                                             |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| The server leaves the connection open after sending a response.                                         | Requires 2 RTTs (Round-Trip Times) per object.                                      |
| Subsequent HTTP messages between the same client/server are sent over an open connection.               | OS incurs overhead for each TCP connection.                                         |
| The client sends requests as soon as it encounters a referenced object.                                 | Browsers often open parallel TCP connections to fetch referenced objects.           |
| Only one RTT is needed for all referenced objects after connection setup.                               | At most one object can be sent over a single TCP connection.                        |

---

## 7. HTTP Status Codes Categories

HTTP status codes are divided into five categories:

| **Category** | **Range**      | **Description**                                |
|--------------|----------------|------------------------------------------------|
| **1xx**      | 100-199        | Informational responses.                       |
| **2xx**      | 200-299        | Success - action successfully received and accepted. |
| **3xx**      | 300-399        | Redirection - further action is required.      |
| **4xx**      | 400-499        | Client Error - bad syntax or cannot fulfill the request. |
| **5xx**      | 500-599        | Server Error - server failed to fulfill a valid request. |

---

## 8. Example of an HTTP Request and Response

### Example HTTP Request (GET Request)

### 2.3.3 Cookies

- There are situations where web sites need to identify users, for security or personalization purposes. HTTP uses cookies to achieve user identification and tracking.
- Cookies have four components: a `cookie header` in HTTP `response` and `request` messages, a `cookie file` on the user's end system, and a `back end database` on the web site.

<img src="https://lh3.googleusercontent.com/pw/ADCreHfFwZxxD_q6lNIW4MotRBCCUUmdnTTAst3aa9ByyF1GoQxQGr9oMpd-3hudmL_VvIqWZhb9sF4Dsw3YYeV3N38qe-HBB9afByGpuvPj1gSfGeATqwiuckHdhRVluCOM_E_NXmqLYBN82wpku2x_BUd1=w1326-h1130-s-no" width="620" height="630">

- Cookies work by sending a unique identification number in a `Set-cookie` header from the server to the user's browser.
- The browser stores the identification number and sends it back to the server in a Cookie header with subsequent requests.
- Cookies are used to track user activity and offer personalized services, like shopping carts or recommendations.
- Users can be identified over multiple sessions by maintaining the same identification number in cookies.
- Cookies are controversial due to potential privacy concerns, as websites can gather and potentially sell user information.

### 2.3.4 Web Caching

- Web caches, or proxy servers, handle HTTP requests on behalf of origin servers.
- Caches store copies of requested objects, reducing the need to fetch them from the origin server.
- Users can configure browsers to direct requests through caches for faster responses.
- Caches serve as both servers (to clients) and clients (to servers) in the caching process.
- Installed by ISPs and institutions, caches enhance performance and lower bandwidth costs.
- Benefits include faster responses, reduced bandwidth upgrades, and decreased overall Internet traffic.
- Content Distribution Networks (CDNs) use distributed caching to localize content delivery.

> An HTTP request message is a so called conditional GET message if (1) the request message uses the GET method and (2) the request message includes an If-Modified-Since: header line.

- `Conditional GET` checks for freshness by comparing the `If-Modified-Since` header with object modification date.
- If an object hasn't changed, a `304 Not Modified response` allows the cache to serve the locally cached object.

> value of the If-modified-since: header line is exactly equal to the value of the Last-Modified: header line that was sent by the server initially.



# Web Caching Explained

Web caching is a technique used to **store copies of web resources** temporarily to reduce loading times, save bandwidth, and improve the overall performance of web applications. Caching helps deliver content faster by storing it close to the user, reducing the need to retrieve the same resources repeatedly from the original server.

---

## 1. What is Web Caching?

In a typical web request, a browser (client) makes a request to the server, which processes and returns the requested data. However, if the same resource (like an image, CSS file, or HTML page) is requested frequently, this process can slow things down. A **cache** saves a copy of the data, so when the client requests the same resource again, it can be quickly delivered from the cache instead of contacting the server.


## 3. How Web Caching Works

The caching process generally works as follows:

1. **Client Requests Resource**: The client requests a resource (e.g., an image or webpage).
2. **Cache Checks if Resource is Available**: The cache checks if a copy of the resource is already stored. If it is, the resource is delivered from the cache (a "cache hit").
3. **Cache Miss**: If the resource is not cached (a "cache miss"), the cache retrieves the resource from the origin server.
4. **Store in Cache**: The resource is stored in the cache for future requests.

---


## 6. Advantages and Disadvantages of Web Caching

### Advantages:
- **Improved Speed and Performance**: Cached resources are served faster.
- **Reduced Bandwidth and Costs**: Less data is transferred between server and client.
- **Less Load on Servers**: The origin server can handle more unique requests by reducing repeated requests.

### Disadvantages:
- **Stale Content**: Cached data might be outdated if not revalidated properly.
- **Inconsistent Data**: Users may see older versions of dynamic content.
- **Complexity in Management**: Configuring and managing caching rules can be complex, especially for frequently updated content.

---
#### Application Layer Protocol: SMTP
> A typical message starts its journey in the sender’s user agent, then travels to the sender’s mail server, and then travels to the recipient’s mail server, where it is deposited in the recipient’s mailbox. Reattempts are often done every 30 minutes

### 2.4.1 Email Components

- **User Agents:** Tools like Microsoft Outlook, Apple Mail, and Gmail, allowing users to manage emails.
- **Mail Servers:** The central infrastructure, hosting mailboxes for recipients like Bob.
- **SMTP (Simple Mail Transfer Protocol):** The principal protocol to send emails between servers.

### 2.4.2 SMTP Basics

- SMTP transfers messages between sender and recipient mail servers at `Port 25`.
- The client (sender's server) initiates a connection to the recipient's server via TCP.

### 2.4.3 Mail Message Structure

- Email messages consist of a `header` and a `body`.
- The header includes sender and recipient information, such as `"From," "To," and "Subject."`. The header lines and the body of the message are separated by a blank line (that is, by CRLF).
- These headers are distinct from SMTP commands used for server handshake communication.

```http
From: alice@crepes.fr
To: bob@hamburger.edu
Subject: Searching for the meaning of life.
```

### 2.4.4 Mail Access Protocols

<img src="https://lh3.googleusercontent.com/pw/ADCreHe0fyv4ULp_uamEsceCVVhVIa89gH-EYeg8F5QQ9MJOB6_HPfvS8QpwFXnBbpd_o5WBJf3SYSGt_KwkgMRBQ0BUtFHZP6lTTLAvPlWIfoypiutfj2fm5ZktaSNOuMKNcfdEXXH7OafVuFbqC-vIcfa4=w1876-h442-s-no" width="680" height="220">

> Bob’s user agent can’t use SMTP to obtain the messages because obtaining the messages is a pull operation, whereas SMTP is a push protocol.

- Users retrieve their email messages from a shared mail server using either HTTP or IMAP.
- HTTP is often used for web based email clients like Gmail, while IMAP is common with clients like Microsoft Outlook.
- Both the HTTP & IMAP approaches allow to manage folders, move messages to folders, delete messages, mark messages as important, and so on.

### Domain Name System (DNS) in Application Layer:
-

The Domain Name System (DNS) is like the internet’s phone book. It helps you find websites by translating easy-to-remember names (like www.example.com) into the numerical IP addresses (like 192.0.2.1) that computers use to locate each other on the internet. Without DNS, you would have to remember long strings of numbers to visit your favorite websites. It is an application layer protocol for message exchange between clients and servers. It is required for the functioning of the Internet.

-
### What is the Need for DNS?
Every host is identified by the IP address but remembering numbers is very difficult for people also the IP addresses are not static therefore a mapping is required to change the domain name to the IP address. So DNS is used to convert the domain name of the websites to their numerical IP address.

DNS translates domain names to IP addresses, making it an essential part of the internet.
-
**Types of Domain**
* Generic Domains: .com(commercial), .edu(educational), .mil(military), .org(nonprofit organization), .net(similar to commercial) all these are generic domains.
* Country Domain: .in (India) .us .uk
* Inverse Domain: if we want to know what is the domain name of the website. IP to domain name mapping. So DNS can provide both the mapping for example to find the IP addresses of geeksforgeeks.org then we have to type
```
nslookup www.geeksforgeeks.org
```
# DNS Services Explained

The **Domain Name System (DNS)** is a fundamental part of the internet infrastructure, providing various essential services that allow users and devices to connect easily using human-readable names. DNS translates these names into IP addresses, manages aliasing for efficiency, directs emails, and distributes server load for better performance.

---

## 1. Hostname-to-IP Address Translation

DNS is primarily responsible for **translating domain names** (hostnames) into **IP addresses**, which computers use to locate each other on a network. 

For example, if a user enters `www.example.com`, the DNS service will convert this hostname to an IP address, like `192.0.2.1`, so the request can reach the correct server. This service allows users to access websites without needing to remember complex numeric IP addresses.

---

## 2. Host Aliasing

Host aliasing allows a single **canonical (official) hostname** to have **multiple alias names**. 

### Example:
- Canonical name: `www.example.com`
- Aliases: `example.com`, `app.example.com`

Through aliasing, users can access the same website with different names, simplifying the user experience and branding. This way, `www.example.com` could be aliased to `example.com`, and users can reach the site by typing either name.

---

## 3. Canonical and Alias Names

- **Canonical Name (CNAME)**: The main, official hostname associated with an IP address.
- **Alias Name**: A secondary name that maps to the canonical name.

**Example**:
If `www.mycompany.com` is the canonical name, an alias like `shop.mycompany.com` might also be mapped to the same server, allowing both names to resolve to the same IP address.

The CNAME record in DNS allows users to create simple or branded names that refer to complex internal infrastructure without exposing that complexity directly to users.

---

## 4. Mail Server Aliasing

DNS supports email delivery by providing **mail server aliasing** using **Mail Exchange (MX) records**. These records direct email messages to the appropriate mail servers.

### Example:
When an email is sent to `user@example.com`, DNS checks for MX records associated with `example.com`. The MX records define which mail servers handle emails for the domain, directing the message to the correct server based on priority.

This flexibility allows organizations to use a single email domain across multiple mail servers or even use external email providers without changing the visible domain name.

---

## 5. Load Distribution

DNS also plays a crucial role in **distributing server load** by mapping a single domain name to multiple IP addresses. This process, often called **round-robin DNS**, helps balance the traffic load across multiple servers, which improves performance and availability.

### Example:
If `www.popularsite.com` has high traffic, it may use multiple IP addresses for different servers:
- `www.popularsite.com` -> `192.0.2.1`
- `www.popularsite.com` -> `192.0.2.2`
- `www.popularsite.com` -> `192.0.2.3`

When a user requests `www.popularsite.com`, the DNS server will cycle through these IP addresses, distributing requests across multiple servers to avoid overloading a single server.

---

## 6. Replicated Web Servers: Many IP Addresses Corresponding to One Name

**Replication** involves deploying multiple servers with identical content in various locations. DNS can point a single hostname to multiple servers, each with a unique IP address.

For example, large-scale websites like Google or Amazon replicate servers across different regions. When a user requests `www.amazon.com`, DNS can return the IP address of the server geographically closest to the user. This approach minimizes latency, speeds up access, and ensures better load distribution globally.

---

> gethostbyname() is the function call that an application calls in order to perform the translation.

* DNS operates through query and reply messages using UDP datagrams on port 53.
* DNS queries involve multiple servers globally distributed.
* A simple centralized design for DNS is not feasible due to scalability issues.
* Issues with centralized design: single point of failure, high traffic volume, distant database, and maintenance.
* DNS uses a hierarchical structure and a distributed database., to handle the vast number of hosts on the Internet.
  
### 2.5.2 Distributed, Hierarchical Database

<img src="https://lh3.googleusercontent.com/pw/ADCreHfjtoFE2ozufMyfFi_xvvvjhwhvWHxaFcgn2jVCEG50nQsaQlTqhQQovC1HaJrlB0h8La--jGtCdoz8c6RxZVLsou9ISfsTEy7uaS-fjCMZNBiZtfTPnFpbVbYUDbQ49wyFPKQJJNUc-_7h4wmYm2IX=w1920-h710-s-no" width="580" height="220">

- DNS uses three classes of servers: `Root` DNS servers, `top level domain (TLD)` DNS servers, and `authoritative` DNS servers.
- Root DNS servers provide IP addresses for TLD servers. TLD servers provide IP addresses for authoritative DNS servers Authoritative DNS servers store DNS records for specific organizations.
- A `local DNS server`, specific to an ISP, also plays a crucial role in DNS queries. It cache DNS information to reduce query traffic and improve performance.

> When a host makes a DNS query, the query is sent to the local DNS server, which acts a proxy, forwarding the query into the DNS server hierarchy.

- DNS extensively utilizes caching to enhance performance. These are stored temporarily and it allows DNS servers to quickly respond to subsequent queries for the same hostname.


# Recursive vs. Iterative DNS Queries

When a DNS client (like a web browser) needs to resolve a domain name, it performs a **DNS query** to find the corresponding IP address. DNS queries can be performed in two ways: **Recursive** and **Iterative**. Each method has its own characteristics, roles, and behavior in the domain resolution process.

---

## 1. Recursive DNS Queries

In a **recursive query**, the **DNS client relies entirely on a DNS resolver** to find the IP address for a domain. The resolver is responsible for querying other DNS servers on behalf of the client and returning the final IP address.

### How Recursive Queries Work:
1. The client sends a request for a domain (e.g., `www.example.com`) to the recursive resolver.
2. The recursive resolver queries various DNS servers on behalf of the client, following the hierarchy:
   - Root DNS servers
   - Top-Level Domain (TLD) DNS servers (like `.com` or `.org`)
   - Authoritative DNS server for the specific domain (`example.com`)
3. The resolver collects the IP address of the domain and returns it to the client.


---

## 2. Iterative DNS Queries

In an **iterative query**, the **DNS resolver does not do all the work** but instead responds with the address of the next DNS server in the hierarchy if it doesn’t know the answer. This shifts the responsibility back to the client to continue the query process.

### How Iterative Queries Work:
1. The client sends a request for a domain (e.g., `www.example.com`) to the DNS server.
2. If the DNS server doesn’t know the IP address, it returns the IP of the next DNS server (e.g., a root server).
3. The client then contacts the returned server (e.g., the TLD server for `.com`).
4. This process repeats until the client receives the final IP address from the authoritative DNS server for `example.com`.

<img src="https://lh3.googleusercontent.com/pw/ADCreHcDzbK4FY8RExEyQO82XsXu_OFQXOqMXfJx6q8TO_Tx4wYRJt9WaiktQr-4bF482giEXJmGfkLMszdS7Ufn_sjYphuuVOdpKVn7RI6laoHLFKiPUtFpU_kOUnZ_UJN7NjeJdt5Bp65KPlNKkiEpFrIF=w1708-h1044-s-no" width="780" height="520">

---

| Feature                   | **Recursive DNS Query**                                                                 | **Iterative DNS Query**                                                      |
|---------------------------|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| **Responsibility**        | The DNS resolver handles the entire process for the client.                             | The client handles the query process and contacts each DNS server iteratively. |
| **Load Distribution**     | Higher load on the DNS resolver due to the complete query resolution.                   | Lower load on individual DNS servers, as each only provides the next server.  |
| **Caching**               | DNS resolvers typically cache responses, improving efficiency on repeated queries.      | Caching is limited, as each query is managed individually by the client.      |
| **Number of Requests**    | The client only makes one request to the DNS resolver.                                  | The client makes multiple requests to different DNS servers.                  |
| **Response Time**         | Potentially faster due to caching and fewer requests.                                   | Can be slower due to multiple iterative queries.                              |
| **Client Complexity**     | Simplified for the client, which only needs one response from the resolver.             | More complex, as the client must manage multiple DNS server interactions.     |

---



## DNS Records

DNS records are database entries that provide key details for domain resolution. Each record type serves a specific purpose:
- **A (Address) Record**: Maps a domain name to an IPv4 address.
- **AAAA (IPv6 Address) Record**: Maps a domain name to an IPv6 address.
- **CNAME (Canonical Name) Record**: Points one domain to another, used for aliases.
- **MX (Mail Exchange) Record**: Directs emails to mail servers for a domain.
- **TXT (Text) Record**: Allows text-based information to be added, often for security verification like SPF and DKIM.

---

## DNS Protocol Messages

DNS uses protocol messages to resolve domain names, sent over UDP (usually) or TCP (if larger than 512 bytes). The key message types are:
- **Query**: Sent from a client to request the IP address for a domain.
- **Response**: Sent by DNS servers with the requested IP or an error if the domain is unresolved.
- **Update**: Used to add or delete records within a DNS zone.
- **Notification**: Alerts other DNS servers about changes to DNS records.

---

## Getting Your Info into the DNS

To add information (like domain records) into the DNS system, follow these steps:
1. **Register your domain** with a domain registrar (e.g., GoDaddy).
2. **Add DNS records** (A, CNAME, MX, etc.) through your DNS hosting provider’s dashboard.
3. **Propagation**: Changes propagate across global DNS servers, typically within 24-48 hours.

This information will then be available for clients querying your domain.

---

## DNS Security

DNS security is essential to prevent threats like **DNS spoofing** and **DDoS attacks**. Key security measures include:
- **DNSSEC (DNS Security Extensions)**: Adds a layer of authentication to DNS responses, preventing spoofing.
- **TLS and HTTPS**: Secure DNS communication channels (e.g., DoH, DNS over HTTPS).
- **Rate Limiting**: Protects against DDoS by limiting queries per IP.
- **Monitoring and Logging**: Tracks suspicious activity on DNS servers to quickly respond to security incidents.

