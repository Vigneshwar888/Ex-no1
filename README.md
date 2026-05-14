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

<img width="649" height="410" alt="WhatsApp Image 2026-05-14 at 11 18 34 AM" src="https://github.com/user-attachments/assets/25d3e815-45a5-4c71-93fc-34e0346cd913" />


#### Manual Calculations

(<img width="732" height="329" alt="WhatsApp Image 2026-05-14 at 11 21 49 AM" src="https://github.com/user-attachments/assets/ea836bcc-e2bb-48a5-aa10-094f1ecab2f3" />

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="727" height="498" alt="WhatsApp Image 2026-05-14 at 11 19 10 AM" src="https://github.com/user-attachments/assets/b21530aa-6ccd-4e14-be7b-caa8add8f2cc" />


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

<img width="689" height="348" alt="WhatsApp Image 2026-05-14 at 11 19 30 AM" src="https://github.com/user-attachments/assets/64d7acb5-86a1-4fba-a8e8-32e095b7c18f" />

#### Manual Calculations

<img width="434" height="394" alt="WhatsApp Image 2026-05-14 at 11 19 48 AM" src="https://github.com/user-attachments/assets/3f5ca59d-3799-4c37-8fa9-2804cc8d4ccd" />


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="720" height="354" alt="WhatsApp Image 2026-05-14 at 11 20 08 AM" src="https://github.com/user-attachments/assets/11f48f79-bee3-494d-a926-e23779dfccc3" />

  
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

<img width="730" height="290" alt="WhatsApp Image 2026-05-14 at 11 20 27 AM" src="https://github.com/user-attachments/assets/ba1f37c9-7dca-4649-b726-4859608f52d7" />
                |                          |

#### Manual Calculations

<img width="464" height="401" alt="WhatsApp Image 2026-05-14 at 11 20 48 AM" src="https://github.com/user-attachments/assets/becb7538-9fc5-4b1e-949f-0511ed841747" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="794" height="418" alt="WhatsApp Image 2026-05-14 at 11 21 17 AM" src="https://github.com/user-attachments/assets/627e303e-a352-4f33-b47b-8eeeb5ba0e42" />



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

<img width="649" height="410" alt="WhatsApp Image 2026-05-14 at 11 18 34 AM" src="https://github.com/user-attachments/assets/4a6d8614-d19f-486c-a869-cfd7b69c1d0b" />

#### Manual Calculations

<img width="732" height="329" alt="WhatsApp Image 2026-05-14 at 11 21 49 AM" src="https://github.com/user-attachments/assets/a4afb272-3e55-491c-83c7-6d7d32809693" />


## OUTPUT FROM MASM SOFTWARE

<img width="838" height="453" alt="WhatsApp Image 2026-05-14 at 11 21 30 AM" src="https://github.com/user-attachments/assets/02adc087-8901-4ebb-bc28-8e3d9d89e137" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

