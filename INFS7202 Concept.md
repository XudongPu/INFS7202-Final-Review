## Short Answer Questions



### Web Information System --- General concept

- ##### What is information?

  When data are processed, interpreted, organized, structured or presented so as to make them meaningful or useful, they are called information 

- ##### What is a system?

  A set of components that interact to accomplish some purpose

- ##### What is an information System?

  Any combination of information technology and people's activities that support operations or management.

- ##### What is Web information system?

  Web information system, or web based system, is a system that can deliver information or services by using internet web technologies to users or other systems / applications.

  It is a software system whose main purpose is to publish and maintain data by using hypertext-based principles.

- ##### What are two major types of Web information system?

  - Informational
    - Disseminate information(static or dynamic)
    - Share information(visitors or WISs)
  - Transactional
    - Conduct transactional business(B2C, C2C)
    - Perform tasks

- ##### Briefly describe the three-tier WIS architecture

  The three-tier WIS architecture includes client, application server and database server.

  The main purpose of each tier is summarized as follows:

  - Client --- user interface, how data is presented to users and the interaction between user and Web
  - Application server --- it implements the business rules and coordinates business process
  - Database server --- data storage and manipulation

- ##### Describe the advantages of three-tier architecture

  - The three-later architecture is more robust, scalable and maintainable
    - Easy to maintain: each tier is independent
    - High performance: because the presentation tier can cache requests, network utilization is minimized, and the load is reduced on the application and data tiers.
    - Scalability: each tier can scale horizontally. For example, the application server can be deployed on many machines.
    - Improved security: users have no direct access to the database.

- ##### Describe the disadvantage of three-tier architecture

  - Increase complexity / effort

- ##### What are the Caching requests?

  The performance of web sites and applications can be significantly improved by reusing previously fetched resources.

- ##### What is a Web?

  A hypermedia-based system that provides a simple 'point and click' means of browsing information on the internet using hyper links.

  - Web servers and clients
  - Documents are written in HTML
  - Servers and clients communicate via HTTP
  - Documents and locations are identified using URL

- ##### What are Web Browsers?

  A client side software to request, receive and process web pages from a Web Server (IE, Mozilla, FireFox, Chrome)

- ##### What is the Web Server Software?

  Web servers are programs that provide documents to browsers

  - Documents -- requested as resources (thus, dynamic results)
  - Stateless -- a request is independent of each other, even when they are from the same client
  - Apache HTTP Server: open source; completely free; supports Linux, Unix, Windows, Mac OS
  - Microsoft Internet Information Server(IIS): closed, proprietary, supports windows and bundled with Windows

- ##### What is a Network?

  A network consists of two or more computers connected for the purpose of communicating and sharing resources.

  - Sever computers
  - Client computers
  - Shared devices such as printers
  - Networking devices

- ##### What are Clint-Server Communication models?

  Clients initiate the communication by requesting a document on a Web Server

  <img src="/Users/puxd/Library/Application Support/typora-user-images/image-20200630145257521.png" alt="image-20200630145257521" style="zoom:50%;" />

  - Server side scripting technologies

  ![Screen Shot 2020-06-30 at 2.55.59 PM](/Users/puxd/Desktop/Screen Shot 2020-06-30 at 2.55.59 PM.png)

  - Client side technologies
    - Dominated by HTML / CSS / DOM / JavaScript / Ajax
  - Motivation
    - Utilization of client-side resources to save bandwidth and server-side load
    - Key consideration: client-side computing power



### Web Security --- General concept and workflow

- ##### Transmit information over the Internet

  - **Privacy** It is accessible to the sender and the receiver only
  - **Integrity** It cannot be changed during transmission
  - **Authenticity** the receiver can be sure it came from the sender
  - **Non-fabrication** the sender can be sure the receiver is genuine
  - **Non-repudiation** the sender cannot deny he sent it

  Security is beyond transmission and protection required for the clients as well as the servers

  - ##### Technologies

    - Firewall
    - Digital certificates and signatures
    - SSL(Secure Socket Layer)

## Definitions

- **Protocol** --- set of rules / agreements in telecommunications

