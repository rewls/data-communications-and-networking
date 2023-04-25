# Ch5 Analog Transmission

## Contents

PART 2: Physical Layer

- Chapter 5 Analog Transmission

    - 5.1 Digital-to-Analog Conversion

        - 5.1.1 Aspects of Digital-to-Analog Conversion

        - 5.1.2 Amplitude Shift Keying

        - 5.1.3 Frequency Shift Keying

        - 5.1.4 Phase Shift Keying

        - 5.1.5 Quadrature Amplitude Modulation

    - 5.2 Analog-to-Analog Conversion

        - 5.2.1 Amplitude Modulation (AM)

        - 5.2.2 Frequency Modulation (FM)

        - 5.2.3 Phase Modulation (PM)

## 5.4 Practice Set

### 5.4.2. Questions

#### 1

- Normally, analog transmission refers to the transmission of analog signals using a band-pass chnnel. Baseband digital or analog signals are converted to a complex analog signal with a range of frequencies suitable for the channel.

#### 2

- In analog transmission, the sending device produces a high-frequency signal that acts as a base for the information signal. This base  signal is called the carrier signal

#### 3

- Digital-to-analog conversion is the process of changing one of the characteristics of an analog signal based on the information in digital.

#### 4

##### a

- amplitude

##### b

- frequency

##### c

- phase

##### d

- amplitude and phase

#### 5

- Since noise can change the amplitude easier than it can change the phase or frequency, ASK is the most susceptible to noise.

#### 6

- A constellation Diagram can help us define the amplitude and phase of a signal element. It is useful when we are dealing with multilevel ASK, PsK, or QAM.

- The diagram has two axes. The horizontal X axis is related to the in-phase carrier; the verical Y axis is related to the quadrature carrier. For each point on the diagram, four pieces of information can be deduced. The projection of the point on the X axis defines the peak amplitude of the in-phase component; the projection of the point on the Y axis defines the peak amplitude of the quadrature component. The length of the line (vector) that connects the point to the origin is the peak amplitude of the signal element (combination of the X and Y components); the angle the line makes with the X axis is the phase of the signal element.

#### 7

- The two components of a signal is in-phase and quadrature components. In-phase component is shown on the horizontal axis and quadrature component is shown on the vertical axis.

#### 8

- Analog-to-analog conversion, or analog modulation, is the representation of analog information by an analog signal.

#### 9

##### a

- amplitude

##### b

- frequency

##### c

- phase

#### 10

- Since noise can change the amplitude easier than it can change the phase or frequency, AM is the most susceptible to noise.

### 5.4.3 Problems

#### 1

##### a

- For BFSK $r = \log_2 2 = 1$, $2,000 \cdot (1/1) = 2,000 \,\text{baud}$

- For ASK with more levels the baud rate is smaller than $2,000 \,\text{baud}$

##### b

- $r = \log_2 2 = 1$, $4,000 \cdot (1/1) = 4,000 \,\text{baud}$

- For ASK with more levels the baud rate is smaller than $2,000 \,\text{baud}$

##### c

- $r = \log_2 4 = 2$, $6,000 \cdot (1/2) = 3,000 \,\text{baud}$

##### d

- $r = \log_2 64 = 6$, $36,000 \cdot (1/6) = 6,000 \,\text{baud}$

#### 2

##### a

- For BFSK $r = \log_2 2 = 1$, $1,000 \cdot 1 = 1,000 \,\text{bps}$

- For FSK with more levels the bit rate is larger than $1,000 \,\text{bps}$

##### b

- For BASK $r = \log_2 2 = 1$, $1,000 \cdot 1 = 1,000 \,\text{bps}$

- For ASK with more levels the bit rate is larger than $1,000 \,\text{bps}$

##### c

- $r = \log_2 2 = 1$, $1,000 \cdot 1 = 1,000 \,\text{bps}$

##### d

- $r = \log_2 16 = 4$, $1,000 \cdot 4 = 4,000 \,\text{bps}$

#### 3

##### a

- $\log_2 4 = 2$

##### b

- $\log_2 8 = 3$

##### c

- $\log_2 4 = 2$

##### d

- $\log_2 128 = 7$

#### 4

##### a

