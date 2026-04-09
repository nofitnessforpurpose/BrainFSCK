# BrainFSCK
BrainFSCK interpreter implementation in Organiser II OPL.

This <a href="https://en.wikipedia.org/wiki/Psion_Organiser"> Organiser II</a> <a href="https://en.wikipedia.org/wiki/Open_Programming_Language">OPL program</a> the interprets <a href="https://en.wikipedia.org/wiki/Brainfuck">BrainFSCK</a> code.  

<div align="center">
  <div style="display: flex; align-items: flex-start;">
    <img src="https://github.com/nofitnessforpurpose/BrainFSCK/blob/main/images/BFSCK-01.png" width="400px" alt="NotFitForPurpose Image copyright (c) 20 August 2025 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

[![Organiser](https://img.shields.io/badge/gadget-Organiser_II-blueviolet.svg?%3D&style=flat-square)](https://en.wikipedia.org/wiki/Psion_Organiser)
[![GitHub License](https://img.shields.io/github/license/nofitnessforpurpose/BrainFSCK?style=flat-square)](https://github.com/nofitnessforpurpose/BrainFSCK/blob/main/LICENSE)
[![Maintenance](https://img.shields.io/badge/maintained%3F-yes-green.svg?style=flat-square)](https://github.com/nofitnessforpurpose/BrainFSCK/graphs/commit-activity)
![GitHub repo size](https://img.shields.io/github/repo-size/nofitnessforpurpose/BrainFSCK?style=flat-square)

<br>  

## Discussion
In the case of the native POPL interpreted version of BrainFSCK the BrainFSCK code can, unlike POPL, be run from the data pack. i.e. it does not need to be loaded into RAM, only the interpreter needs to be loaded into RAM. As a result the interpreter might be considered relatively memory efficient.

Note
The interpreter can be stored on a data pack, as the native POPL interpreter  program is compiled code will be loaded into RAM. 

<BR>

## Use Case
Investigation into operation of micro interpreters, edge case software.

<BR>

The CODE folder contains two OPL files:  
bfsk.opl: The core interpreter. It processes a BrainFSCK string and executes the corresponding commands.  
brainfk.opl: A demonstration script. It shows how to construct a BrainFSCK command sequence and pass it to the interpreter.  

### Technical Details  
Flexibility: The system supports various command sequences, allowing for a wide range of programs.  
Optimization: For developers looking for higher performance, the bfsk.opl code can be modified to operate directly on a specific area of memory rather than using standard string manipulation.

### Getting Started
To see the interpreter in action, place the two proceedures in the A: storage or data pack locations. Translate them via the PROG menu and run brainfk.opl. This will load the sample program into a string and pass it to the bfsk procedure for execution.  

Syntax Note: Character Support
In this implementation, the standard Brainfsk loop characters [ and ] are aliased to ( and ).
This accommodation is made because entering the native square bracket characters in the OPL editor on certain Psion hardware platforms can be difficult. The interpreter accepts both the traditional symbols and their rounded counterparts interchangeably.

<BR>  

### BrainFSK In Action
What’s happening in the animation:  

The Tape: The row of numbered boxes represents the memory cells.  

The Green Cell: This is where the Data Pointer is currently looking.  

The Title: Shows the current command being executed (in brackets) and the symbol it corresponds to.  

The Logic: You can see Cell 0 act as a "counter." The loop continues as long as Cell 0 is not zero, effectively "moving" and multiplying the value into Cell 1.  

By the end of this short program, the machine has successfully calculated 2×3=6.  

<div align="center">
  <div style="display: flex; align-items: flex-start;">
    <img src="https://github.com/nofitnessforpurpose/BrainFSCK/blob/main/images/Code_Generated_Image.gif" width="400px" alt="NotFitForPurpose Image copyright (c) 08 Feb 2026 nofitnessforpurpose All Rights Reserved">
  </div>
</div>
<BR>

## Questions / Discussion
See <a target="_blank" rel="noopener noreferrer" href="https://www.organiser2.com/"> Organiser 2 Software </a> forum, though see note below first.

<BR>

## Please note:  
All information is For Indication only.
No association, affiliation, recommendation, suitability, fitness for purpose should be assumed or is implied.
Registered trademarks are owned by their respective registrants.
