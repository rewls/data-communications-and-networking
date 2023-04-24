# Ch3 Introduction to Physical Layer

PART 2: Physical Layer

- Chapter 3 Introduction to Physical Layer

    - 3.1 Data and Signals

        - 3.1.1 Analog and Digital Data

        - 3.1.2 Analog and Digital Signals

        - 3.1.3 Periodic and Nonperiodic

    - 3.2 Periodic Analog Signals

        - 3.2.1 Sine Wave

        - 3.2.2 Phase

        - 3.2.3 Wavelength

        - 3.2.4 Time and Frequency Domains

        - 3.2.5 Composite Signals

        - 3.2.6 Bandwidth

    - 3.3 Digital Signals

        - 3.3.1 Bit Rate

        - 3.3.2 Bit Length

        - 3.3.3 Digital Signal as a Composite Analog Signal

        - 3.3.4 Transmission of Digital Signals

    - 3.4 Transmission Impairment

        - 3.4.1 Attenuation

        - 3.4.2 Distortioin

        - 3.4.3 Noise

    - 3.5 Data Rate Limits

        - 3.5.1 Noiseless Channel: Nyquist Bit Rate

        - 3.5.2 Noisy Channel: Shannon Capacity

        - 3.5.3 Using Both Limits

    - 3.6 Performance

        - 3.6.1 Bandwidth

        - 3.6.2 Throughput

        - 3.6.3 Latency (Delay)

        - 3.6.5 Jitter

## 3.8 Practice set

### 3.8.1 Quizzes

#### 12~14

- Attenuation is a type of transmission impairment in which the signal loses strength due to the resistance of the transmission medium.

- Distortion is a type of transmission impairment in which the signal loses strength due to the different propagation speeds of each frequency that makes up the signal.

- Noise is a type of transmission impairment in which an outside source such as crosstalk corrupts a signal.

### 3.8.2 Questions

#### 1

- The period of a signal is the inverse of its frequency and vice versa: $T = 1 / f$ and $f = 1 / T$

#### 2

- amplitude는 신호의 세기를 의미하고, frequency는 1초 당 cycle 수를 의미하고, phase는 time 0에 대한 waveform의 상대적 위치를 의미한다.

#### 3

- Fourier series gives the frequency domain of a periodic signal; Fourier analysis gives the frequency domain of a nonperiodic signal.

#### 4

- attenuation, distortion, noise

#### 5

- Baseband transmission means sending a digital or an analog signal without modulation using a low-pass channel. Broadband transmission means to mod- ulate signal using a band-pass channel

#### 6

- low-pass channel은 bandwidth가 0에서 시작하는 channel이고, band-pass channel은 bandwidth가 임의의 frequency에서 시작하는 channel이다.

#### 7

- Nyquist theorem은 noiseless channel에 대해 최대 bit rate를 정의한다.

#### 8

- Shannon capacity는 noisy channel에 대해 최대 bit rate를 정의한다.

#### 9

- light는 매우 작은 period를 갖기 때문에 $\lambda = cp$ 공식에 의해 짧아진다.

#### 10

- periodic signal은 frequency domain에서 불연속적으로 나타나고 nonperiodic signal은 연속적으로 나타난다.

#### 11

- continuous

#### 12

- discrete

#### 13

- baseband 

#### 14

- baseband

#### 15

- broadband

### 3.8.3 Problems

#### 1

##### a

$$
{1 \over 24 \,\text{Hz}} = 41.67 \,\text{ms}
$$

##### b

$$
{1 \over 8 \,\text{MHz}} = 0.125 \,\mu\text{s} = 125 \,\text{ns}
$$

##### c

$$
{1 \over 140 \,\text{KHz}} = 7.143 \times 10^{-3} \,\text{ms} = 7.143 \,\mu\text{s}
$$

#### 2

##### a

$$
{1 \over 5 \,\text{s}} = 0.2 \,\text{Hz}
$$

##### b

$$
{1 \over 12 \,\mu\text{s}} = 8.334 \times 10^{-2} \,\text{MHz} = 83.34 \,\text{KHz}
$$

##### c

$$
{1 / 220 \,\text{ns}} = 4.545 \times 10^{-3} \,\text{GHz} = 4.545 \,\text{MHz}
$$

#### 3

##### a

