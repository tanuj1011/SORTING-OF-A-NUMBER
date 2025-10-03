## Aim
To write and execute an Assembly Language Program for sorting data in Ascending and  descending order using 8051 microcontroller on Keil software.
---

## Apparatus Required
- Personal Computer  
- Keil µVision software  
---

## Algorithm(ASCENDING ORDER)
1. Initialize the register **R7** with count (number of elements).  
2. Get the first two elements into two registers.  
3. Compare the two elements:  
   - If the value in register **R0** is lower, exchange **A** and **R0** data.  
   - Otherwise, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0** → if yes, move the register **R0 & A**.  
5. Increment pointer and decrement **R7**.  
6. If **R7 ≠ 0**, repeat from Step 2.  
7. Otherwise, stop the program.  
---

## Program (Ascending order)
ORG 000H
LOOP1:MOV R0,#40H
MOV R6,30H
LOOP:MOV A, @R0
INC R0
MOV B, @R0
CJNE A,B,NEXT 
NEXT:JC DOWN
MOV @R0,A
DEC R0
MOV @R0,B
INC R0
DOWN: DJNZ R6, LOOP
MOV R1, #02H
DJNZ R1, LOOP1
END

## OUTPUT(Ascending order)
![WhatsApp Image 2025-09-24 at 11 25 42_6b1bc3f3](https://github.com/user-attachments/assets/55727a01-a224-4798-abeb-8407f5296f22)


## Algorithm(Descending order)
1. Initialize the register **R7** with count.  
2. Get first two elements in two registers.  
3. Compare the two elements of data:  
   - If the value of **R0** register is high, then exchange **A** and **R0** data.  
   - Else, increment pointer and decrement register **R7**.  
4. Check if **R7 = 0**, then move the contents of **R0** and **A**.  
5. Again increment pointer and decrement **R7**.  
6. Check if **R7 = 0**:  
   - If **No**, repeat the process from Step 2.  
   - If **Yes**, stop the program.  
---
## Program (Descending order)

ORG 000H
LOOP1:MOV R0,#40H
MOV R6,30H
LOOP:MOV A, @R0
INC R0
MOV B, @R0
CJNE A,B,NEXT 
NEXT:JNC DOWN
MOV @R0,A
DEC R0
MOV @R0,B
INC R0
DOWN: DJNZ R6, LOOP
MOV R1, #02H
DJNZ R1, LOOP1
END

## OUTPUT(Descending order)
![WhatsApp Image 2025-09-24 at 11 04 56_748508a5](https://github.com/user-attachments/assets/22d98d53-69d4-492d-a892-0ab4564a0cfb)

---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

