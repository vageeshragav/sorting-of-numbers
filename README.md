# sorting-of-numbers
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

```asmORG 0000H

MOV R7,20H
DEC R7

UP: MOV R6,R7
MOV R0,#30H

NEXT: MOV A,@R0
INC R0
MOV B,@R0

CJNE A,B,CHECK
SJMP SKIP

CHECK: JC SKIP

MOV @R0,A
DEC R0
MOV @R0,B
INC R0

SKIP: DJNZ R6,NEXT
DJNZ R7,UP

HERE: SJMP HERE

END





```
## OUTPUT(Ascending order)
```asm
<img width="587" height="437" alt="image" src="https://github.com/user-attachments/assets/c86f62b7-2419-42b1-bba2-56895acd1f58" />
<img width="442" height="188" alt="image" src="https://github.com/user-attachments/assets/78a45a94-76f4-4379-8ae9-7149daff81ab" />

ORG 0000H

MOV R7,20H
DEC R7

UP: MOV R6,R7
MOV R0,#30H

NEXT: MOV A,@R0
INC R0
MOV B,@R0

CJNE A,B,CHECK
SJMP SKIP

CHECK: JC SKIP

MOV @R0,A
DEC R0
MOV @R0,B
INC R0

SKIP: DJNZ R6,NEXT
DJNZ R7,UP

HERE: SJMP HERE

END

---

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

```asmORG 0000H

MOV R7,20H
DEC R7

UP: MOV R6,R7
MOV R0,#30H

NEXT: MOV A,@R0
INC R0
MOV B,@R0

CJNE A,B,CHECK
SJMP SKIP

CHECK: JC SKIP

MOV @R0,A
DEC R0
MOV @R0,B
INC R0

SKIP: DJNZ R6,NEXT
DJNZ R7,UP

HERE: SJMP HERE

END




```
## OUTPUT(Descending order)
```asm
<img width="587" height="437" alt="image" src="https://github.com/user-attachments/assets/c86f62b7-2419-42b1-bba2-56895acd1f58" />
<img width="442" height="188" alt="image" src="https://github.com/user-attachments/assets/78a45a94-76f4-4379-8ae9-7149daff81ab" />


<img width="442" height="188" alt="image" src="https://github.com/user-attachments/assets/b92ec1c5-ecd4-4602-8786-6e375b371557" />

---
## RESULT:
Thus the sorting of given data was done using 8051 keil software.