$$
{1 \over 2}n\pi \,\text{radians}
$$

##### b

$$
2n\pi \,\text{radians}
$$

##### c

$$
{1 \over 2}n\pi \,\text{radians}
$$

#### 4

- 200 Hz

```
Amplitude (V)
   ^
  5|_ _ _ _ _ _ _ _ _ _ _ _ _ _ _
   !   !       !        !        !
   !   !       !        !        !
 -------- ... --- ... ---- ... ----> Frequency (Hz)
   0  20  ... 50      100      200
   |<-bandwidth = 200 - 0 = 200->|
```

#### 5

```
Amplitude (V)
   ^
 20|_ _ 
   |   !         
   .   .         
   .   .         
   .   .         
  5|_ _!_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _
   |   !                                 !
 -------------------- ... -----------------> Frequency (Hz)
   0 100                              2100
   |   |<-bandwidth = 2100 - 100 = 2000->|
```

#### 6

- 100Hz sine wave와 200Hz sine wave는 simple signal이므로 bandwidth는 모두 0이다.

#### 7

##### a

$$
{1 \over 0.001 \,\text{s}} = 1000 \,\text{bps} = 1 \,\text{Kbps}
$$

##### b

$$
{1 \over 2 \,\text{ms}} = 0.5 \,\text{Kbps} = 500 \,\text{bps}
$$

##### c

$$
{1 \over 2 \,\mu\text{s}} = 0.5 \,\text{Mbps} = 500 \,\text{Kbps}
$$

#### 8

##### a

$$
1 \,\text{s} : 1000 \,\text{bps} = x \,\text{s} : 10 \,\text{bps}
$$

$$
x = 0.01 \,\text{s}
$$

##### b

$$
1 \,\text{s} : 1000 \,\text{bits} = x \,\text{s} : 8 \,\text{bits}
$$

$$
x = 0.008 \,\text{s}
$$ 

##### c

$$
1 \,\text{s} : 1000 \,\text{bits} = x \,\text{s} : 8 \times 10^5 \,\text{bits}
$$

$$
x = 800 \,\text{s}
$$

#### 9

$$
16 \,\text{ns} : 8 \,\text{bits} = 1 \,\text{s} : x \,\text{bits}
$$

$$
x = {8 \over 16 \times 10^{-9}} = 0.5 \times 10^9 = 500 \,\text{Mb}
$$

#### 10

$$
4 \,\text{ms} : 8 \,\text{cycle} = 1 \,\text{s} : x \,\text{cycle}
$$

$$
x = {8 \over 4} = 2 \,\text{KHz}
$$

#### 11

- 25

#### 12

```
Amplitude (V)
   ^
 10|_ _ _ _ _ _
   |   !       !
   |   !       !
 ---------------------> Frequency (KHz)
   0  10      30
   |
```

#### 13

```
Amplitude (V)
   ^
 30|_ _ _ _ 
   |      /!\
 10|_ _ ///!\\\
   |   !///!\\\!
 ---------------------> Frequency (KHz)
   0  10  20  30
   |
```

#### 14

$$
6 \times {2 \over 5} = 2.4
$$

#### 15

$$
10\log_{10}{90 \over 100} = -0.4576 \,\text{dB}
$$

#### 16

$$
10\log_{10}{x \over 5} = -10 \,\text{dB}
$$

$$
10^{-1} = {x \over 5}
$$

$$
x = 0.5 \,\text{W}
$$

#### 17

$$
3 \times 4 = 12 \,\text{dB}
$$

$$
10\log_{10}{P_2 \over P_1} = 12
$$

$$
{P_2 \over P_1} = 10^{1.2} = 15.85
$$

- The signal is amplified 15.85 times. 

#### 18

$$
\text{transmission time} = 100 / 5 = 20 \,\text{s}
$$

#### 19

$$
(8 \times 60) \times (3 \times 10^8) = 144 \times 10^9 \,\text{m} = 144 \times 10^6 \,\text{km}
$$

#### 20

- $1000 \,\mu\text{m} = 1 \,\text{mm}$

#### 21

$$
4000\log_2(1 + 1000) = 39869 \,\text{bps}
$$

#### 22

$$
\text{SNR} = {10^4 \over 5} = 2 \times 10^3
$$

$$
4\log_2(1 + 2 \times 10^3) = 43.87 \,\text{bps}
$$

