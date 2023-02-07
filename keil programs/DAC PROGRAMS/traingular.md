# code for traingular wave
```
#include <reg51.h>
sbit CS=P3^3;
sbit WR2=P3^4;
sbit XFER=P3^5;
unsigned char Data;
void main(void)
{
CS=0;
while(1)
{
for( Data=0;Data<255;Data++)
{

WR2=1;
XFER=1;
P1=Data;
WR2=0;
XFER=0;

}

By Avinash Dangwani ( VESP )

for( Data=255;Data>0;Data--)
{
WR2=1;
XFER=1;
P1=Data;
WR2=0;
XFER=0;
}
}
}
```