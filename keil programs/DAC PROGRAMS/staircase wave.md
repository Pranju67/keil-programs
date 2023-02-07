# code for staircase wave
```
#include <REG51.H>
sbit CS=P3^3;
sbit WR2=P3^4;
sbit XFER=P3^5;
int i;
unsigned char Data;
void main(void)
{
CS=0;
while(1)
{
for(Data=0;Data<255;Data++)
{
WR2=1;
XFER=1;
P1=Data;
WR2=0;
XFER=0;
for(i=0;i<10000;i++)
{ }
}
}

}
```