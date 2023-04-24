# Ch2 Network Models

## Contents

PART 1: Overview

- Chapter 2 Network Models

    - 2.1 Protocol Layering

        - 2.1.1 Scenarios

        - 2.1.2 Principles of Protocol Layering

        - 2.1.3 Logical Connections

    - 2.2 TCP/IP Protocol Suite

        - 2.2.1 Layered Architecture

        - 2.2.2 Layers in the TCP/IP Protocol Suite

        - 2.2.3 Description of Each Layer

        - 2.2.4 Encapsulation and Decapsulation

        - 2.2.5 Addressing

        - 2.2.6 Multiplexing and Demultiplexing

    - 2.3 The OSI Model

        - 2.3.1 OSI versus TCP/IP

        - 2.3.2 Lack of OSI Models's Success

## 2.5 Practice set

### 2.5.1 Quizzes

#### 4~6

- application layer protocol은 Hypertext Transfer Protocol (HTTP), Simple Mail Transfer Protocol (SMTP), File Transfer Protocol (FTP), Terminal Network (TELNET), Secure Shell (SSH), Simple Network Management Protocol (SNMP), Domain Name System (DNS), Internet Group Management Protocol (IGMP) 등이 있다.

- transport layer protocol은 Transmission Control Protocol (TCP), User Datagram Protocol (UDP), Stream Control Transmission Protocol (SCTP) 등이 있다.

- network layer protocol은 Internet Protocol (IP), Internet Control Message Protocol (ICMP), Internet Group Management Protocol (IGMP), Dynamic Host Configuration Protocol (DHCP), Address Resolution Protocol (ARP) 등이 있다.

#### 10

|Packet names|Layers|Addresses|
|-|-|-|
|Message|Application layer|Names|
|Segment/User datagram|Transport layer|Port numbers|
|Datagram|Network layer|Logical addresses|
|Frame|Data-link layer|Link-layer addresses|
|Bits|Physical layer| |

#### 12

- The transport layer is responsible for the delivery of a message from one process to another.

#### 13

- The Internet Protocol (IP) is an unreliable and a connectionless protocol.

#### 15~16

- In TCP/IP, a message at the application layer is encapsulated in a packet at the transport layer.

- In TCP/IP, a message at the transport layer is encapsulated in a packet at the network layer.

#### 17~18

- In TCP/IP, a message belonging to the network layer is decapsulated from a packet at the data-link layer.

- In TCP/IP, a message belonging to the transport layer is decapsulated from a packet at the network layer.

#### 21

|Layer 5|Application|
|Layer 4|Transport|
|Layer 3|Network|
|Layer 2|Data link|
|Layer 1|Physical|

- In TCP/IP, a packet at the third layer carries data belonging to the fourth layer and the header belonging to the third layer.

### 2.5.2 Questions

#### 1

- 각 layer는  각 방향으로 하나씩 두 개의 반대 작업을 수행할 수 있어야 한다.

- To make the communication bidrectional, each layer needs to be able to provide two opposit tasks, one in each direction.

#### 2

- physical layer, data-link layer

#### 3

- a 3개, b 3개, c 1개

#### 4

- messages

#### 5

##### a

- message

##### b

- datagram

##### c

- frame

#### 6

- b

#### 7

- c

#### 8

- b

#### 9

- HTTP, SMCP, FTP, TELNET, SSH, SNMP, DNS, IGMP

#### 10

- transport layer header는 source, destination port number를 포함해야 하므로 최소 4 bytes는 되어야 한다.

#### 11

##### a

- names

##### b

- logical addresses

##### c

- link-layer addresses

#### 12

- multiplexing은 한 layer의 하나의 protocol이 여러 next-higher layer protocol에서 하나의 packet을 encapsulate할 수 있음을 의미하고, demultiplexing은 하나의 protocol이 하나의 packet을 decapsulate하고 여러 next-higher layer protocol로 전달할 수 있음을 의미한다.

- 따라서 multiplexing과 demultiplexing은 하나의 packet에 대해서 작용하므로 여러 message를 하나의 packet에 결합할 수는 없다.

#### 13

- application layer는 최상위 layer이므로 서비스를 제공할 layer가 없다. 따라서 multiplexing, demultiplexing은 application layer에 존재하지 않는다.

#### 14

- link-layer switch는 두 개 이상의 link를 연결할 때 사용하는 데 이 경우 link가 하나만 있으므로 필요하지 않다.

#### 15

- router는 두 개 이상의 link를 연결할 때 사용하는데 이 경우 link가 하나만 있으므로 필요하지 않다.

### 2.5.3 Problems

#### 1

##### a

- Layer 1 takes the ciphertext from layer 2, inserts (encapsulates) it in an
envelope and sends it.

##### b

- Layer 1 receives the mail, removes (decapsulates) the ciphertext from the
envelope and delivers it to layer 2.

#### 2

##### a

- layer 3에서 받은 plaintext를 encrypt하여 layer 1에게 전달한다.

##### b

- layer 1에서 받은 ciphertext를 decrypt하여 layer 3에게 전달한다.

#### 3

- 약 $3,096 * 10^6$개이다.

#### 4

- ${100 \over 150} = 0.6667$

#### 5

- The advantage of using large packets is less overhead. When using large packets, the number of packets to be sent for a huge file becomes small. Since we are adding three headers to each packet, we are sending fewer extra bytes than in the case in which the number of packets is large.

- The disadvantage manifests itself when a packet is lost or corrupted during the transmission; we need to resend a large amount of data.

#### 6

##### a

- data-link layer, network layer

##### b

- physical layer

##### c

- application layer

#### 7

##### a

- transport layer

##### b

- data-link layer

##### c

- physical layer

#### 8

- A protocol has a field in its header to identify to which protocol the encapsulated packets belong.

#### 9

- The following shows the situation. If we think about multiplexing as many-to-one and demultiplexing as one-to-many, we have demultiplexing at the source node and multiplexing at the destination node in the data-link layer. However, some purists call these two inverse multiplexing and inverse demultiplexing.

![P02-09](/images/P02-09.png)

#### 10

- application layer에서 encrypt, decrypt하는 protocol을 추가할 수 있으므로 별도의 layer를 추가하지 않아도 된다.

#### 11

![P02-11](/images/P02-11.png)

#### 12

- application layer 바로 아래에 둔다.

#### 13

- The only two layers that need to be changed are the data-link layer and the physical layer. The new hardware and software need to be installed in all host, routers, and link-layer switches. As long as the new data-link layer can encapsulate and decapsulate datagrams from the network layer, there is no need to change any protocol in the upper three layers. This is one of the characteristics of the protocol layering.

#### 14

- UDP가 제공하는 서비스와 TCP가 제공하는 서비스가 다르기 때문에 변경해야 한다.

#### 15

- The following shows the layers and the flow of data. Note that each host is involved in five layers, each switch in two layers, and each router in three layers. 

![P02-15](/images/P02-15.png)
