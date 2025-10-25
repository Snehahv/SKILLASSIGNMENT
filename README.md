SKILL ASSIGNMENT-2

PROGRAM:
Write an assembly language program in 8086 to calculate the sum of 5 numbers stored sequentially in memory and store the result in a another memory location.


APPARATUS REQUIRED:

LAPTOP WITH KEIL SOFTWARE

PROGRAM:
```
DATA SEGMENT
    NUMBERS DB 10H, 20H, 30H, 40H, 50H  
    RESULT DW ?                         
DATA ENDS

CODE SEGMENT
ASSUME DS:DATA, CS:CODE

START:
    MOV AX, DATA      
    MOV DS, AX

    LEA SI, NUMBERS   
    MOV CX, 05H       
    XOR AX, AX        

SUM_LOOP:
    MOV BL, [SI]      
    ADD AL, BL        
    INC SI            
    LOOP SUM_LOOP     

    MOV RESULT, AX    

    MOV AH, 4CH       
    INT 21H

CODE ENDS
END START
```
OUTPUT:

<img width="634" height="388" alt="image" src="https://github.com/user-attachments/assets/73cce0a7-3765-4698-8e56-8fe325ebeb7f" />


RESULT:

THUS THE PROGRAM TO calculate the sum of 5 numbers stored sequentially in memory and store the result in a another memory location is executed. 
