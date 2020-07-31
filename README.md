# STM32F407 Discovery Board simple register programming
Done from scratch starting by memory mapping the registers from peripheral base address + specific register offsets.

## Description
This little project makes a LED blink and sends a message to the debug SWV trace line when a button is pressed. <br>
But what is kind of neat is that it does that without any use of previously configured STM32F407GV files for the registers. <br>
I went to the datasheet and the reference manual of the microcontroller STM32F407GV of the board STM32F407 DISCOVERY KIT version DISC1, and using the memory map data of the datasheet and the reference manual register offset's mapped each register (variable) into memory (BASE_ADDRESS + OFFSET) and from there programmed this little program using direct register programming. <br>
Of course this is a simple thing but a neat example of how to do it. <br>
I also made reg_base_addresses.h, that as all memory maps defined, for more serious uses, use the 15K lines file from STM32 for this processor that is more complete and as all the registers already mapped.

## License
BSD 3-Clause license

## Have fun!
Best regards <br>
Joao Nuno Carvalho