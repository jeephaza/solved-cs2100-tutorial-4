Download Link: https://assignmentchef.com/product/solved-cs2100-tutorial-4
<br>
<ol>

 <li>Given below are the contents of some registers and memory locations, where mem(<em>A</em>) refers to the data word stored in the memory location at address <em>A</em>:</li>

</ol>

<table width="409">

 <tbody>

  <tr>

   <td width="263">                 $s0 =  100</td>

   <td width="146">mem (100)      =   1000</td>

  </tr>

  <tr>

   <td width="263">                 $s1 =  160</td>

   <td width="146">mem (160)      =   1600</td>

  </tr>

  <tr>

   <td width="263">                 $s2 = 200</td>

   <td width="146">mem (200)      =   2000</td>

  </tr>

  <tr>

   <td width="263">                $s3  =  240</td>

   <td width="146">mem (240)      =   2400</td>

  </tr>

  <tr>

   <td width="263">                 $s4 =  300</td>

   <td width="146">mem (300)      =   3000</td>

  </tr>

  <tr>

   <td width="263">                 $t0 =  10000</td>

   <td width="146">mem (10000) =   100</td>

  </tr>

  <tr>

   <td width="263">                 $t1 =  15000</td>

   <td width="146">mem (15000) =   150</td>

  </tr>

  <tr>

   <td width="263">                 $t2 = 20000</td>

   <td width="146">mem (20000) =   200</td>

  </tr>

  <tr>

   <td width="263">                 $t3 = 25000</td>

   <td width="146">mem (25000) =   250</td>

  </tr>

  <tr>

   <td width="263">                 $t4 = 30000</td>

   <td width="146">mem (30000) =   300</td>

  </tr>

 </tbody>

</table>

For each of the MIPS instructions below, ‘op’ is an unknown opcode, which is not of our concern here. For each of the data operands in the instruction, if the format is legal, give its <strong>memory address (if applicable) </strong>and <strong>the content inside</strong>. Note that $s0, …, $s4, $t1, …, $t4 are symbolic register names, $zero is register 0 with content zero inside, and only the three addressing modes (register, immediate, and displacement) mentioned in class are considered as legal.

<ul>

 <li>op $t1, $t2</li>

 <li>op $s2, 100($zero)     (c) op $t4, 40($s2)</li>

 <li>op $s3, 200($zero)</li>

 <li>op $t3, $zero($t1)</li>

 <li>op $s1, 140($s1)</li>

</ul>

The answers for (a) have been done for you.

<table width="439">

 <tbody>

  <tr>

   <td width="37"> </td>

   <td width="104"><strong>Operand </strong></td>

   <td width="239"><strong>Target Memory Address </strong></td>

   <td width="59"><strong>Content </strong></td>

  </tr>

  <tr>

   <td width="37">(a)</td>

   <td width="104">$t1$t2</td>

   <td width="239">Not applicableNot applicable</td>

   <td width="59">1500020000</td>

  </tr>

  <tr>

   <td width="37">(b)</td>

   <td width="104">$s2100($zero)</td>

   <td width="239"> </td>

   <td width="59"> </td>

  </tr>

  <tr>

   <td width="37">(c)</td>

   <td width="104">$t440($s2)</td>

   <td width="239"> </td>

   <td width="59"> </td>

  </tr>

  <tr>

   <td width="37">(d)</td>

   <td width="104">$s3200($zero)</td>

   <td width="239"> </td>

   <td width="59"> </td>

  </tr>

  <tr>

   <td width="37">(e)</td>

   <td width="104">$t3$zero($t1)</td>

   <td width="239"> </td>

   <td width="59"> </td>

  </tr>

  <tr>

   <td width="37">(f)</td>

   <td width="104">$s1140($s1)</td>

   <td width="239"> </td>

   <td width="59"> </td>

  </tr>

 </tbody>

</table>







For question 2 below, we are exploring four different types of ISAs. MIPS belongs to the <em>Register-Register</em> style.

<ol start="2">

 <li>You are tasked to design a dedicated 16-bit processor to perform simple addition and would like to evaluate the design using the four different instruction set architecture (ISA) styles. For each of these architectures, the corresponding data movement and arithmetic operations are shown below.  Note that the operands for the instructions are annotated with either @ for address, or $ for register.</li>

</ol>

