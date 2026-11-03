# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200🔢       01         12

|         1200                    |

#### Manual Calculations
<img width="1600" height="948" alt="WhatsApp Image 2026-10-30 at 8 56 43 AM" src="https://github.com/user-attachments/assets/855a4276-ddb2-4ca8-b3da-429ce9e5543e" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="641" height="423" alt="WhatsApp Image 2026-10-16 at 8 13 14 AM" src="https://github.com/user-attachments/assets/734679b0-1e3d-48ab-a8b3-0aa03a5c1661" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1600" height="900" alt="WhatsApp Image 2026-10-30 at 8 57 51 AM" src="https://github.com/user-attachments/assets/d6dcb5f5-834a-4255-97c0-11168115ed2c" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="636" height="431" alt="WhatsApp Image 2026-10-16 at 8 53 26 AM" src="https://github.com/user-attachments/assets/2227e8fb-a276-40a3-8ac3-6d5c17d681ff" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1600" height="807" alt="WhatsApp Image 2026-10-30 at 8 59 07 AM" src="https://github.com/user-attachments/assets/c045931a-2c44-44d2-85a1-10b40d3f3c5a" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="435" alt="WhatsApp Image 2026-10-23 at 8 30 01 AM" src="https://github.com/user-attachments/assets/e480b6c3-fe4b-4b35-80ca-48f01d638d2d" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1600" height="570" alt="WhatsApp Image 2026-10-30 at 9 00 51 AM" src="https://github.com/user-attachments/assets/6613a5d5-8be4-404c-b070-5aa0bc17b17c" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="635" height="427" alt="WhatsApp Image 2026-10-16 at 9 16 34 AM" src="https://github.com/user-attachments/assets/392288df-38a7-4307-a851-68ef2918e7db" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

