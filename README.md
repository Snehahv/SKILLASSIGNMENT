SKILL ASSIGNMENT-2

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

![WhatsApp Image 2025-10-25 at 10 03 47_34931c21](https://github.com/user-attachments/assets/74f11fb6-8cb4-4bf6-82f0-3c00a59cb806)

![WhatsApp Image 2025-10-25 at 10 03 54_b97d0b0c](https://github.com/user-attachments/assets/eed611e8-97a4-42e4-b233-b9f6c4817092)

RESULT:

THUS THE PROGRAM generate 2ms delay is executed.
