# code
```
#include<reg51.h>      /* .h indicates header file. it is library file which contains all registers, Timer, serial port
                         & interrrupts of 8051. if we want to use them in program we must include in our program */
			 
void main()    // program execution starts from main. void indicates that main() is not returning any value to other pgm
{              // opening braces

	
  signed char A,B,QUOT,REM;   // A,B,QUOT & REM are variables & sgined char is data type (range -128 to +127 )
	A = 10;
	B = 3;
	QUOT = A/B;              // " / " is used for Division & it gives only quotient
	REM = A % B;             //  " % " is used for division & it gives remainder
	P0 = QUOT;               //  " = "  is assignment operator. it assigns right side value to left side value
	P1 = REM;             
	                     // P0 = (03)decimal = (0x03) hexadecimal = (0000 0011) binary
	                     // P1 = (01)decimal = (0x01) hexadecimal = (0000 0001) binary
}                      // closing brace
```