- **Internet protocol suite(TCP/IP)** --- a family of communication protocols used to connect computer

  ##### The TCP/IP architectural model has four abstraction layers

  - **Application (process-to-process) layer**: HTTP, SOAP, IMAP, ...

    Creates and communicate data to other processes or applications

    - **HTTP** --- HyperText Transfer Protocol

      HTTP is the protocol used to transfer Web pages through the Internet at application layer

      - One protocol for the entire Web
      - Stateless connection: the server has no memory of previous ones(i.e., a request is closed once responded)

    - **FTP** --- File Transfer Protocol

      Transfer files from one machine to the other

    - **SMTP** --- Simple Mail Transport Protocol

      Email delivery

    - **Telnet Protocol** — Open telnet session

      Remote login

    - **SOAP** --- Simple Object Access Protocol

  - **Transport (host-to-host) layer**: TCP, UDP, DCCP, ...

    Deals with opening and maintaining connections, provides end-to-end communication services for applications

    **Reliable data delivery**

    Using acknowledgements and retransmissions to ensure reliable delivery

    - **TCP** — Transmission Control Protocol

      A reliable connection-oriented transport service that provides end-to-end reliability, resequencing, and flow control

    - **UDP** --- User Datagram Protocol

      A connectionless ("datagram") transport service

    - **DCCP** --- Datagram Congestion Control Protocol

  - **Internet/Network layer**: IPv4 (32-bit), IPv6 (128-bit), ...

    Moves data packets from node to node

    Route the data

    - **IP** --- Internet Protocol

    In order to route the data, we need two information:

    - IP Address (like your home address)

      - Logical address
      - In the following form: xxx.xxx.xxx.xxx (130.102.82.67)
      - Identify the physical location of the computer
        - In UQ domain, all computers are :130.102.xxx.xxx

    - Media Access Control (MAC) Address (like your passport) --- DATA LINK Layer(@TODO)

      - Physical address
      - The identity of the network card
      - All network cards in the world have DIFFERENT MAC Address
        - IEEE standard

    - **DNS** --- domain name systems

      - How to visit a website?
        - Human access information online through domain names
        - Web browsers interact through IP address
      - DNS is the phonebook of Internet
        - DNS Translates domain names to IP addresses
        - Web Browsers can load the targeted pages

    - How to find your IP address and MAC address?

      `Ifconfig /all`

    **Internal and external IP addresses**

    ![Screen Shot 2020-06-30 at 5.00.15 PM](/Users/puxd/Library/Application Support/typora-user-images/Screen Shot 2020-06-30 at 5.00.15 PM.png)

    - Connect your computer straight to the Internet --- your computer is assigned the external IP address
    - Your computer connects to a router --- you will get an internal IP and your router will get the external IP address
    - In UQ, every computer has a different internal IP address as they are on the same network. They share the same external IP.

  - **Link layer**: ARP, RARP, MAC, ...

    Describes local network topology and the interfaces

    - **MAC** --- Media Access Control

    - **ARP** --- Address Resolution Protocol
    - **RARP** --- Reverse Address Resolution Protocol

  - **Example**
    - Browsers and servers use TCP/IP to connect to the Internet
    - A browser uses TCP/IP to access a server. Server uses TCP/IP to send HTML back to a browser.
    - Email program uses TCP/IP to connect to the Internet in order to send and receive emails.
    - Internet address "130.102.158.15" is a part of the standard TCP/IP protocol

- **HTML** --- HyperText Markup Language

- **Sass** --- Sass is the most mature, stable, and powerful professional grade CSS extension language in the world

- **URL** --- Uniform Resource Locator

  URL is a string of alphanumeric and characters that uniquely represents the location or address of a resource on the Internet and how that resource should be accessed

  - Syntax
    - <protocol>://<host>[:<port>]/path_to_document[?Arguments]
      - e.g., http://www.itee.uq.edu.au/...
    - Protocols: http, file, mailto, ftp, ...
    - Path: complete or partial, depending on web server configuration
    - Many characters, such as [ ] [,] [;] [&] cannot be used

- **Tier** --- physical separation

- **Layer** --- logical separation

- **Cache** --- Caching is a technique that stores a copy of a given resource and serves it back when requested

  **Advantages**

  - By making use of HTTP caching, Web sites become more responsive

    - Reuse previously fetched resources
    - Reduce network traffic
    - Lessen the time needed to display a representation of a resource

  - Private Cache

    - A browser cache holds all documents dowloaded via HTTP by the user. This cache is used to make visited documents available for back/forward navigation, saving, viewing-as-source, etc. without requiring an additional trip to the server

  - Freshness

    - Cache eviction --- Once a resource is stored in a cache ...
      - Theoretically permanent ... periodically removed from storage
    - Resource updated
      - **Before** this expiration time, the resource is fresh
      - **After** the expiration time, the resource is stale
      - Eviction algorithms often privilege fresh resources over stale resources

  - Cache Validation

    Verify the status of the stale resources before using it and expired ones should not be used

  - How to control HTTP caching?

    - By default, a response is cacheable

    - HTML Meta Tag! --- controlling Browser Cache

      `<meta http-equiv="Cache-Control" content="max-age=7200"/>`

      `<meta http-equiv="Expires" content="Mon, 20 Jul 2019 23:00:00 GMT"/>`

    - no-cache: revalidate with server --- A cache will send the request to the origin server for validation before releasing a cached copy.

    - no-store: do not cache --- prevents storage of the representation in any form of cache whatsoever max-age: a cached response is acceptable if its age is no greater than the specified time in seconds

