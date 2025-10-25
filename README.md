SKILL ASSIGNMENT-1

PROGRAM:
Write an assembly language program in 8051 to generate a 2 ms delay using Timer 0 in Mode 1 and toggle an LED connected to Port 2.0.


APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
ORG 0H        
MOV P2, #00H  

HERE:  
    
    MOV TH0, #0F8H
    MOV TL0, #030H

 1
    MOV TMOD, #01H
    SETB TR0         

WAIT:  
    JNB TF0, WAIT
    CLR TR0          
    CLR TF0          
    CPL P2.0         

    SJMP HERE        
END

```
OUTPUT:

![WhatsApp Image 2025-10-25 at 10 03 47_c2455176](https://github.com/user-attachments/assets/eb77dfc0-82eb-4610-afae-c43606b16d72)

![WhatsApp Image 2025-10-25 at 10 03 54_cab5ae2a](https://github.com/user-attachments/assets/afc18a62-a9f3-444d-a300-503c358b0552)


RESULT:

THUS THE PROGRAM TO calculate the sum of 5 numbers stored sequentially in memory and store the result in a another memory location is executed. 