#### 23

- 56-Kbps channel

$$
{(2 \times 8) \times 10^3 \over 56} = 285.7 \,\text{s}
$$

- 1-Mbps channel 

$$
{2 \times 8 \over 1} = 16 \,\text{s}
$$

#### 24

$$
\log_2 1024 = 10
$$

$$
1200 \times 1000 \times 10 = 1200 \times 1000 \times 10 = 12 \,\text{Mb}
$$

#### 25

$$
\text{SNR} = {200 \times 10^3 \over 10 \times 2} = 10^4
$$

$$
\text{SNR}_\text{dB} = 10\log_{10} 10^4 = 40 \,\text{dB}
$$

#### 26

$$
P = IV = {V^2 \over R}
$$

$$
\text{SNR} = 20^2 = 400
$$

$$
\text{SNR}_\text{dB} = 10\log_{10} 400 = 26.02 \,\text{dB}
$$

#### 27

##### a

- Solution 1

$$
40 = 10\log_{10} \text{SNR}
$$

$$
\text{SNR} = 10^4
$$

$$
20\log_2(1 + 10^4) = 265.8 \,\text{Kbps}
$$

- Solution 2 (approximately calculate)

$$
20 \times 40 / 3 = 266.7 \,\text{Kbps}
$$

##### b

- Solution 1

$$
4 = 10\log_{10} \text{SNR}
$$

$$
\text{SNR} = 10^{0.4}
$$

$$
200\log_2(1 + 10^{0.4}) = 362.4 \,\text{Kbps}
$$

- Solution 2 (approximately calculate)

$$
200 \times 4 / 3 = 266.7 \,\text{Kbps}
$$

##### c

- Solution 1

$$
20 = 10\log_{10} \text{SNR}
$$

$$
\text{SNR} = 10^2
$$

$$
\log_2(1 + 10^2) = 6.658 \,\text{Mbps}
$$

- Solution 2 (approximately calculate)

$$
1 \times 20 / 3 = 6.667 \,\text{Kbps}
$$

#### 28 

##### a

- rate가 두 배가 될 것이다.

##### b

- rate가 $\text{bandwidth}$만큼 늘어난다.

#### 29

- Solution 1

$$
4 \times \log_2 (1 + \text{SNR}) = 100
$$

$$
\text{SNR} = 2^{100 \over 4} - 1 = 33554431
$$

$$
\text{SNR}_\text{dB} = 10\log_{10} 33554431 = 75.26
$$

- Solution 2 (approximately calculate)

$$
4 \times \text{SNR}_\text{dB} / 3 = 100
$$

$$
\text{SNR}_\text{dB} = 100 / 4 \times 3 = 75
$$

$$
\text{SNR}_\text{dB} = 10\log_{10} \text{SNR} = 75
$$

$$
\text{SNR} = 10^{7.5} = 31622776
$$

#### 30

$$
8 \times 10^3 / 200 = 40 \,\text{s}
$$

#### 31

##### a

$$
(2 \times 10^8) \times 10^{-6} = 200 \,\text{m}
$$

##### b

$$
(2 \times 10^8) \times 10^{-7} = 20 \,\text{m}
$$

##### c

$$
(2 \times 10^8) \times 10^{-8} = 2 \,\text{m}
$$

#### 32

##### a

$$
10^6 \times (2 \times 10^{-3}) = 2 \,\text{Kb}
$$

##### b

$$
10^7 \times (2 \times 10^{-3}) = 20 \,\text{Kb}
$$

##### c

$$
10^8 \times (2 \times 10^{-3}) = 200 \,\text{Kb}
$$

#### 33

$$
\text{propagation time} = (2000 \times 10^3) / (2 \times 10^8) = 10 \,\text{ms}
$$

$$
\text{transmission time} = 5 / 5 = 1 \,\text{s}
$$

$$
\text{queuing time} = 2 \times 10 = 20 \,\mu\text{s}
$$

$$
\text{proccessing time} = 1 \times 10 = 10 \,\mu\text{s}
$$

$$
\text{delay} = 10 \times 10^{-3} + 1 + 20 \times 10^{-6} + 10 \times 10^{-6} = 1.01003 \,\text{s}
$$

- Dominant component is transmission time.

- Queuing time and proceccing timeis negligible.
