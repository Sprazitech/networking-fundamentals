# Summarizing the OSI model, IP addressing calculations, and TCP/IP analysis.

**1. explaining the OSI model layers with real-world examples for each layer.**

case study is Lagos to Accra: Sending an Email for tourist Adventure Through the OSI Model.

**1. The Application Layer (Layer 7):** Our adventure begins with the email client, Outlook—using SMTP (Simple Mail Transfer Protocol) to draft the message. Think of this as the email putting on its business suit, ready for international travel.

**2. The Presentation Layer (Layer 6):** Before departure, the email needs a little makeover. This layer handles formatting and encryption, ensuring the email not only looks sharp but also stays safe from prying eyes.

**3. The Session Layer (Layer 5):** Now, it’s time to book a session between Lagos and Accra. This layer sets up and manages the connection between the sender’s email server and the recipient’s. It’s like keeping a phone call active just long enough to get all the juicy gossip (or, in this case, data) across.

**4. The Transport Layer (Layer 4):** The email is too big to travel in one piece, so the Transport Layer chops it into neat little packets. TCP (Transmission Control Protocol) steps in as the overly cautious travel guide, ensuring every packet boards the right digital plane—and in the correct order, too.

**5. The Network Layer (Layer 3):** With the packets packed and labeled with source and destination IP addresses, they embark on a multi-hop journey across networks. Routers and switches act as tour guides, ensuring the packets stay on the best path to Acccra.

**6. The Data Link Layer (Layer 2):** Here, the packets are handled at a more local level, using MAC addresses to navigate through local networks. This layer is like a regional guide, correcting any missteps and keeping everything on track.

**7. The Physical Layer (Layer 1):** Finally, the data is transformed into electrical signals. It zips through fiber-optic cables beneath the Atlantic Ocean—talk about a deep-sea adventure!

**The Accra Landing:**

When the email arrives in Accra, it goes through customs in reverse:

**Physical Layer:** Signals are turned back into data packets.

**Data Link Layer:** Reassembles the packets and checks for errors.

**Network Layer:** Confirms all packets have made it safely.

**Transport Layer:** Reorders packets if needed, making sure nothing is lost in translation.

**Session Layer:** Keeps the connection steady until the entire email is received.

**Presentation Layer:** Decrypts and formats the email for easy reading.

**Application Layer:** Finally, the email pops up in the recipient’s inbox, ready to be read—perhaps over a cup of tea.

**2. Using subnetting calculator to calculate 1 subnet for the following IP range**

**1. IP Address: 9.4.3.47**

Default Class: Class A
Default Subnet Mask: 255.0.0.0 (/8)
Subnet Range:
Network Address: 9.0.0.0
First Usable IP: 9.0.0.1
Last Usable IP: 9.255.255.254
Broadcast Address: 9.255.255.255
Host Capacity: 16,777,214

**2. IP Address: 151.10.13.55**
   
Default Class: Class B
Default Subnet Mask: 255.255.0.0 (/16)
Subnet Range:
Network Address: 151.10.0.0
First Usable IP: 151.10.0.1
Last Usable IP: 151.10.255.254
Broadcast Address: 151.10.255.255
Host Capacity: 65,534

**3. IP Address: 203.42.62.1**
   
Default Class: Class C
Default Subnet Mask: 255.255.255.0 (/24)
Subnet Range:
Network Address: 203.42.62.0
First Usable IP: 203.42.62.1
Last Usable IP: 203.42.62.254
Broadcast Address: 203.42.62.255
Host Capacity: 254


**3. short analysis of how the TCP/IP protocol suite operates across layers in a real-world scenario**

 The TCP/IP protocol suite facilitates the communication between the client and the web server through its four layers:

**1. Application Layer:**
The browser operates at this layer using the HTTP/HTTPS protocol. It sends a request to access the web page by generating an HTTP GET request. This request is then passed to the Transport Layer.

**2. Transport Layer:**
The Transmission Control Protocol (TCP) takes over, establishing a reliable connection between the client and the server through a three-way handshake. TCP breaks the HTTP request into segments, assigns sequence numbers, and manages flow control and error checking to ensure data integrity.

**3. Internet Layer:**
The Internet Protocol (IP) is responsible for addressing and routing the data. The segments from the Transport Layer are encapsulated into IP packets, with the source and destination IP addresses included. The Domain Name System (DNS) may also come into play here, translating the domain name (www.example.com) to its corresponding IP address.

**4. Network Access Layer:**
This layer is sometimes called the Link Layer. It handles the physical transmission of data. The IP packets are further encapsulated into frames with MAC addresses for the physical hardware (e.g., the network interface card). The data is then transmitted over the physical medium (e.g., Ethernet, Wi-Fi) to the server.

**On the Server Side:**
The server receives the data through the same layered approach but in reverse. It reconstructs the HTTP request, processes it, and sends back the web page data through the same TCP/IP layers to the client's browser.

**And finally,**
The browser receives the data, reassembles it, and renders the web page for the user to see.


