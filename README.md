# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JNC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4300H;
HLT;
```

## Output:
<img width="1788" height="687" alt="Screenshot 2025-09-12 152214" src="https://github.com/user-attachments/assets/88c42144-b6d3-4bb3-a986-a425c18f262a" />



<img width="504" height="469" alt="Screenshot 2025-09-12 152226" src="https://github.com/user-attachments/assets/be37b823-1d80-4d7d-b25b-ab5c1c583c7b" />

## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H;
MOV C,A;
LXI H,4201H;
MOV A,M;
INX H;
DCR C;
LOOP:CMP M;
JC NEXT;
MOV A,M;
NEXT:INX H;
DCR C;
JNZ LOOP;
STA 4301H;
HLT;
```

## Output:
<img width="1791" height="753" alt="Screenshot 2025-09-12 191314" src="https://github.com/user-attachments/assets/aaf80105-74bd-4ab0-ba4d-630f3620690c" />
<img width="523" height="491" alt="Screenshot 2025-09-12 191323" src="https://github.com/user-attachments/assets/9849c4dd-9f99-4858-9cb6-e37ec4ffa28b" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
