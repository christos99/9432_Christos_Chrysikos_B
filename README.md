# 9432_Christos_Chrysikos_B
2nd Lab on gem-5 simulations Computer Architecture

--------------------------------------------------------------------------------------------------------------------------------------------------------------

## First Part


### 1.(Basic Paramters of the CPU):

#### Cache


* L1I:
  * Size = 32kB
  * Assoc = 2

* L1D:
  * Size = 64kB
  * Assoc = 2

* L2:
   * Size = 2MB
   * Assoc = 8

* Cache Line:
  * Size = 64


Reference File:[here](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/References/Options.py)

--------------------------------------------------------------------------------------------------------------------------------------------------------------


### 2. (SIM_SECONDS, CPI, MISS RATES):

#### specbzip

  * SIM_SECONDS = 0.160359

  * CPI = 1.603595

  * MISS RATES
    * L1I = 0.000075
    * L1D = 0.014123
    * L2 = 0.295235

#### specmcf

* SIM_SECONDS = 0.123265

* CPI = 1.232645

* MISS RATES
  * L1I = 0.019046
  * L1D = 0.002062
  * L2 = 0.067668

#### spechmmer

* SIM_SECONDS = 0.118517

* CPI = 1.185174

* MISS RATES**
  * L1I = 0.000212
  * L1D = 0.001619
  * L2 = 0.078295

#### speclibm

* SIM_SECONDS = 0.262262

* CPI = 2.622616

* MISS RATES 
  * L1I = 0.000095	
  * L1D =0.060972
  * L2 = 0.999978

#### specsjeng

* SIM_SECONDS = 0.705640

* CPI = 2.622616

* MISS RATES
  * L1I = 	0.000020
  * L1D = 0.121831
  * L2 = 0.999940

Date gathered in a [file](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/spec_results_1GHz-default.txt)
* GRAPHS:
  * [CPI GRAPH](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Graphs/CPI.pdf)  
  * [SIM SECONDS GRAPH](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Graphs/SIM_SECONDS.pdf)  
  * [L1I MISS GRAPH](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Graphs/L1I_Miss_Rate.pdf)  
  * [L1D MISS GRAPH](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Graphs/L1D_Miss_Rate.pdf)  
  * [L2 MISS GRAPH](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Graphs/L2_Miss_Rate.pdf)  
  
  Reference Files:
* [specbzip](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specbzip)
* [spechmmer](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/spechmmer)
* [speclibm](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/speclibm)
* [specmcf](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specmcf)
* [specsjeng](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specsjeng)


--------------------------------------------------------------------------------------------------------------------------------------------------------------



### 3.(CPU CLOCK = 2GHz)

When we run the simualtion with cpu-clock = 2GHz we see that the system.clk_domain.clock = 1000 but the cpu_cluster.clk_domain.clock = 500. If we increase the cpu-clock=4GHz then cpu_cluster.clk_domain.clock= 250 so I suppose that whatever the clock cycle is in GHz it is two or in the last case four times faster than the systems clock.  
* **SIM_SECONDS**
  * 1GHz(average) = 0.2740086s [spec_results_1GHz](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/RESULTS_1_2_4_GHz/spec_results_1GHz-latest-all.txt)
  * 2GHz(average) = 0.1788366s [spec_results_2GHz](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/RESULTS_1_2_4_GHz/spec_results_2GHz-default.txt)
  * 4GHz(average) = 0.1316488s [spec_results_4GHz](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/RESULTS_1_2_4_GHz/spec_results_4GHz-default.txt)

As we review the sim_seconds for each individual simulation, we can easily extract that there is definetely increased performance as we increase the clock speeds .On the contrary we can't observe any type of scalabilty to the clock increase. For example for the first simulation we have a clock speed of 1GHz and the sim_seconds are 0.274s in average, as we double the clock speed we expect to see half the runntime but that it is not the case here. The sim_seconds for 2GHz are 0.1788s which is greater than 0.274/2 = 0.137s and we procceed with a greater clock increase such as 4GHz we see that the change in sim_seconds is even smaller sim seconds = 0.1316488s which is much greater than 0.1788/2 = 0.0894s and even greater than 0.137/2 = 0.0685s which is the 1/4 of the 1GHz runtime.  

