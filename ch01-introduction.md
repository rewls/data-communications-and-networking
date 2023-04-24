# Ch1 Introduction

## Contents

PART 1: Overview

- Chapter 1 Introduction

    - 1.1 Data Communications

        - 1.1.1 Components

        - 1.1.2 Data Representation

        - 1.1.3 Data Flow

    - 1.2 Networks

        - 1.2.1 Network Criteria

        - 1.2.2 Physical Structures

    - 1.3 Networks Types

        - 1.3.1 Local Area Network

        - 1.3.2 Wide Area Network

        - 1.3.3 Switching

        - 1.3.4 The Internet

        - 1.3.5 Accessing the Internet

    - 1.4 Internet History

        - 1.4.1 Early History

        - 1.4.2 Birth of the Internet

        - 1.4.3 Internet Today

    - 1.5 Standards and Administration

        - 1.5.1 Internet Standards

        - 1.5.2 Internet Administration

## 1.7 Practice set

### 1.7.1 Quizzes

#### 3

- RFC의 maturity level에는 proposed standard, draft standard, internet standard, historic, experimental, informational이 있다.

#### 5

- data communications system의 effectiveness는 다음 네 가지 특징에 따라 다르다: delivery, accuracy, timeliness, and jitter.

#### 8

- network criteria에는 performance, reliability, security가 있다.

#### 10

- connection의 type 중 point-to-point connection은 두 device 사이 dedicated link를 제공한다.

### 1.7.2 Questions

#### 1

- sender, receiver, message, transmission medium, protocol이다.

#### 2

- performance, reliability, security이다.

#### 3

- channel의 capacity를 공간적으로 또는 시간적으로 공유할 수 있어 여러 device를 쉽게 적은 비용으로 연결할 수 있다. 

#### 4

- point-to-point, multipoint이다.

#### 5

- mesh, star, ring은 point-to-point connection이고 bus는 multipoint connection이다.

#### 6

- half-duplex는 동시에 data를 보내고 받을 수 없지만, full-duplex는 할 수 있다.

#### 7

- mesh: 견고하다. fault identification과 fault isolation이 편리하다.

    1. each connection can carry its own data load

    2. robustness

    3. privacy or security

    4. easy fault identification and fault isolation

- star: mesh에 비해 installation과 reconfiguration이 편리하다. fault identification과 fault isolation이 편리하다.

    1. easy installation and reconfiguration

    2. robustness

    3. easy fault identification and fault isolation

- bus: installation이 편리하고 공간을 효율적으로 사용할 수 있다.

    - easy installation

- ring: installation과 reconfiguration이 편리하다. fault identification과 fault isolation이 편리하다.

    - easy installation and reconfiguration

    - easy fault isolation

#### 8

- mesh: ${n(n-1) \over 2}$

- ring: $n-1$

- bus: $1$

- star: $n$

#### 9

- size, geographical coverage, ownership, structure

#### 10

- internet은 두 개 이상의 network가 연결된 것이고, Internet는 수많은 network가 연결된 것이다.

#### 11

- sender와 reciever가 모두 따르는 규칙이 있어야 data communication이 이루어지기 때문이다.

#### 12

- data를 모든 host에게 보내지 않고 destination host에게만 보내기 위해 address가 필요하다.

#### 13

- ${n(n-1) \over 2}$

#### 14

- circuit-switched network이다.

#### 15

- telephone company가 ISP 역할을 하여 resident와 telephon company 사이를 point-to-point WAN으로 연결한다.

#### 16

- 2.5.2 Questions 1번

#### 17

- Internet draft는 working document with no official status and a six-month lifetime이다. Internet authorities의 추천을 받으면 draft는 Request for Comment (RFC)로 발행되어 proposed standard가 될 수 있다.

#### 18

- required RFC는 모든 Internet system에서 구현되어야 하는 것이고 recommended RFC는 유용하니까 구현을 권장하는 것이다.

#### 19

- IETF는 operational problem을 식별하고 해당 문제에 대한 해결책을 제시하는 데 책임이 있고 IRTF는 long-term research topics에 집중한다.

### 1.7.3 Problems

#### 1

- $2^{32}$

#### 2

- $2^{16}$

#### 3

- cable 15개가 필요하고 각 device에 port 5개가 필요하다.

#### 4

##### a

- 연결 실패한 device에 대한 연결을 제외하고 잘 연결된다.

##### b

- 연결 실패한 device에 대한 연결을 제외하고 잘 연결된다.

##### c

- backbone에서 문제가 생긴 경우 모든 연결이 실패하고 drop line에서 문제가 생긴 경우 해당 device에 대한 연결을 제외하고 잘 연결된다.

##### d

- 단방향 통신이기 때문에 한 device의 연결 실패는 모든 네트워크 연결 실패로 이어진다.

#### 5

- LAN이다. Ethernet hub는 LAN을 만든다.

#### 6

- 모든 연결이 작동하지 않는다.

#### 7

- backbone에서 drop line을 통해 station과 연결하기 때문에 drop line에 station이 연결되지 않아도 나머지는 작동한다.

#### 8

- Internet surfing은 사용자와 Internet간의 상호작용을 필요로 하므로 delay에 민감하다.

#### 9

- point-to-point connection이다. 두 지점 간에 dedicated line으로 연결되기 때문이다.

#### 10

- telephon network는 voice communication을 기본으로 하고 Internet은 다양한 data communication을 기본으로 한다. 둘다 수많은 network와 연결되어 있고 telephon network는 contiuous data communication이 필요하기 때문에 대부분 circuit-switched network를 사용하고 Internet은 대부분 보다 효율적인 packet-switch network를 사용한다.
