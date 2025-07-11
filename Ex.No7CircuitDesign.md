# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:  22-04-25                                                                         
### REGISTER NUMBER : 212222040118
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
```
xor(0,1,1).
xor(0,0,0).
xor(1,0,1).
xor(1,1,0).
and(1,1,1).
and(0,0,0).
and(0,1,0).
and(1,0,0).
not(0,1).
not(1,0).
or(0,1,1).
or(1,0,1).
or(0,0,0).
or(1,1,1).
halfadder(A,B,Sum,Carry):-
    xor(A,B,Sum),
    and(A,B,Carry).
halfsubtractor(A,B,Diff,Carry):-
    xor(A,B,Diff),
    not(A,C),
    and(C,B,Carry).
fulladder(A,B,Cin,S,Cout):-
    xor(A,B,X),
    xor(X,Cin,S),
    and(X,Cin,Y),
    and(A,B,Z),
    or(Y,Z,Cout).
```

### Output:
![image](https://github.com/user-attachments/assets/6b20d0ee-2e3d-4ecc-807d-9b92ecd67ee5)
![image](https://github.com/user-attachments/assets/4876730f-6714-465a-b018-ccf5ccf0e39a)
![image](https://github.com/user-attachments/assets/6d1f7ea9-4330-4776-95e4-0c2a9405bdd4)

### Result:
Thus the truth table of circuit verified sucessfully.
