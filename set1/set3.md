**Teleportation**  
Time Limit: 1s  
 Memory Limit: 256 MB  
**Problem Description**  
Mr. Dengklek is trapped inside a one-floor building owned by four-dimensional creatures from another galaxy. The building contains N rooms. The rooms are numbered A0, A1, A2, ..., AN-1. However, there may be more than one room having the same number.

Initially, Mr. Dengklek is placed in a room numbered x. He then uses his teleportation machine, which works as follows : 

* As long as Mr. Dengklek is inside a room, he will continue using the teleportation machine and keep moving from one room to another.  
* Whenever Mr. Dengklek is in a room numbered k, he will move to the room numbered Ak.

Help Mr. Dengklek determine how many times he moves before he eventually becomes trapped in the same room forever and can no longer move anywhere else using his teleportation machine.  
---

**Input Format**  
N x  
A0 A1 A2 … AN-1  
---

**Output Format**  
Print a single integer representing the number of moves made.  
---

**Sample Input**  
4 1  
1 2 3 3  
---

**Sample Output**  
3  
---

**Explanation**  
Initially, Mr. Dengklek is in room 1\.

* He moves to room 2  
* Then moves to room with labeled number 3  
* Then moves to room with labeled number 3 again

After that, he cannot move anywhere else anymore.  
   
   
**Constraint**  
Open Test Case

Hash\_map=unorderlist\<int,int\>timeMachine;  
For i \= 0; i\<x; i++{  
timeMachine.list

A0 \= 1  
A1 \= 2  
A2 \= 3  
A3 \= 3

