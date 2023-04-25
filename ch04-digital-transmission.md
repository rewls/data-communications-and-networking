# Ch4 Digital Trasmission

## Contents

PART 2: Physical Layer

- Chapter 4 Digital Transmission

    - 4.1 Digital-to-Digital Conversion

        - 4.1.1 Line Coding

        - 4.1.2 Line Coding Schemes

        - 4.1.3 Block Coding

        - 4.1.4 Scrambling

    - 4.2 Analog-to-Digital Conversion

        - 4.2.1 Pulse Code Modulation (PCM)

        - 4.2.2 Delta Modulation (DM)

    - 4.3 Transmission Modes

        - 4.3.1 Parallel Transmission

        - 4.3.2 Serial Transmission

## 4.5 Practice set

### 4.5.1 Quizzes

#### 3

- In polar schemes, the voltage level oscillates between a positive and a negative value although it may remain at zero level between the two values.

#### 12

- Differential Manchester encoding has a transition at the beginning of each 0 bit.

#### 16

- Block coding, line coding and scrambling are the process of converting digital data to a digital signal.

### 4.5.2 Questions

#### 1

- Three techniques of digital-to-digital conversion are line coding, block coding and scrambling.

#### 2

- A data element is the smallest entity that can represent a piece of information, and a signal element is the shortest unit of a digital signal that carries data elements.

#### 3

- The data rate defines the number of data elements (bits) sent in 1s whose unit is bits per second (bps). The signal rate is the number of signal elements sent in 1s whose unit is the baud.

#### 4

- Baseline wandering is a drift in the baseline, which is a running average of the received signal power. Since the incomming signal power is evaluated against this baseline to determine the value of the data element, tha baseline wandering make it difficult for the receiver to decode correctly.

#### 5

- When the voltage level in a digital signal is constant for a while, the spectrum creates very low frequencies, called DC components, that present problems for a system that cannot pass low frequencies or a system that uses electrical coupling (via a transformer).

#### 6

- A self-synchronizing digital signal includes timing information in the data being transmitted, that can be achieved if there are transitions in the signal that alert the receiver to the beginning, middle, or end of the pulse.

#### 7

- Five line coding schemes discussed in this book are unipolar, polar, bipolar, multilevel and multitransition.

#### 8

- Block coding changes a block of $m$ bits into a block of $n$ bits, where $n$ is larger than $m$ which provide redundancy to ensure synchronization and to provide some kind of inherent error detecting.

#### 9

- Scrambling does not increase the number of bits and does provide synchronization by substituting long zero-level pulsed with a combination of other levels to provide synchronization.

#### 10

- PCM finds the value of the signal amplitude for each sample but DM finds the change from the previous sample to reduce the complexity of PCM

#### 11

- In parallel mode multiple bits are sent with each clock tick, but in serial mode 1 bit is sent with each clock tick.

#### 12

- Three different techniques in serial transmission are asynchronous, synchronous and isochronous.

- In asynchronous transmission, we send 1 start bit (0) at the beginning and 1 or more stop bits (1s) at the end of each byte.

- In synchronous transmission, we send bits one after another without start or stop bits or gaps so receiver is responsible for grouping the bits.

- The isochronous mode provides synchronization for the entire stream of bits.

### 4.5.3 Problems

#### 1

- In case a ($r = 1$),

$$
\begin{aligned}
S
&= c \times N \times (1/r) \\
&= 1/2 \times 1 \text{Mbps} \times 1 = 1/2\text{Mboud}
\end{aligned}
$$

- In case b ($r = {1 \over 2}$) 

$$
S = 1/2 \times 1 \text{Mbps} \times 2 = 1\text{Mboud}
$$

- In case c ($r = 2$)

$$
S = 1/2 \times 1 \text{Mbps} \times 1/2 = 1/4\text{Mboud}
$$

- In case d ($r = 4/3$)

$$
S = 1/2 \times 1 \text{Mbps} \times 3/4 = 3/8\text{Mboud}
$$

#### 2

- The sender send extra $1\text{Mbit} \times 0.002 = 0.002\text{Mbit} = 2\text{kbit}$.

#### 3

##### a

```
  ^
  ! 0   0   0   0   0   0   0   0    
  !_______________________________ 
  !                                
--!---------------------------------->Time
  !                                
  !                                
```

- The number of changes in the signal level is 0.

##### b

