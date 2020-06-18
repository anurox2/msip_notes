

## Codec Summary
Summary of NB, WB, SWB and FB speech codecs

|Codec|Standard Body/Year|Type|NB or WB or FB|Bit rate (kb/s)|Speech frame(ms)|Bits per sample/frame|Look-ahead (ms)|Algorithm delay (ms)|
|-|-|-|-|-|-|-|-|-|
|G.711|ITU/1972|PCM|NB|64|0.125|8|0|0.125|
|G.726|ITU/1990|ADPCM|NB|40|0.125|5|0|0.125|
|||||32||4||
|||||24||3||
|||||16||2||
|G.728|ITU/1992|LD-CELP|NB|16|0.625|10|0|0.625|
|G.729|ITU/1996|CS-ACELP|NB|8|10|80|5|15|
|G.723.1|ITU/1996|ACELP|NB|5.3|30|159|7.5|37.5|
|||MP-MLQ|NB|6.3||189||
|GSM|ETSI/1991|(FR)RPE-LTP|NB|13|20|260|0|20|
||ETSI/1999|(HR)VSELP|NB|5.6||112|0|20|
||ETSI/2000|(EFR)ACELP|NB|12.2||244|0|20|
|AMR|ETSI/2000|ACELP|NB|4.75|20|95|5|25|
|||||5.15||103|||
|||||5.9||118|||
|||||6.7||134|||
|||||7.4||148|||
|||||7.95||159|||
|||||10.2||204|||
|||||12.2||244|||
|iBLC|IETF/2004|CELP|NB|15.2|20|304|0|20|
|||||13.33|30|400||30|
|G.711.1|ITU/2008|PCM-WB<br>(MDCT)|NB/WB|64|5|320|5|11.875|
|||||80||400|||
|||||96||480|||
|G.722|ITU/1988|SB-ADPCM|WB|64|0.125|8|0|0.125|
|||||56||7|||
|||||48||6|||
|G.722.1|ITU/1999|Transform Coding|WB|24|0.125|8|0|0.125|
|||||32||640|||
||ITU/2005||SWB|24/32/48||480-960|||
|G.719|ITU/2008|Transform Coding|FB|32-128|20|640-2560|20|40|
|AMR-WB<br>(G.722.2)|ETSI/ITU/2003|ACELP|WB|6.6-23.85|20|132-477|0|20|
|SILK|IETF/2009|CELP|WB|6-40|20|120-800|0|20|

### Legend
Abbreviation| Description
-|-
NB|Narrowband = 0 - 4kHz
WB|Wideband = 0 – 7kHz high fidelity speech general audio frequency range
SWB|Super-Wideband = 50 – 14kHz
FB|Fullband = 20 – 20kHz to provide high quality, efficient compression for speech music and general audio. Used in teleconferencing and tele-presence applications
ITU|International Telecommunications Union
ETSI|European Telecommunication Standards Institute
IETF|Internet Engineering Task Force
PCM|Pulse Code Modulation
ADPCM|Adaptive Differential Pulse Code Modulation
LD-CELP|Low-delay Code Excited Linear Prediction uses analysis-by-synthesis approach for codebook search
CS-ACELP|Conjugate Structure-Algebraic Code Excited Linear Prediction
MP-MLQ/ACELP|Multi Pulse—Maximum Likelihood Quantization 
GSM|Global System for Mobile Communications
(FR) Full Rate RPE-LTP|Regular Pulse Excitation/Long Term Prediction Linear prediction coder
(HR) VSELP|Half Rate Vector-Sum Excited Linear Prediction
(EFR) ACELP|Enhanced Full Rate ACELP
AMR|Adaptive Multi Rate Used in wireless communications (3G)
iLBC|Internet Low Bit Rate Codec robust tolerance to packet loss used in Google Talk and Yahoo Messenger
SILK|Super Wideband Audio Codec used in Skype

---
---

### Summary of NB, WB, SWB, and FB speech/audio compression coding

|Mode|Signal Bandwidth (Hz)|Sampling rate (kHz)|Bit-rate(kb/s)|Examples|
|-|-|-|-|-|
|Narrowband (NB)|300 - 3400|8|2.4 - 64|G.711, G.729, G.723, AMR, LPC-10|
|Wideband (WB)|50 - 7000|16|6.6 - 96|G.711.1, G.722, G.722.1, G.722.2|
|Super-wideband (SWB)|50 - 14000|32|24 - 48|G.722.1 (Annex C)|
|Fullband (FB)|20 - 20000|48|32 - 128|G.719|