```
      ^
      |
      |
------|-o---o-->
     0| 1   3
      |
```

##### b

```
      ^
      |
      |
--o---|---o-->
 -2   |   2
      |
```

##### c

```
sqrt(9/2)^
     o---|---o
     |   |   |
---------|--------->
     |   |   |
     o---|---o
         |
```

##### d

```
sqrt(9/2)^
   o-----|-----o
   |sqrt2|     |
   |   o | o   |
---------|--------->
   |   o | o   |
   |     |     |
   o-----|-----o
         |
```

#### 5

##### a

```
      ^
      |
      |
------|---o-o-->
     0|   2 3
      |
```

- BASK with peak amplitude values of 2 and 3

##### b

```
        ^
        |
        |
--o-----|-----o-->
 -3    0|     3
        |
```

- BPSK with peak amplitude value of 3

##### c 

```
      2^
   o---|---o
   |   |   |
-------|------->
 -2|   |   |2
   o---|---o
       |-2
```

- QPSK or 4-QAM with peak amplitude value of $2\sqrt{2}$

##### d

```
      ^
      o 2 
      |
------|------>
      |
      o-2
      |
```

- BPSK with peak amplitude value of 2

#### 6

##### a

- $\log_2 2 = 1$

##### b

- $\log_2 4 = 2$

##### c

- $\log_2 16 = 4$

##### d

- $\log_2 1024 = 10$

#### 7

##### a

- For BASK $S = N = 4,000$, $B = (1 + 1) \cdot 4,000 = 8 \,\text{kHz}$

- For ASK with more levels the bandwidth is smaller.

##### b

- For BFSK $S = N = 4,000$, $B = (1 + 1) \cdot 4,000 + 4,000 = 12 \,\text{kHz}$.

- For FSK with more levels the bandwidth is larger.

##### c

- $r = \log_2 4 = 2$, $S = 4,000 \cdot (1/2) = 2,000$, $B = (1 + 1) \cdot 2,000 = 4 \,\text{kHz}$

##### d

- $r = \log_2 16 = 4$, $S = 4,000 \cdot (1/4) = 1,000$, $B = (1 + 1) \cdot 1,000 = 2 \,\text{kHz}$

#### 8

##### a

- For BASK $r = \log_2 2 = 1$, $B = (1 + 0) \cdot N = 4 \,\text{KHz}$ , $N = 4 \,\text{kbps}$.

##### b

- $r = \log_2 4 = 2$, $B = (1 + 0) \cdot N \cdot (1/2) = 4 \,\text{KHz}$, $N = 8 \,\text{kbps}$

##### c

- $r = \log_2 16 = 4$, $B = (1 + 0) \cdot N \cdot (1/4) = 4 \,\text{KHz}$, $N = 16 \,\text{kbps}$

##### d

- $r = \log_2 64 = 6$, $B = (1 + 0) \cdot N \cdot (1/6) = 4 \,\text{KHz}$, $N = 24 \,\text{kbps}$

#### 9

- The bandwidth for each channel is $1 \,\text{MHz} / 10 = 100 \,\text{kHz}$.

- In QAM the bandwidth is $B = (1 + 0) \cdot 10 \,\text{Mbps} \cdot (1/\log_2 L) = 100 \,\text{kHz}$.

- $\log_2 L = 10$, $L = 2^{10} = 1,024$

- The minimum number of bits per baud is 10 and the number of points in the constellation diagram is 1024.

#### 10

- $r = \log_2 64 = 6$, $B = (1 + d) \cdot N \cdot (1/6) = 6 \,\text{MHz}$

- Supposing $d = 1$, $N = 18 \,\text{Mbps}$.

- The available data rate is at least $18 \,\text{Mbps}$.

#### 11

##### a

- $B = 2 \cdot 5 \,\text{KHz} = 10 \,\text{KHz}$

##### b

- $B = 2 \cdot (1 + 5) \cdot 5 \,\text{KHz} = 60 \,\text{KHz}$

##### c

- $B = 2\cdot (1 + 1) \cdot 5 \,\text{KHz} = 20 \,\text{KHz}$

#### 12

##### a

- $(1700 - 530)/10 = 117$

##### b

- $(108 - 88)/0.2 = 100$