```
  ^
  ! 1   1   1   1   1   1   1   1    
  !                                
  !                                
--!----------------------------------> Time
  !_______________________________ 
  !                                
```

- The number of changes in the signal level is 0.

##### c

```
  ^
  ! 0   1   0   1   0   1   0   1    
  !___     ___     ___     ___     
  !   |   |   |   |   |   |   |    
--!---|---|---|---|---|---|---|------> Time
  !   |___|   |___|   |___|   |___ 
  !                                
```

- The number of changes in the signal level is 7.

##### d

```
  ^
  ! 0   0   1   1   0   0   1   1  
  !_______         _______         
  !       |       |       |        
--!-------|-------|-------|----------> Time
  !       |_______|       |_______
  !                                
```

- The number of changes in the signal level is 3.

- Since more changes in the signal mean injecting more frequencies into the signal, we can guess the bandwidth using the average number of changes.

- The average number of changes in the signal level is $(0 + 0 + 7 + 3)/4 = 5 / 2$.

- Since in the given data streams there is 8 bits, we can think data rate is $N = 8$ and bandwidth is $B = 5 / 16N$.

- Our guess is smaller than the average bandwidth in Table 4.1, $N/2$.

#### 4

##### a

```
  ^
  ! 0   0   0   0   0   0   0   0
  !_______________________________
  !    
--!----------------------------------> Time
  !
  !
```

- The number of changes in the signal level is 0.

##### b

```
  ^
  ! 1   1   1   1   1   1   1   1  
  !    ___     ___     ___     ___
  |   |   |   |   |   |   |   |
--|---|---|---|---|---|---|---|------> Time
  |___|   |___|   |___|   |___|
  !
```

- The number of changes in the signal level is 7.

##### c

```
  ^
  ! 0   1   0   1   0   1   0   1
  !___         _______         ___
  !   |       |       |       |
--!---|-------|-------|-------|------> Time
  !   |_______|       |_______|
  !
```

- The number of changes in the signal level is 4.

##### d

```
  ^
  ! 0   0   1   1   0   0   1   1
  !_______     ___________     ___
  !       |   |           |   |
--!-------|---|-----------|---|-----> Time
  !       |___|           |___|
  !
```

- The number of changes in the signal level is 4.

- The average number of changes in the signal level is $(0 + 7 + 4 + 4) / 4 = 15 / 4$ for $N = 8$.

- We can guess the bandwidth $B = 15 / 32N$.

- Our guess is smaller than the average bandwidth in Table 4.1, $N/2$.

#### 5

##### a
 
```
  ^
  ! 0   0   0   0   0   0   0   0
  !_   _   _   _   _   _   _   _ 
  ! | | | | | | | | | | | | | | |
--!-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|----> Time
  ! |_| |_| |_| |_| |_| |_| |_| |_ 
  ! 
```

- The number of changes in the signal level is 15.

##### b

```
  ^
  ! 1   1   1   1   1   1   1   1  
  !  _   _   _   _   _   _   _   _ 
  | | | | | | | | | | | | | | | |  
--|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|----> Time
  |_| |_| |_| |_| |_| |_| |_| |_|  
  !
```

- The number of changes in the signal level is 15.

##### c

```
  ^
  ! 0   1   0   1   0   1   0   1
  !_     ___     ___     ___     _
  ! |   |   |   |   |   |   |   | 
--!-|---|---|---|---|---|---|---|----> Time
  ! |___|   |___|   |___|   |___| 
  !
```

- The number of changes in the signal level is 8.

##### d

```
  ^
  ! 0   0   1   1   0   0   1   1
  !_   _     _   ___   _     _   _
  ! | | |   | | |   | | |   | | | 
--!-|-|-|---|-|-|---|-|-|---|-|-|----> Time
  ! |_| |___| |_|   |_| |___| |_| 
  !
```

- The number of changes in the signal level is 12.

- The average number of changes in the signal level is $(15 + 15 + 8 + 12) / 4 = 25 / 2$ for $N = 8$

- We can guess the bandwidth $B = 25 / 16N$.

- Our guess is larger than the average bandwidth in Table 4.1, $N$.

#### 6

##### a

```
  ^
  ! 0   0   0   0   0   0   0   0
  !  _   _   _   _   _   _   _   _ 
  | | | | | | | | | | | | | | | |  
--|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-----> Time
  |_| |_| |_| |_| |_| |_| |_| |_|  
  !
```