Sources that say more about clock speed and general cpu performance increase:
[Factors affecting processor performance](https://isaaccomputerscience.org/concepts/sys_arch_performance)

* **STATS:**
  * [stats.txt for the 2GHz](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_2GHz-32kB-4-64kB-4-2048kB-16-64)  
  * [stats.txt for the 4GHz](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/specbzip/stats.txt) 

In case we add another CPU the frequency is going to be 2GHz or what ever else we define as we run the simulation. 



 
Benchmark Files for 2GHz:[specbzip](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specbzip), [specmcf](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specmcf), [spechmmer](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/spechmmer), [specsjeng](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specsjeng), [speclibm](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/speclibm)  
Benchmark Files for 4GHz:[specbzip](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/specbzip), [specmcf](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/spechmmer), [spechmmer](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/speclibm), [specsjeng](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/specmcf), [speclibm](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/specsjeng)


--------------------------------------------------------------------------------------------------------------------------------------------------------------



## Second Part

### 1. DIfferent Configurations:

**System 1** 

**1GHz-64kB-2-32kB-2-512kB-8-64:**

* L1 instruction cache size = 64kB
* L1 instruction cache associativity = 2
* L1 data cache size = 32kB
* L1 data cache associativity = 2
* L2 cache size = 512kB
* L2 cache associativity = 8
* cache line size = 64

CPI(average):2.7348436  
[BENCHMARKS](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-64kB-2-32kB-2-512kB-8-64)

**System 2**  

**1GHz-128kB-1-64kB-1-1024kB-2-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 1
* L1 data cache size = 64kB
* L1 data cache associativity = 1
* L2 cache size = 1024kB
* L2 cache associativity = 2
* cache line size = 64

CPI(average):2.7343856  
[BENCHMARKS](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-128kB-1-64kB-1-1024kB-2-64)

**System 3**  

**1GHz-128kB-1-128kB-1-2048kB-2-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 1
* L1 data cache size = 1
* L1 data cache associativity 1
* L2 cache size = 2048kB
* L2 cache associativity = 2
* cache line size = 64

CPI(average):2.717256  
[BENCHMARKS](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-128kB-1-128kB-1-2048kB-2-64)

**System 4**  

**1GHz-128kB-8-64kB-8-1024kB-16-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 64kB
* L1 data cache size = 64kB
* L1 data cache associativity = 8
* L2 cache size = 1024kB
* L2 cache associativity = 16
* cache line size = 64

CPI(average):2.7174622  
[BENCHMARKS](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-128kB-8-64kB-8-1024kB-16-64)

**System 5**  

**1GHz-128kB-16-64kB-16-1024kB-32-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 16
* L1 data cache size = 64kB
* L1 data cache associativity = 16
* L2 cache size = 1024kB
* L2 cache associativity = 32
* cache line size = 64

CPI(average):2.7166182  
[BENCHMARKS](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-128kB-16-64kB-16-1024kB-32-64)

**System 6**  

**1GHz-256kB-4-256kB-4-4096kB-16-64:**

* L1 instruction cache size = 256kB
* L1 instruction cache associativity = 4
* L1 data cache size = 256kB
* L1 data cache associativity = 4
* L2 cache size = 4096kB
* L2 cache associativity = 16
* cache line size = 64

CPI(average):2.7005728  

  
CPI(average)(specjeng not included):1.61242525

I've noticed that that specjeng benchmark increased dramtically the cpi avergae and that makes me wonder if there are any errors.  
[BENCHMARKS](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-256kB-4-256kB-4-4096kB-16-64)




[Results File](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/Results_spec_results_cpi_all.txt)

### 2. Graphs






Bibliography:
* [https://www.sciencedirect.com/topics/computer-science/set-associative-cache](https://www.sciencedirect.com/topics/computer-science/set-associative-cache)  
* [https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf](https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf)
* [Memory systems](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/References/memory-systems.pdf)
* [Caches and Memory](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/References/lecture_caches-handout.pdf)
* [Science Magazine](https://www.extremetech.com/extreme/188776-how-l1-and-l2-cpu-caches-work-and-why-theyre-an-essential-part-of-modern-chips)


## Third Part

Custom Cache Prices: 
* L1i and L1d = 5.000$ per GB (considering manufacture and design)
* L2 = 2.500 per GB (easier to make than L1 cache)
* Assocativity = for every multiplication by two the cost doubles(for example: assoc = 2, cost = 2 | assoc = 4, cost = 4 etc) 
  lets say assoc = 2 then cost = 0.5$ dollars per core
* Cache line is not changed so I won't consider the cost  

**System 1 :**
Cost:
* L1 instruction cache size = 64kB : 0.32$
* L1 instruction cache associativity = 2 : 0.5$
* L1 data cache size = 32kB : 0.16$
* L1 data cache associativity = 2 : 0.5$
* L2 cache size = 512kB : 2.56$
* L2 cache associativity = 8 : 2$

Total Cost = 6.04$  

**System 2 :**
Cost:
* L1 instruction cache size = 128kB : 0.64$
* L1 instruction cache associativity = 1 : 0.25$
* L1 data cache size = 64kB : 0.32$
* L1 data cache associativity = 1 : 0.25$
* L2 cache size = 1024kB : 5.12$
* L2 cache associativity = 2 : 0.5$

Total Cost = 8.54$

**System 3 :**  
L1 instruction cache size = 128kB : 0.64$
L1 instruction cache associativity = 1 : 0.25$
L1 data cache size = 128 : 0.64$
L1 data cache associativity 1 : 0.25
L2 cache size = 2048kB : 10.24$
L2 cache associativity = 2 : 0.5$

Total cost = 12.52$


**System 4 :**  
L1 instruction cache size = 128kB : 0.64$
L1 instruction cache associativity = 8 : 2$
L1 data cache size = 64kB : 0.32$
L1 data cache associativity 8 : 2$
L2 cache size = 1024kB : 5.12$
L2 cache associativity = 16 : 4$

Total cost = 14.08$

**System 5 :**  
L1 instruction cache size = 128kB : 0.64$
L1 instruction cache associativity = 16 : 4$
L1 data cache size = 64kB : 0.32$
L1 data cache associativity 16 : 4$
L2 cache size = 1024kB : 5.12$
L2 cache associativity = 32 : 8$

Total cost = 22.08$


**System 6 :**  
L1 instruction cache size = 256kB : 1.28$
L1 instruction cache associativity = 4 : 1$
L1 data cache size = 256kB : 1.28$
L1 data cache associativity 4 : 1$
L2 cache size = 4096kB : 20.48$
L2 cache associativity = 16 : 4$

Total cost = 29.04$
