# embedded-interview-questions

1) __Which endianness is: A) x86 families. B) ARM families. C) internet protocols. D) other processors? One of these is kind of a trick question.__

2) __Explain how interrupts work. What are some things that you should never do in an interrupt function?__

3) __Explain when you should use "volatile" in C.__

4) __Explain UART, SPI, I2C buses. Describe some of the signals in each. At a high-level describe each. Have you ever used any? Where? How? What type of test equipment would you want to use to debug these types of buses? Have you ever used test equipment to do it? Which?__

5) __Explain how DMA works. What are some of the issues that you need to worry about when using DMA?__

6) __Where does the interrupt table reside in the memory map for various processor families?__

7) __In which direction does the stack grow in various processor families?__

8) __Implement a Count Leading Zero (CLZ) bit algorithm, but don't use the assembler instruction. What optimizations to make it faster? What are some uses of CLZ?__

9) __What is RISC-V? What is it's claimed pros or cons?__

10) __List some ARM cores. For embedded use, which cores were most commonly used in the past? now?__

11) __Explain processor pipelines, and the pro/cons of shorter or longer pipelines.__

12) __Explain fixed-point math. How do you convert a number into a fixed-point, and back again? Have you ever written any C functions or algorithms that used fixed-point math? Why did you?__

13) __What is a pull-up or pull-down resistor? When might you need to use them?__

14) __What is "zero copy" or "zero buffer" concept?__

15) __How do you determine if a memory address is aligned on a 4 byte boundary in C?__

16) __What hardware debugging protocols are used to communicate with ARM microcontrollers?__

JTAG and SWD. 

17) __What processor architecture was the original Arduino based on?__

The ATmega168 on the Arduino Duemilanove (?)

18) __What are the basic concepts of what happens before main() is called in C?__

19) __What are the basic concepts of how printf() works? List and describe some of the special format characters? Show some simple C coding examples.__

20) __Describe each of the following? SRAM, Pseudo-SRAM, DRAM, ROM, PROM, EPROM, EEPROM, MRAM, FRAM, ...__

21) __Show how to declare a pointer to constant data in C. Show how to declare a function pointer in C.__

```c
const uint8_t foo = 20;
uint8_t * bar;
bar = &foo;
```

```c
void (*foo) (int);
```

22) __How do you multiply without using multiply or divide instructions for a multiplier constant of 15, 30, 60, 260?__

23) __When do you use memmove() instead of memcpy() in C? Describe why.__

24) __Why is strlen() sometimes not considered "safe" in C? How to make it safer? What is the newer safer function name?__

25) __When is the best time to malloc() large blocks of memory in embedded processors? Describe alternate approach if malloc() isn't available or desired to not use it, and describe some things you will need to do to ensure it safely works.__

26) __Describe symbols on a schematic? What is a printed circuit board?__

27) __Do you know how to use a logic probe? multimeter? oscilloscope? logic analyzer? function generator? spectrum analyzer? other test equipment? Describe when you might want to use each of these. Have you hooked up and used any of these?__

28) __What processors or microcontrollers are considered 4-bit? 8-bit? 16-bit? 24-bit? 32-bit? Which have you used in each size group? Which is your favorite or hate?__

29) __What is ohm's law?__

`V = I * R`

30) __What is Nyquist frequency (rate)? When is this important?__
- Nyquist frequency is the highest possible frequency that can be accurately sampled based on the sampling rate. Any data sampled past the Nyquist frequency will come with aliasing, a type of digital distortion.

31) __What is "wait state"?__

32) __What are some common logic voltages?__

3.3v is most commonly used nowadays, followed by 5v and 1.8v.

33) __What are some common logic famlies?__

34) __What is a CPLD? an FPGA? Describe why they might be used in an embedded system?__

35) __List some types of connectors found on test equipment.__

36) __What is AC? What is DC? Describe the voltage in the wall outlet? Describe the voltage in USB 1.x and 2.x cables?__

- Alternative Current and Direct Current. Alternative Current alternates between VCC and GND at a fixed frequency, usually 60Hz. Direct current does not. 

- In a wall outlet, the AC voltage is 220v (in European and Asian countries), and 110V (in US and Canada).

- In USB 1.x and 2.x cables, DC voltage is 5v. 

37) __What is RS232? RS432? RS485? MIDI? What do these have in common?__

- They are all serial communication protocols. 
- RS232 is full-duplex, RS432 is half-duplex. RS485 is differential transmission mode, while RS232 is single-ended transmission mode. MIDI is very similar to RS232, however MIDI has a baud rate of 31250 baud, while RS232 has many standard baud rates.

38) __What is ESD? Describe the purpose of "pink" ESD bags? black or silvery ESD bag? How do you properly use a ground strap? When should you use a ground strap? How critical is it to use ESD protections? How do you safely move ESD-sensitive boards between different parts of a building?__

39) __What is "Lockout-Tagout"?__

- Lockout-Tagout is a safety protocol used to prevent tampering with machinery when not in use. The machinery in question has to be locked and tagged (with the name of the person who holds the key) when not in use. 

40) __What is ISO9001? What is a simple summary of it's concepts?__