- The number of changes in the signal level is 15.

##### b

```
  ^
  ! 1   1   1   1   1   1   1   1  
  !_     ___     ___     ___     _
  ! |   |   |   |   |   |   |   | 
--!-|---|---|---|---|---|---|---|-----> Time
  ! |___|   |___|   |___|   |___| 
  !
```

- The number of changes in the signal level is 8.

##### c

```
  ^
  ! 0   1   0   1   0   1   0   1
  !  ___   _     _   ___   _     _
  | |   | | |   | | |   | | |   | 
--|-|---|-|-|---|-|-|---|-|-|---|-----> Time
  |_|   |_| |___| |_|   |_| |___| 
  !
```

- The number of changes in the signal level is 11.

##### d

```
  ^
  ! 0   0   1   1   0   0   1   1
  !  _   ___     _   _   ___     _
  | | | |   |   | | | | |   |   | 
--|-|-|-|---|---|-|-|-|-|---|---|----> Time
  |_| |_|   |___| |_| |_|   |___| 
  !
```

- The number of changes in the signal level is 11.

- The average number of changes in the signal level is $(15 + 8 + 11 + 11)/4 = 45 / 4$ for $N = 8$.

- We can guess the bandwidth $B = 45 / 32N$.

- Our guess is larger than the average bandwidth in Table 4.1, $N$.

#### 7

##### a

```
  ^
  ! 00   00   00   00   00   00   00   00
  !
  !
  !
  !
--!------------------------------------------> Time
  !
  !
-3!_______________________________________
  !
```

- The number of changes in the signal level is 0.

##### b

```
  ^
  ! 11   11   11   11   11   11   11   11
  !
  !
 1!_______________________________________
  !
--!------------------------------------------> Time
  !
  !
  !
```

- The number of changes in the signal level is 0.

##### c

```
  ^
  ! 01   01   01   01   01   01   01   01
  !
  !
  !
  !
--!------------------------------------------> Time
-1!_______________________________________
  !
  !
  !
```

- The nubmer of changes in the signal level is 0.

##### d

```
  ^
  ! 00   11   00   11   00   11   00   11
  !
  !
 1!     ____      ____      ____      ____
  !    |    |    |    |    |    |    |     
--!----|----|----|----|----|----|----|-------> Time
  !    |    |    |    |    |    |    |     
  !    |    |    |    |    |    |    |     
-3!____|    |____|    |____|    |____|     
  !
```

- The number of changes in the signal level is 7.

- The average number of changes in the signal level is $(0 + 0 + 0 + 7)/4 = 7/4$ for $N = 16$.

- We can guess the bandwidth $B = 7 / 48$. 

- Our guess is smaller than the average bandwidth in Table 4.1, $N/4$.

#### 8

##### a

```
  ^
  ! 0   0   0   0   0   0   0   0
  !
  |
--!ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ---> Time
  !
  !
```

- The number of changes in the signal level is 0.

##### b

```
  ^
  ! 1   1   1   1   1   1   1   1
  !    ___             ___
  |   |   |           |   |
--!ㅡㅡ-----ㅡㅡ-----ㅡㅡ-----ㅡㅡ-------> Time
  !           |___|           |___ 
  !
```

- The number of changes in the signal level is 7.

##### c

```
  ^
  ! 0   1   0   1   0   1   0   1
  !            ___             ___
  |           |   |           |   
--!ㅡㅡ-----ㅡㅡ-----ㅡㅡ-----ㅡㅡ-------> Time
  !   |___|           |___|
  !
```

- The number of changes in the signal level is 7.

##### d

```
  ^
  ! 0   0   0   1   1   0   0   0
  !           
  |           
  !ㅡㅡㅡㅡㅡㅡㅡ-----ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ---> Time
  !           |___|
  !
```

- The number of changes in the signal level is 2.

- The average number of changes in the signal level is $(0 + 7 + 7 + 2)/4 = 4$ for $N = 8$.

- We can guess the bandwidth $B = 4 / 8$.

- Our guess is larger than the average bandwidth in Table 4.1, $N/3$.

#### 9

##### a

- 10011001

##### b

- 11000100

##### c

- 01110001

#### 10

- For frequency at 0 Hz, using Figure 4.6 in $0/100 = 0$, the value of the normalized energy is 1.

- For frequency at 50 KHz, using Figure 4.6 in $50/100 = 0.5$, the value of the normalized energy is approximately 0.4.