<table width="565">

 <tbody>

  <tr>

   <td width="130">ISA</td>

   <td width="191">Instructions</td>

   <td width="243">Explanation</td>

  </tr>

  <tr>

   <td width="130"><em>Stack </em></td>

   <td width="191"><strong>push</strong> @<em>src</em> <strong>pop</strong> @<em>dest</em> <strong>add </strong></td>

   <td width="243">Load value in <em>@src</em> onto top of stack.Transfer value at top of stack to<em> @dest.</em>Remove top two values in stack, add them, and load the sum onto top of stack.</td>

  </tr>

  <tr>

   <td width="130"><em>Accumulator</em></td>

   <td width="191"><strong>load</strong> @<em>src</em><strong>add</strong> @<em>src</em><strong> </strong><strong>store</strong> @<em>dest</em></td>

   <td width="243">Load value in <em>@src</em> into accumulator. Add value in<em> @src</em> and value in accumulator, and put sum back into accumulator.Store the value in accumulator into <em>@dest.</em></td>

  </tr>

  <tr>

   <td width="130"><em>Memory-Memory </em></td>

   <td width="191"><strong>add</strong> @<em>dest</em>, @<em>src1</em>, @<em>src2 </em></td>

   <td width="243">Add values in <em>@src1</em> and <em>@src2</em>, and put the sum into <em>@dest</em>.</td>

  </tr>

  <tr>

   <td width="130"><em>Register-Register </em></td>

   <td width="191"><strong>load</strong> $<em>reg</em>, @<em>src</em> <strong>add</strong> $<em>dest</em>, $<em>src1</em>, $<em>src2</em><strong> </strong><strong>store</strong> $<em>reg</em>, @<em>dest</em></td>

   <td width="243">Load value in <em>@src</em> into <em>$reg</em>.Add values in <em>$src1</em> and <em>$src2</em>, and put sum into <em>$dest</em>.Store value in <em>$reg</em> into <em>@dest</em>.</td>

  </tr>

 </tbody>

</table>

Consider the following three C statements with integer variables a0, a1 and a2:

<strong>     a0 = a1 + a2;  a1 = a0 + a2;  a2 = a0 + a1; </strong>

For each of the four architectural styles above, write the assembly code corresponding to the above C code.  Assume that the values of a0, a1, a2 are pre-assigned to memory in addresses @a0, @a1, @a2 respectively. The registers are denoted by $r0 to $r4. First part of each code is given.

<table width="502">

 <tbody>

  <tr>

   <td width="95"><strong><em>Stack </em></strong></td>

   <td width="99"><strong><em>Accumulator </em></strong></td>

   <td width="168"><strong><em>Memory-Memory </em></strong></td>

   <td width="140"><strong><em>Register-Register </em></strong></td>

  </tr>

  <tr>

   <td width="95"><strong>push</strong> @a1 <strong>push </strong>@a2<strong>add </strong> </td>

   <td width="99"><strong>load</strong> @a1<strong>add</strong> @a2 </td>

   <td width="168"><strong>add</strong> @a0, @a1, @a2 </td>

   <td width="140"><strong>load</strong> $r1, @a1 </td>

  </tr>

 </tbody>

</table>




<ol start="3">

 <li>This is a follow up on question 2. We studied the assembly code generated for four different storage architectures, namely stack, accumulator, memory-memory and register-register. For your reference, the code fragment corresponds to the following high level statements:</li>

</ol>

<strong>     a0 = a1 + a2;  a1 = a0 + a2;  a2 = a0 + a1; </strong>(a) Let us study the instruction encoding for this question. Assume that 3 bits will be used for the opcode, and minimal space will be used to represent 128 bytes of addressable memory. Moreover, for the Register-Register ISA, there are only 5 general-purpose registers available.  Assume also a fixed-length instruction format, and that the memory is byte-addressable.

For each of the four architectures, what is the number of bits required for the longest instruction? Hence, what is the size, in number of bytes, of the instructions?

Partial answers are given below. Discuss.

<table width="445">

 <tbody>

  <tr>

   <td width="149"> </td>

   <td width="164"><em>Number of bits for longest instruction </em></td>

   <td width="132"><em>Number of bytes </em></td>

  </tr>

  <tr>

   <td width="149"><em>Stack </em></td>

   <td width="164">10</td>

   <td width="132">2</td>

  </tr>

  <tr>

   <td width="149"><em>Accumulator </em></td>

   <td width="164">10</td>

   <td width="132">2</td>

  </tr>

  <tr>

   <td width="149"><em>Memory-Memory </em></td>

   <td width="164"><strong> </strong></td>

   <td width="132">4</td>

  </tr>

  <tr>

   <td width="149"><em>Register-Register </em></td>

   <td width="164"><strong> </strong></td>

   <td width="132"><strong> </strong></td>

  </tr>

 </tbody>

</table>




(b) What is the size (in number of bytes) of the code in question 2 for each of the four architectures? Which architecture is most efficient in terms of code size for this code?




<ol start="4">

 <li>[Past-year’s exam question]</li>

</ol>

An ISA has 16-bit instructions and 5-bit addresses. There are two classes of instructions: class <em>A</em> instructions have one address, while class <em>B</em> instructions have two addresses. Both classes exist and the encoding space for opcode is completely utilized.

<ul>

 <li>What is the minimum total number of instructions?</li>

 <li>What is the maximum total number of instructions?</li>

</ul>








