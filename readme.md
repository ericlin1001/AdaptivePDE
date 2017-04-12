# Adpative Parallel Differential Evolution for PEC
A parallel program running in cluster to solve Power Electronic Circuit (PEC) problem, https://github.
com/ericlin1001/AdaptivePDE

# What has it achieved?
* Parallelized Differential Evolution (DE) algorithm, achieved approximately 50% parallel efficiency
* Support for adaptively distributing tasks among cores, efficiently utilizing all CPU cores
* Defined an unified Json format for setting up all DE arguments
* Published corresponding paper: Parallel Differential Evolution Based on Distributed Cloud Computing Resources for Power Electronic Circuit Optimization in GECCO '16 Companion


# What's purpose of the experiment?
1. Adaptively assign tasks among all cores.
2. Achieve the theoretical limit of speedup ratio.
3. On different setting of CPUs, achieve the least time.


# About the experiment
## Cluster Setting&Info:  
```
All the computers:
	ComputerNo.	Note	hasChecked  
	1			MainHost   
	2~23		i3CPU	2cores,8G(No2)  
	55~58		i5CPU  
	59~95		i7CPU	4cores,4G(No59)  
	96~200		i5CPU	4cores,12G(No96)  
```

```
	i3: 40cores
	i5: 400cores
	i7: 140cores
```

```
	No.		Memory  
	96~104	16G  
	145~131	32G  
	others	unknow
```

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

## What's the result i want?
* If the computers are different, my algorithm is better.
* If the computers are all the same, my algorithm is not worser.

## Experimental Setting
### In last paper
Runing on 1,2,6,26,51,101 cores i5.

### In current paper
Notice: Always land the master node in high-performance computer(i7).

1. When computers are different:

	Purpose: Keep each core processes more data, such that the differences in cpu can be realized.
```
			Exp1	Exp2
			cores	cores
	i3		2		10
	i5		2		10
	i7		2		10
	total	6		30
```

2. When computers are the same:
```
			Exp1	Exp2	Exp3	Exp4
			cores	cores	cores	cores
	i5		5		6		30		31
```

### How to do that:
Compare serial version with my version over the above 2 experimental settings.
That means, get the last version program and get its result over the settings, and implement my version and get my results. And finally, analyse two results, and get the conclusion.




