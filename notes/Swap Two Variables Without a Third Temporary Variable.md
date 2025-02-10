#mathematics #programming #logic 

This is done using XOR logic. (x3 using three times)

| A   | B   | O   |
| --- | --- | --- |
| 1   | 1   | 0   |
| 1   | 0   | 1   |
| 0   | 1   | 1   |
| 0   | 0   | 0   |

P  = 1 0 1 0
Q = 0 0 1 1
.......................
P  = 1 0 0 1     <---- XOR of P and Q assign to P
.......................
Q = 1 0 1 0     <---- XOR of Q and new P assign to Q
.......................
P  = 0 0 1 1     <---- XOR of new P and new Q assign to P
...................................................................................................................
Now, above Q and P values are swapped.

