---
title: "Science of Information"
draft: false
layout: post
date: 2019-06-12 11:11
image: https://ichef.bbci.co.uk/childrens-responsive-ichef-ck/480xn/amz/cbbc/Science_Fact_Science_Fiction.jpg
headerImage: true
tag:
- infobite
- science
star: true
category: blog
author: maximonakpil
description: Notes on exploring the science of information technology.
---
**A brief explanation on how my curiosity lead me here.**
<br>
I needed a recap on math to get sharp at data structures and algorithms, math visualization offered plenty aha moments, found difficulty keeping focused on statistics. I found a *treasure trove of wonder* in an Information science course, that had a lot of answers to how we measure the transfer of knowledge and the mechanics of communication.
<br>
Here are some notes so far...


###### [Study from Science of Information Technology: From Language to Black Holes @ Great Courses](https://www.thegreatcourses.com/courses/the-science-of-information-from-language-to-black-holes.html)
---

### How Computing Began
* Babbage and the Differential Analyzer
* Ada Lovelace - 1815-1852 - first computer programmer
* Vannevar Bush 1931 - recreates Babbage's Differential Analyzer
* Claude Shannon - Builds computer out of logic gates from Boolean Logic.

![LogicCircuits](https://www.nutsvolts.com/uploads/wygwam/NV_0407_Marston_Figure1.jpg)
[Logic Gate Symbols from nutvolts.com](https://www.nutsvolts.com/uploads/wygwam/NV_0407_Marston_Figure1.jpg)
**Logic Gates** <br>
* from Boolean Logic & Electric Circuits
-> 2 light switches 1 | 0
* John Napier - Logarithm Rules LOG2 (base algorithm)
#### MAXWELL'S DEMON
[photo from Information and Energy article](http://www.normalesup.org/~adanchin/science/maxwell.html)
![Maxwell's Demon Experiment](http://www.normalesup.org/~adanchin/icons/demon.jpg) <br>
<br>
* Natural Log
* Information Entropy vs. Entropy in thermodynamics
* Demon's Info is form of Entropy (Zurek)
<br>
**Sorting Demon - trap door to a box with heat in motion.**
<br>
#### Hartley - Shannon Entropy
* ENTROPY H - minimum # of bits required to represent the source.

#### Probability (17th Century)
*RULES:* | *(0 = Impossible; 1 = Certain)*
1. For Any X : <br>
        X, 0 ≤ P(X) ≤ 1
        <br>  0 - 1 = P(X)
2. E (sum of all) P(X) = 1

<div class="breaker"></div>

#### _ E T A O I N S H R D L U (common english letters)
* "Letter Probabilities" 19.3%
* Surprise of a message
* "Pre-fix Free Code Word" - no code word can be the 1st part of any other code word.
* Average Code Word >= Entropy of Information Source
* **"HUFFMAN CODE"** - Best pre-fix free code

<div class="breaker"></div>

#### SHANNON'S FIRST FUNDAMENTAL THEOREM
- Information Inequality relates to entropy to the number of bits to represent messages.
- **Entropy H(X)** of a source (the Average Surprise) equals the main average number of bits necessary to code messages from that source.

#### DATA COMPRESSION
* 1970s GZIP (Israel) - First Data Compression - Analyzes Text & Retruns Compressed File.
<br> Images & Sound Encoding = Runline Encoding (through combination of frequencies)
* 1990s JPEG, MPEG, PNG  - Joint Photographic Experts Group, Moving Pictures Experts Group, Portable Network Graphics.
<br> - 8x8 pixel block via Huffman Code
<br> - Video - 1 Frame = 2,000,000 Pixels - 3 bytes of color per pixel
<br> - 180 Million Bites of info per sec. (US - 30FPS / UK 25FPS)
<br> - Records difference from "P-Frame / Key-frame"

* LOSSLESS Compression

#### Shannon's Second Fundamental Theorem:
* **"Communication Channel"** (Input / Output)
* Defeat Noise
* As long as a channel capacity is not exceeded, then you dont have to communicate slower to be rid of errors.

#### Richard Hamming - "Hamming Distance" (N, K values)
* Distance from one code to another.<br>
**ENCODE : Hamming | Channel : 7, 4 | Error Correction : Binary Code | Decode :  1  Bit of Memory (Err Probability 10-14)**
<br>
*1 radiation induced error per year!*

#### Timeline of Computing Technology
* 1725: Weaving Looms
* 1804: Jacquard Loom - Charles Babbage - Jules Carpentier's Musical Melotrope
* 1890: Herman Hollerith Data Processing - Punch Cards - US census - Tabulating Company (IBM)
* 1954: Fortran IBM - John Backus | "IF / ELSE" - fortran statement
<br> -  8 BITS = 256 different combinations = BYTE
<br> -  Binary -> Compiler -> Language
* 1955: Grace Hopper (US Admiral) COBOL - Common Business Oriented Language
<br> - named after Blaise Pascal. "good tracking tool"
* 1960: ASCII - American Standards Association creates ANSI (American National Standards Institute)
<br> which developed ASCII - American Standard Code for Information Interchange (character to binary)
* 1969: Unix, Linux, Macos - Hacker hats (white: good | black: bad)
* 1973: C Foundation
* 2001: Lockheed Martin - F35 Stealth Fighter Jet
<br> - "M-LOCKS" - 8 million lines of code in C++
* 2014: Swift / OBJ-C
* TODAY = 700 Languages - GE powers turbines and highways
* Robotics - CNC "Computer Numerically Controlled Lathes" (Milling machines)
* Quantum Computing - manipulating state of electrons to process calculations faster.

#### BUILDING BLOCKS
1. System Programming - OS, C++, Assembly language
2. Architectural Programming - Frameworks, Java, Microsoft.Net
3. Application Programming - PHP, Ruby, Python, Web Browser
4. Data Manipulation - My SQL, NoSQL, MongoDB

#### Timeline of Information Theory
* 1676 Order & Disorder - philosophy of engineering - heat - steam engines - "Napoleonic Wars"
* 1824 "Reflections on the motive power of fire" by Nicholas Carnot
<br> - Hot -> Cold = change in temp = energy
<br> (dies of cholera and papers are burned)
* Rudolph Calcius - Laws of thermodynamics
<br> - entropy = irreversible (meanwhile victorian scientists like Ernest Mach reject atomic theory)
* 1844- 1906 Ludwig Boltzman - hot atoms move rapidly
* ENTROPY = measures disorder of things
* 1831 - 1879 JAMES CLERK MAXWELL "MAXWELLS DEMON"
* 1948 Claude Shannon BELL labs - mathematical theory
<br> - bit = atom = 2 states
* 1952 Turing - Morphogenisis, Embryo - clumps cells & form skin, self, organization - describes a living process.
<br> - Found the same natural process in chemistry of nature with Boris Belusov's Human Sugar Consumption.
* Bletchley Park WWII codebreaker [More on Alan Turing...](https://mxnkpl.com/blog/2019-alan-turing/)
* 1960s Newtonian Physics - Precise predictions. Chaos Theory to predict weather - Edward Lorenz (meteorologist)
* 1950s IBM, Benoit,  Mandelbrot set, "Thumbprint of God"
<br> - Turings Patterns - Belusov's Principles - Mandelbrot Fractals

#### REED SOLOMON CODE
**Encode -> Interleave -> Channel -> De-Interleave -> Error Correction -> Decode**

<div class="side-by-side">
    <div class="toright">
        <p>Laser Diode scans Polycarbonate Transparent Plastic - Labeled Surface
        <br> 1/2 Micron wide - Data Layer / "pits"
        <br> Dust = Errors - Super Decoder
        <br> SCHROEDER - "Perceptual Coding"
        <br> - SINEWAVE - spatial frequencies (fourier transform for images)
        </p>
    </div>

    <div class="toleft">
        <img class="image" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/Comparison_CD_DVD_HDDVD_BD.svg/2560px-Comparison_CD_DVD_HDDVD_BD.svg.png">
    </div>
</div>
[Image By Cmglee - Own work, CC BY-SA 3.0]( https://commons.wikimedia.org/w/index.php?curid=21959547)

![Laser Diode Scan Area](https://www.electroschematics.com/wp-content/uploads/2010/02/CD-Working.png)

### SUPER CODER & SUPER CHANNEL
- OUTER CODER | Reed Solomon  | 28,24   
- InterCoder | Reed Solomon |  32, 28
- Raw Channel
- Inner | Decoder
- Outer | Decoder

*Radial errors are easy to correct, CD = corrects 35,000 errors in 1 track*

#### NASA using lossless compression adds Reed-Solomon code
* Voyager - Mission to uranus and neptune - more precise data transactions due to error corrections.
<br>
<br>
<br>

#### FAR REACHING SIGNALS & BANDWITH

<div class="side-by-side">
    <div class="toleft">
        <p> DIGITAL:
        <br> -> Information in a finite number of discrete alternatives
        <br> -> Boolean Logic Gates
        <br> -> Logic Gates
        </p>
    </div>
    <div class="toright">
        <p> ANALOG:
        <br> -> Radio / Sound
        <br> -> Differential Engine
        <br> -> Continous Variables
        <br> -> Time & Velocity
        <br> -> Amplitude & Modulation
        <br> -> Frequency
        </p>
    </div>
</div>

##### Joseph Fourier - Fourier Transform
* Any signal can be regarded as a mixture of simple sinewaves of different frequencies.
<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="https://upload.wikimedia.org/wikipedia/commons/a/a4/Amfm3-en-de.gif">
        <figcaption class="caption"></figcaption>
    </div>
    <div class="toright">
        <img class="image" src="http://hyperphysics.phy-astr.gsu.edu/hbase/Audio/imgaud/rfban.gif">
        <figcaption class="caption"></figcaption>
        </div>
</div>
[Fourier Carrier AM/FM Waves - image from wikipedia](https://commons.wikimedia.org/wiki/File:Amfm3-en-de.gif#/media/File:Amfm3-en-de.gif) | [Bandwith- image from wikipedia](https://commons.wikimedia.org/wiki/File:Amfm3-en-de.gif#/    media/File:Amfm3-en-de.gif)
<br>
##### Nyquist Shannon Sampling Theorem
<div class="breaker"></div>

#### CRYPTOGRAPHY
* Kerckhoff's Principle -> lock has 6 tumblr pins - 5-10 mil, 8 possible lengths
* Log2(8) = 3 bits per pin - 6 pins  
* Julius Cesar Cipher - <br>
-> Plain Text -> Cipher -> Cipher Text -> Encryption -> Encipherment
Msg -> Rule 2 Convert -> Converted Msg -> Transforming 2 plain text (babbage kasiski method)
<br>
##### CRYPTANALYSIS - Frequency Analysis
* TURING'S BOMBE - enigma - Arthur Zimmerman - Linear B (Alice Kobel, Micheal Ventris)
* Shannon - Communication theory of secrecy systems. - Entropy.
* Redundancy (D) D = Hc - Hp - John Hadwick - info gained = # of letters X Bits / Letter
<br>      - information basis for cryptanalysis
* Speech Encipherment - SIG SALLY system - pulse code modulation - "Calculation Complexity"
* Neumann - Computer & the Brain - Entropy - shannon & neumann
* TURING'S Universal Machine
* Algorithmic Information - k2k(m) - algorithmic entropy -> for any particular string of bits, h= ave(k) *(Shannon Entropy)*


---