### Things to think about regarding Codecs
1. **Determine the input and output data rates for a G.711 codec given that the sample rate is 8kHz and the sample is converted to a 14-bit linear code before being compressed into non-linear PCM.**

    Ans:
    - Input data rate $= 8000$ samples/sec * $14$ bits/sample $= 112$ kb/s
    - Output data rate $= 8000$ samples/sec * $8$ bits/sample $= 64$ kb/s

    The compression ratio is <font size="4">$\frac{112}{64}$ </font>$= 1.75$


2. **The G.726 codec is based on ADPCM (Adaptive Differential PCM). Assume the codec’s input speech signal is 16-bit linear PCM with a sampling rate of 8 kHz. The output of the G.726 can operate at four possible data rates; 40kb/s, 32kb/s, 24kb/s and 16 kb/s. How are these data rates obtained?**

    Ans: For the ADPCM encoder, only the difference signal between the input PCM linear signal and the predicted signal is quantized and coded. The difference signal has a much smaller dynamic range than the input to the PCM speech signal so fewer quantization levels are needed.

    - Assume that the number of bits needed to code each quantized difference signal is x, 
    - For $40$ kb/s        
        => $40$ kb/s = $8000$ samples/sec $*$ bits/sample
    <br>=> $X = 40*$<font size="4">$\frac{1000}{8000}$</font> $= 5$ bits/sample
    
    - For $32$ kb/s        
        => $32$ kb/s = $8000$ samples/sec $*$ bits/sample
    <br>=> $X = 32*$<font size="4">$\frac{1000}{8000}$</font> $= 4$ bits/sample
    
    - For $24$ kb/s        
        => $24$ kb/s = $8000$ samples/sec $*$ bits/sample
    <br>=> $X = 24*$<font size="4">$\frac{1000}{8000}$</font> $= 3$ bits/sample
    
    - For $16$ kb/s        
        => $16$ kb/s = $8000$ samples/sec $*$ bits/sample
    <br>=> $X = 16*$<font size="4">$\frac{1000}{8000}$</font> $= 2$ bits/sample
    
    For compression ratios when compared to standard PCM at $64$ kb/s
    - <font size="4">$\frac{64}{40}$</font> $= 1.6$
    - <font size="4">$\frac{64}{32}$</font> $= 2$
    - <font size="4">$\frac{64}{24}$</font> $= 2.67$
    - <font size="4">$\frac{64}{16}$</font> $= 4$

---
---


3. **The G.723.1 codec transmission rates can operate at 5.3(ACELP Algebraic-Code-Excited Linear Predication) or 6.3 kb/s (MPMLQ Multi-Pulse—Maximum Likelihood Quantization)**
   1. What is the frame size?
      - $30$ ms

   2. How many samples are in each frame?
      - G.723.1 is a narrow band code so the sampling rate would be $8000$ samples/sec
      - $8000$ samples/sec $*$ $30$ ms $= 240$ samples

   3. What is the number of parameter bits encoded in each frame for the operating bit rates?
       - For bit rate $5.3$ kb/s
         - $30 ms * 5.3 kb/s = 159 bits$
       - For bit rate $6.3$ kb/s
         - $30 ms * 6.3 kb/s = 189 bits$

---
---

4. **In a Voip system an 8 kb/s G.729 is applied. The packet size can be configured to include one G.729 speech frame per packet or two G.729 speech frames per packet. What is the G.729 payload size, required G.729 IP bandwidth and bandwidth efficiency in each case.**
   
   - For $8 kb/s$ G.729 codec, the length of a speech frame is 10ms, the codec bits for a 10ms frame is then $8 kb/s * 10ms = 80 bits$ or $10 bytes$.
   - If one packet includes one speech frame the payload is 10 bytes. If a packet includes 2 speech frames the payload is 20 bytes.

    The required IP bandwidth for two frames one packet case is:
    <br><font size="5">$\frac{(20 + 40) * 8bits/byte}{20ms}$</font> = 24 kb/s
    - The bandwidth efficiency is: <font size="5">$\frac{20}{20+40}$</font> = 0.33 or 33%


    The required IP bandwidth for one frame one packet (where the IP/UDP/RTP header is 40 bytes, IP 20 bytes, UDP 8 bytes, RTP 12 bytes):
    <br><font size="5">$\frac{(10 + 40) * 8bits/byte}{10ms}$</font> = 40 kb/s
    - The bandwidth efficiency is: <font size="5">$\frac{10}{10+40}$</font> = 0.2 or 20%