- For frequency at 100 KHz, using Figure 4.6 in $100/100 = 1$, the value of the normalized energy is 0.

#### 11

- For frequency at 0 KHz, using Figure 4.8 in $0/100 = 0$, the value of the normalized energy is 0.

- For frequency at 50 KHz, using Figure 4.8 in $50/100 = 0.5$, the value of the normalized energy is approximately 0.3.

- For frequency at 100 KHz, using Figure 4.8 in $100/100 = 1$, the value of the normalized energy is approximately 0.4.

#### 12

##### a

```
0100 0000 0000 0000 0000 0001
```

- Output:

```
01010 11110 11110 11110 11110 01001
```

##### b

- 17

##### c

- 2

#### 13

- The number of invalid code sequences is $2^6 - 2^5 = 2^5 = 32$ for 5B/6B encoding and $2^4 - 2^3 = 2^3 = 8$ for 3B/4B encoding.

#### 14

```
11100000000000
```

##### a

```
  ^
  ! 1   1   1   0   0   0   V   B   0   V   B   0   0   0
  !    ___                 ___             ___
  |   |   |               |   |           |   |
--|---|---|----ㅡㅡㅡㅡㅡㅡㅡ----|----ㅡㅡ----|----ㅡㅡㅡㅡㅡㅡㅡㅡ---> Time
  |___|   |___|               |___|   |___|
  !
```

##### b

```
  ^
  ! 1   1   1   B   0   0   V   B   0   0   V   0   0   0
  !    ___     ___         ___
  |   |   |   |   |       |   |
--|---|---|---|----ㅡㅡㅡㅡㅡ---|----ㅡㅡㅡㅡㅡ----ㅡㅡㅡㅡㅡㅡㅡㅡ---> Time
  |___|   |___|               |___|       |___|
```

#### 15

##### a

- Since the bandwidth of a low-pass signal starts at 0, the maximum frequency is equal to bandwidth, 200 kHz.

- According to the Nyquist theorem, the sampling rate is at least 2 times 200,000, 400,000 samples per second.

##### b

- The maximum frequency of the band-pass signal is 300 kHz.

- According to the Nyquist theorem, the sampling rate is at least 2 times 300,000, 600,000 samples per second.

#### 16

##### a

- According to the Nyquist theorem, the sampling rate is at least 2 tiems 200,000, 400,000 samples per second.

- The number of bits per sample is $\log_2 1024 = 10$.

- Thus the bit rate is 10 * 400,000 = 4 Mbps.

##### b

$$
\text{SNR}_{\text{dB}} = 6.02\cdot10 + 1.76 = 61.96
$$

##### c

- 10 * 200 KHz = 2 MHz

#### 17

- The maximum data rate is $2 \times 200,000 \times \log_2 4 = 800\,\text{kbps}$

#### 18

- According to the Nyquist theorem, the sampling rate is at least 2 times 20,000, 40,000 samples per second.

- If we sample the signal using $L$ levels, the number of bits for each sample is $n_b = \log_2 L$.

- The bit rate is $40,000 \times n_b = 30 \,\text{Kbps}$. $n_b = 4/3$, or 1.

- $\text{SNR}_\text{dB} = 6.02 \cdot 1 + 1.76 = 7.78$

#### 19

##### a

- Since for NRZ-L the average bandwidth is $N/2$, the data rate is $2B = 2\,\text{Mbps}$

- Since for Manchester the average bandwidth is $N$, the data rate is $B = 1\,\text{Mbps}$

- Since for MLT-3 the average bandwidth is $N/3$, the data rate is $3B = 3\,\text{Mbps}$

- Since for 2B1Q the average bandwidth is $N/4$, the data rate is $4B = 4\,\text{Mbps}$

#### 20

##### a

- Since in synchronous transmission we send bits one after another without start or stop bits or gaps, the number of transmitted bits is $1,000 \cdot 8 = 8,000 \,\text{bits}$

##### b

- Since in asynchronous transmission we send 1 start bit (0) at the beginning and 1 or more stop bits (1s) at the end of each byte, the number of transmitted bits is $1,000 \cdot 8 + 2 \cdot 1,000 = 10,000 \,\text{bits}$.

##### c

- The redundancy percent in synchronous transmission is $0\%$ and in synchronous is $2,000/8,000 \times 100 = 25\%$
