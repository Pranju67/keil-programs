# code for square wave
```
#include <reg51.h> //All 8051 SFR ‘s are present in reg51.h file
sbit wr = P0^7; // P0.7 is declared as sbit (single bit)
void main ()
{

TMOD=0X01; //Select Timer 0 Mode 1 (16bit Timer mode)
P1 = 0XFF; // 0XFF Hexa = 255 Decimal = 1111 1111 Binary

//This digital value will generate 5v(Logic 1) at the output of edsim DAC
while (1) // creating infinite loop by passing 1 (true) as argument in while loop
{
P1 = ~ P1; // ~ -> Taking 1’s compliment of P1 i.e. 11111 1111 -> 0000 0000 & viceversa
wr = 0; // Enable edsim DAC for writing
//Initializing Timer with 0XFE32 for 0.5msec time delay
TH0=0XFE;
TL0=0X32;
TR0=1; //Turn – on Timer 0
while ( TF0 != 1 ) // empty body will be executed till timer flag 0 is not equal to 1 ( TF0 !=1 )
{ }
TR0=0; //Turn – off Timer 0
TF0=0; //Clearing timer flag
}
}
```