41) __What is A/D? D/A? OpAmp? Comparator Other Components Here? Describe each. What/when might each be used?__

42) __What host O/S have you used? List experience from most to least used.__

- Linux (Fedora, Ubuntu, Debian, Arch)

- Windows 

- MacOS

43) __What embedded RTOS have you used? Have you ever written your own from scratch?__


44) __Have you ever implemented from scratch any functions from the C Standard Library (that ships with most compilers)? Created your own because functions in C library didn't support something you needed?__
Most <string.h> functions, `atoi`, `itoa`, and other misc. functions in K&R's book.

45) __Have you ever used any encryption algorithms? Did you write your own from scratch or use a library (which one)? Describe which type of algorithms you used and in what situations you used them?__

45) __What is a CRC algorithm? Why would you use it? What are some CRC algorithms? What issues do you need to worry about when using CRC algorithms that might cause problems? Have you ever written a CRC algorithm from scratch?__

46) __Do you know how to solder? Have you ever soldered surface mount devices?__

47) __How do you permanently archive source code? project? what should be archived? what should be documented? have you ever written any procedures of how to archive or build a project? How about describing how to install software tools and configuring them from scratch on a brand new computer that was pulled out of a box?__

48) __What issues are a concern for algorithms that read/write data to DRAM instead of SRAM?__

49) __What is the "escape sequence" for "Hayes Command Set"? Where was this used in the past? Where is it used today?__

50) __What is the "escape character" for "Epson ESC/P"? Where is this used?__

51) __After powerup, have you ever initialized a character display using C code? From scratch or library calls?__

52) __Have you ever written a RAM test from scratch? What are some issues you need to test?__

53) __Have you ever written code to initialize (configure) low-power self-refreshing DRAM memory after power up (independent of BIOS or other code that did it for the system)? It's likely that most people have never done this.__

54) __Write code in C to "round up" any number to the next "power of 2", unless the number is already a power of 2. For example, 5 rounds up to 8, 42 rounds up to 64, 128 rounds to 128. When is this algorithm useful?__

55) __What are two of the hardware protocols used to communicate with SD cards? Which will most likely work with more microcontrollers?__

56) __What issues concerns software when you WRITE a value to EEPROM memory? FLASH memory?__

57) __What is NOR-Flash and NAND-Flash memory? Are there any unique software concerns for either?__

58) __Conceptually, what do you need to do after reconfiguring a digital PLL? What if the digital PLL sources the clock for your microcontroller (and other concerns)?__

59) __What topics or categories of jokes shouldn't you discuss, tell, forward at work?__
- Jokes considered inappropriate or of discriminative nature.

60) __Have you ever used any power tools for woodworking or metalworking?__

61) __What is a common expression said when cutting anything to a specific length? (old expression for woodworking)__

Measure twice cut once.

62) __Have you ever 3D printed anything? Have you ever created a 3D model for anything? List one or more 3D file extensions.__

- `.stl`, `.obj`

63) __Do you know how to wire an AC wall outlet or ceiling light? Have you ever done either?__

64) __Have you ever installed a new hard drive / RAM / CPU in a desktop computer?__


65) __Have you ever installed Windows or Linux from scratch on a computer that has a brand-new hard drive?__


66) __Have you ever "burned" a CD-R or DVD-R disc? Have you ever created an ISO image of a CD or DVD or USB drive or hard drive?__

67) __Have you ever read the contents of a serial-EEPROM chip from a dead system (though EEPROM chip is ok)?__


68) __Have you ever written data to a serial-EEPROM chip before it is soldered down to a PCB?__


69) __How do you erase an "old school" EPROM chip? (has a glass window on top of the chip)__

- Erasing an EPROM is done by shining ultraviolet ray on the window - an alternative is to leave it out under direct sunlight for a bit.

70) __Describe any infrared protocols, either for data or remote controlling a TV.__

71) __What is the most common protocol is used to communicate with a "smart card"? Have you ever written any software to communicate with a "smart card" in an embedded product?__

72) __What is I2S? Where is it used? Why might you want to use I2S in an embedded system? Have you ever used it?__

73) __What is CAN, LIN, FlexRay? Where are they used? Have you ever used any?__

74) __What is ARINC 429? Where is it commonly used? Have you ever used it?__

75) __What in-circuit debuggers or programmers have you used? Which one do you like or hate?__


76) __Do you know any assembler code? For which processor? What assembler code is your favorite or hate? Have you ever written an assembler from scratch?__

77) __What is "duff's device"? Have you ever used it?__

78) __What is dual-port RAM? Why would it be useful in some embedded systems? What concerns do you need to worry about when using it? Have you ever used it? How?__

79) __Have you ever soldered any electronic kits? Have you ever designed your own PCB(s)? Describe. What is a Gerber file?__

- A Gerber file is usually a collection of files with information on how a Printed Circuit Board should be manufactured, including routes, drill holes, silkscreen..

80) __If you create a circular buffer, what size of buffer might optimized code be slightly faster to execute? why?__

81) __Describe how to multiply two 256-bit numbers using any 32-bit processor without FPU or special instructions. Two or more methods?__
