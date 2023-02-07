# code for ramp wave
```
#include <reg51.h>
sbit wr = P0^7; // edsim wr pin is declared as sbit (single bit)
unsigned int Data; // unsigned int range is 0 - 65535
void main(void)
{
while(1) //infinite loop is created
{
for( Data=0;Data<=255;Data++)
{

wr = 1; //Disable DAC for Writing
P1 = Data;
wr = 0; //Enable DAC for Writing

}
}

}
```