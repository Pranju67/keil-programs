# code
```
#include<reg51.h>      /* .h indicates header file. it is library file which contains all registers, Timer, serial port
                         & interrrupts of 8051. if we want to use them in program we must include in our program */
			 
void main()    // program execution starts from main. void indicates that main() is not returning any value to other pgm
{              // opening braces

	
  signed char A,B,SUM;      // A,B & SUM are variables & sgined char is data type (range -128 to +127 )
	A = 6;
	B = 5;
	SUM = A-B;
	P0 = SUM;                    //  " = "  is assignment operator. it assigns right side value to left side value
	                     // P0 = (01)decimal = (0x01) hexadecimal = (0000 0001) binary
}   
```