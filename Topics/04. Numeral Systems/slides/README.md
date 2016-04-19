<!-- section start -->
<!-- attr: { id:'', class:'slide-title', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Numeral Systems
## Binary, Decimal and Hexadecimal Numbers

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/hex-fingers.png" style="top:45%; left:60%; width:45%; z-index:-1" /> -->

<div class="signature">
	<p class="signature-course">C# Fundamentals - Part II</p>
	<p class="signature-initiative">Telerik Software Academy</p>
	<a href="https://telerikacademy.com" class="signature-link">https://telerikacademy.com</a>
</div>

<!-- section start -->
<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Table of Contents
- [Numeral Systems](#/numeral-systems)
  - [Binary and Decimal Numbers](#/binary-decimal-numbers)
  - [Hexadecimal Numbers](#/hexadecimal-numbers)
  - [Conversion between Numeral Systems](#/numeral-systems-conversions)
- [Representation of Numbers](#/numbers-representation)
  - [Positive and Negative Integer Numbers](#/positive-negative-numbers)
  - [Floating-Point Numbers](#/floating-point-numbers)
- [Text Representation](#/text-representation)

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic03.png" style="top:13.88%; left:80.47%; width:24.79%; z-index:-1" /> -->




<!-- section start -->
<!-- attr: { id:'numeral-systems', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# <a id="numeral-systems"></a> Numeral Systems
<!-- ## Conversion between Numeral Systems -->
<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic04.png" style="top:55%; left:14.00%; width:22%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic05.png" style="top:55%; left:61.75%; width:25%; z-index:-1" /> -->


<!-- attr: { id:'binary-decimal-numbers', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
<!-- # <a id="binary-decimal-numbers"></a>  Decimal Numbers -->
- Decimal numbers (base 10)
  - Represented using 10 numerals: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`
- Each position represents a power of 10:

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/dec-nums.png" style="top:40%; left:5%; width:90%; z-index:-1" /> -->
<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic06.png" style="top:80%; left:76.16%; width:28.69%; z-index:-1" /> -->


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Binary Numeral System
- Binary numbers are represented by sequence of bits (smallest unit of information – 0 or 1)
  - Bits are easy to represent in electronics

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic07.png" style="top:40%; left:1.87%; width:102.26%; z-index:-1" /> -->



<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Binary Numbers
- Binary numbers (base 2)
  - Represented by 2 numerals:  `0` and `1`
- Each position represents a power of 2:

  <!-- <img class="slide-image" showInPresentation="true"  src="imgs/bin-nums.png" style="top:45%; left:5%; width:90%; z-index:-1" /> -->


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Binary to Decimal Conversion
- Multiply each numeral by its exponent:

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/bin-2-dec.png" style="top:25%; left:5%; width:90%; z-index:-1" /> -->

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# Decimal to Binary Conversion
- Divide by 2 and append the reminders in reversed order:
- 500/2  = 250 (0)
- 250/2  = 125 (0)
- 125/2  = 62  (1)
-  62/2  = 31  (0)
-  31/2  = 15  (1)
-  15/2  = 7   (1)
-   7/2  = 3   (1)
-   3/2  = 1   (1)
-   1/2  = 0   (1)

<p style="font-size: 46px; color: orange; position: absolute; top: 35%; left: 50%;">500<sub>d</sub> = 111110100<sub>b</sub></p>


<!-- attr: { id:'hexadecimal-numbers', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# <a id="hexadecimal-numbers"></a>  Hexadecimal Numbers
- Hexadecimal numbers (base 16)
  - Represented using 16 numerals: `0`, `1`, `2`, ... `9`, `A`, `B`, `C`, `D`, `E` and `F`
- Usually prefixed with `0x`

| **Hex digits value**                            |||
|:-------------:|:-------------:|:-----:|
|0 &rarr; 0x0| 8 &rarr; 0x8||4 &rarr; 0x4|12 &rarr; 0xC|
|1 &rarr; 0x1| 9 &rarr; 0x9||5 &rarr; 0x5|13 &rarr; 0xD|
|2 &rarr; 0x2|10 &rarr; 0xA||6 &rarr; 0x6|14 &rarr; 0xE|
|3 &rarr; 0x3|11 &rarr; 0xB||7 &rarr; 0x7|15 &rarr; 0xF|


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Hexadecimal Numbers
- Each position represents a power of 16:

  <!-- <img class="slide-image" showInPresentation="true"  src="imgs/hex-nums.png" style="top:25%; left:5%; width:95%; z-index:-1" /> -->


<!-- attr: { id:'numeral-systems-conversions', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'font-size: 42px' } -->
# <a id="numeral-systems-conversions"></a>  Hexadecimal to Decimal Conversion
- Multiply each digit by its exponent

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/hex-2-dec.png" style="top:35%; left:5%; width:80%; z-index:-1" /> -->


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Decimal to Hexadecimal Conversion
- Divide by 16 and append the reminders in reversed order
- 500/16 = 31 (4) 	
- 31/16  = 1 (F)
- 1/16   = 0 (1) 	
<p style="font-size: 46px; color: orange; position: absolute; top: 35%; left: 50%;">500<sub>d</sub> = 1F4<sub>hex</sub></p>


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px' } -->
# Binary to Hexadecimal (and reverse) Conversion
- The conversion from binary to hexadecimal (and back) is straightforward: each hex digit corresponds to a sequence of 4 binary digits:

| **0 - 3** | **4 - 7** | **8 - B** | **C - F** |
|:--------:|:--------:|:--------:|:--------:|
|0x0 = 0000|0x4 = 0100|0x8 = 1000|0xC = 1100|
|0x1 = 0001|0x5 = 0101|0x9 = 1001|0xD = 1101|
|0x2 = 0010|0x6 = 0110|0xA = 1010|0xE = 1110|
|0x3 = 0011|0x7 = 0111|0xB = 1011|0xF = 1111|




<!-- section start -->
<!-- attr: { id:'numbers-representation', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- <a id="numbers-representation"></a>  # Numbers Representation -->
<!-- ## Positive and Negative Integers and Floating-Point Numbers -->

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic20.png" style="top:60%; left:75%; width:15%; z-index:-1" /> -->


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
# Representation of Integers
- A `short` is represented by 16 bits
  - 100	= **2**<sup>`6`</sup> + **2**<sup>`5`</sup> + **2**<sup>`2`</sup> = 00000000 01100100
- An `int` is represented by 32 bits  
  - 65545 = **2**<sup>`16`</sup> + **2**<sup>`3`</sup> + **2**<sup>`0`</sup> = 00000000 00000001 00000000 00001001
- A `char` is represented by 16 bits
  - '0'	= 48 = **2**<sup>`5`</sup> + **2**<sup>`4`</sup> =	= 00000000 00110000


<!-- attr: { id:'positive-negative-numbers', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<a id="positive-negative-numbers"></a>  
# Positive and Negative Numbers
- A number's sign is determined by the`Most Significant Bit` (MSB)
  - Only in signed integers: `sbyte`, `short`, `int`, `long`
  - Leading **0** means positive number
    - Leading **1** means negative number
  - _Example_: (8 bit numbers)
    - **0**`XXXXXXX`<sub>b</sub> > 0	e.g. 00010010b = 18
    - **0**`0000000`<sub>b</sub> = 0
    - **1**`XXXXXXX`<sub>b</sub> < 0	e.g. 10010010b = -110


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Positive and Negative Numbers
- The largest positive 8-bit `sbyte` number:
  - **127** = (**2**<sup>`7`</sup> - 1) = 01111111<sub>b</sub>
- The smallest negative 8-bit number:
  - **-128** = (**-2**<sup>`7`</sup>) = 10000000<sub>b</sub>
- The largest positive 32-bit `int` number:
  - **2 147 483 647** (**2**<sup>`31`</sup> - 1) = 01111…11111<sub>b</sub>
- The smallest negative 32-bit number:
  - **-2 147 483 648** (**-2**<sup>`31`</sup>) = 10000…00000<sub>b</sub>


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px' } -->
# Representation of 8-bit Numbers
- Positive 8-bit numbers have the format <!-- .element: class="" style="width: 70%" --> **0** XXXXXXX
  - Their value is the decimal of their last 7 bits (XXXXXXX)
- Negative 8-bit numbers have the format <!-- .element: class="" style="width: 70%" --> **1** YYYYYYY
  - Their value is 128 (2<sup>7</sup>) minus (-) the decimal of YYYYYYY
  - 10010010<sub>b</sub> = 2<sup>7</sup> – 10010<sub>b</sub> = 128 - 18 = -110

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/table.png" style="top:10%; left:70%; width:30%; z-index:-1" /> -->

<!-- attr: { id:'floating-point-numbers', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 42px' } -->
<a id="floating-point-numbers"></a>  
# Floating-Point Numbers
- Floating-point numbers representation (according to the IEEE 754 standard*):

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/ieee-754-float.png" style="top:25%; left:0%; width:95%; z-index:-1" /> -->
- Example:

<!-- .element: class="" style="position: absolute; top: 55%" -->

<!-- <img class="slide-image" showInPresentation="true"  src="imgs/ieee-754-float-example.png" style="top:60%; left:0%; width:90%; z-index:-1" /> -->



<!-- section start -->
<!-- attr: { id:'', class:'slide-section', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Text Representation in Computer Systems -->
<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic22.png" style="top:55%; left:32%; width:35%; z-index:-1" /> -->


<!-- attr: { id:'text-representation, class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
<a id="text-representation"></a>
# How Computers Represent Text Data?
- `Text encoding` is a system that uses binary numbers (1 and 0) to represent characters
  -  Letters, numerals, symbols etc.
- In the `ASCII` encoding each character consists of 8 bits (one byte) of data
  - ASCII is used in nearly all personal computers
- In the `Unicode` (`UTF-16`) encoding each character consists of 16 bits (two bytes)
  - Can represent many alphabets


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'font-size: 40px' } -->
# Character Codes – ASCII Table
<!-- <img class="slide-image" showInPresentation="true"  src="imgs/pic23.png" style="top: 60%; left: -15%; width: 20%; z-index: -1"> -->

|Binary code|Decimal code|Character|
|:---------:|:----------:|:-------:|
|01000001   |65          |A        |
|01000010   |66          |B        |
|01000011   |67          |C        |
|01000100   |68          |D        |
|00100011   |35          |#        |
|01100000   |48          |0        |
|00110001   |49          |1        |
|01111110   |126         |~        |

<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'False', style:'' } -->
# Strings of Characters
- Strings are sequences of characters
  - Null-terminated (like in C)

  <!-- <img src="imgs/null-term-string.png" showInPresentation="true" style="display: block; width: 100%; z-index: -1"> -->
  - Represented by array

  <!-- <img src="imgs/string-arr.png" style="display: block; width: 100%; z-index: -1"> -->
- Characters in the strings can be:
  - 8 bit (ASCII / windows-1251 / …)
  - 16 bit (UTF-16)


<!-- attr: { id:'', class:'', showInPresentation:'True', hasScriptWrapper:'True', style:'' } -->
<!-- # Numeral Systems -->
<!-- <img class="slide-image" showInPresentation="true"  src="https://raw.githubusercontent.com/TelerikAcademy/Common/master/revealjs-theme/css/imgs/questions-ninja.png" style="width:70%; top:15%; left:10%" /> -->
<div style="position: absolute; bottom: 1em; right: 0; font-size: 26px;">http://academy.telerik.com</div>
