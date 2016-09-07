#Adpative Parallel Differential Evolution for PEC
Well, this is a basic project plan.

#What's purpose of the paper? Why do i want to write it?
1.It features on adaptive assgining task.
2.Achieving the theoretical limit of speedup ratio.
3.On different setting cpu, we achive the best time.


#What do I want from the program? What's the program for?
Cluster setting:  
ComputerNo. Note hasChecked  
1		MainHost   
2~23	i3CPU	2cores,8G(No2)  
55~58	i5CPU  
59~95	i7CPU	4cores,4G(No59)  
96~200	i5CPU	4cores,12G(No96)  

* i3 cores~:40  
* i5 cores~:400  
* i7 cores~:140  

---
No.		Memory  
96~104	16G  
145~131	32G  

```
No.				InTheSameSwitch
2~18			1
19~23,96~108	2
146~163			3
128~145			4
183~200			5
164~182			6
109~127			7
```

---
Run one serial program on each computer:
one core's performance: i7>i5>i3


---
Data needed for paper:
Compared with universal distribution in following setting:

#What's the result i want?(Vision)
* If the computers are different, my algorithm is better.
* If the computers are all the same, my algorithm is not worser.
I want prove that my version is better, over all cases.

#Experimental Setting
1,2,6,26,51,101
Always land the master node in high-performance computer(i7).
1. Computers are different:
Purpose:Keep each core processes more data, such that the differences in cpu can be realized.
```
		cores	cores
i3		2		10
i5		2		10
i7		2		10
total	6		30
```

2. Computers are the same:
```
		cores	cores	cores	cores
i5		5		6		30		31
```


#How to do that:
Compare serial version with my version over 2 experimental settings.








