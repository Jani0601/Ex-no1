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
<img width="1280" height="1093" alt="image" src="https://github.com/user-attachments/assets/3f189a00-0162-4e5a-b5ac-2ea455060dfb" />


#### Manual Calculations
![WhatsApp Image 2026-02-07 at 8 18 01 AM](https://github.com/user-attachments/assets/fe9b07db-8815-454b-8e92-9f11b82af767)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="655" height="447" alt="image" src="https://github.com/user-attachments/assets/120cde55-9af9-4d1d-9f58-80f39f279438" />


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

![WhatsApp Image 2026-02-07 at 8 17 02 AM](https://github.com/user-attachments/assets/1255c146-3524-4f09-8407-36358130b859)


#### Manual Calculations
![WhatsApp Image 2026-02-07 at 8 18 12 AM](https://github.com/user-attachments/assets/8fa57593-36c7-41b0-87ba-b2edf75cbe15)





## OUTPUT SCREEN FROM MASM SOFTWARE


<img width="638" height="431" alt="image" src="https://github.com/user-attachments/assets/8e385997-b435-4123-8aaa-4d7cac8d25d6" />



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
![WhatsApp Image 2026-02-07 at 8 17 31 AM](https://github.com/user-attachments/assets/333c66d1-efc1-43b6-bee8-a4c14ab0c645)




#### Manual Calculations


<img width="1599" height="606" alt="image" src="https://github.com/user-attachments/assets/635c2480-ec46-416e-8da0-a0d073625fac" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="642" height="424" alt="image" src="https://github.com/user-attachments/assets/b84231e0-f979-4d7e-bd6e-1f417827eebe" />


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

![WhatsApp Image 2026-02-07 at 8 17 47 AM](https://github.com/user-attachments/assets/6d2c5310-a03c-430c-9d82-adfe67c5cc1b)



#### Manual Calculations

![WhatsApp Image 2026-02-07 at 8 18 23 AM](https://github.com/user-attachments/assets/b3baf251-200a-4588-b482-fa7ef07422ac)




---
## OUTPUT FROM MASM SOFTWARE

<img width="638" height="431" alt="image" src="https://github.com/user-attachments/assets/348a598b-5463-4042-8b5e-1bae679eb0cc" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

