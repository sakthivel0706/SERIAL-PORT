
# Serial Transfer of Single Byte / Character using 8051 (Keil)

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character

```
#include <reg51.h>

void main (void)
{
TMOD = 0X20;
TH1 = 0XFA;
SCON = 0X50;
TR1 =1;
	
SBUF ='A';
while (T1 == 0);
T1=0;
	
while(1);
}

```
### (ii) Serial Port to Transfer a Message

```
#include <reg51.h>

void main(void)
{
    unsigned char msg[] = "SAKTHI";
    unsigned char i;

    TMOD = 0X20;  
    TH1  = 0XFA;
    SCON = 0X50;      
    TR1  = 1;

    for(i = 0; i<=12; i++)
    {
        SBUF = msg[i];
        while(TI == 0);
        TI = 0;
    }

    while(1);
}


```

### OUTPUT:
### (i) Serial Port Transfer a Single Character
<img width="1919" height="1199" alt="552510410-25759442-924d-48f4-b060-37386d74fd3d" src="https://github.com/user-attachments/assets/aa7dc52b-b280-4b53-b4b0-78b5963da02a" />


### (ii) Serial Port to Transfer a Message
<img width="1436" height="960" alt="Screenshot 2026-02-20 105410" src="https://github.com/user-attachments/assets/bd6e22b0-d854-4847-a251-297f21884909" />


### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
