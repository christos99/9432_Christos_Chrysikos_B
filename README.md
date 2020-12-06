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
**STATS:**
* [stats.txt for the 2GHz]()  
* [stats.txt for the 4GHz](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/Benchmarks/spec_results_4GHz-32kB-4-64kB-4-2048kB-16-64/specbzip/stats.txt) 

In case we add another CPU the frequency is going to be 2GHz or what ever else we define as we run the simulation. 



 
Benchmark Files for 2GHz:[specbzip](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specbzip), [specmcf](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specmcf), [spechmmer](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/spechmmer), [specsjeng](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/specsjeng), [speclibm](https://github.com/christos99/9432_Christos_Chrysikos_B/tree/main/Files/Benchmarks/spec_results_1GHz-32kB-4-64kB-4-2048kB-16-64/speclibm)  
Benchmark Files for 4GHz:[specbzip](), [specmcf](), [spechmmer](), [specsjeng](), [speclibm]()


--------------------------------------------------------------------------------------------------------------------------------------------------------------



## Second Part

### 1. DIfferent Configurations:

**1GHz-64kB-2-32kB-2-512kB-8-64:**

* L1 instruction cache size = 64kB
* L1 instruction cache associativity = 2
* L1 data cache size = 32kB
* L1 data cache associativity = 2
* L2 cache size = 512kB
* L2 cache associativity = 8
* cache line size = 64

CPI(average):2.7348436


**1GHz-128kB-1-64kB-1-1024kB-2-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 1
* L1 data cache size = 64kB
* L1 data cache associativity = 1
* L2 cache size = 1024kB
* L2 cache associativity = 2
* cache line size = 64

CPI(average):2.7343856

**1GHz-128kB-1-128kB-1-2048kB-2-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 1
* L1 data cache size = 1
* L1 data cache associativity 1
* L2 cache size = 2048kB
* L2 cache associativity = 2
* cache line size = 64

CPI(average):2.717256

**1GHz-128kB-8-64kB-8-1024kB-16-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 64kB
* L1 data cache size = 64kB
* L1 data cache associativity = 8
* L2 cache size = 1024kB
* L2 cache associativity = 16
* cache line size = 64

CPI(average):2.7174622

**1GHz-128kB-16-64kB-16-1024kB-32-64:**

* L1 instruction cache size = 128kB
* L1 instruction cache associativity = 16
* L1 data cache size = 64kB
* L1 data cache associativity = 16
* L2 cache size = 1024kB
* L2 cache associativity = 32
* cache line size = 64

CPI(average):2.7166182

**1GHz-256kB-4-256kB-4-4096kB-16-64:**

* L1 instruction cache size = 256kB
* L1 instruction cache associativity = 4
* L1 data cache size = 256kB
* L1 data cache associativity = 4
* L2 cache size = 4096kB
* L2 cache associativity = 16
* cache line size = 64

CPI(average):2.7005728  
(specjeng not included)  
CPI(average):1.61242525






[Results File](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/Results_spec_results_cpi_all.txt)

### 2. Graphs






Bibliography:
* [https://www.sciencedirect.com/topics/computer-science/set-associative-cache](https://www.sciencedirect.com/topics/computer-science/set-associative-cache)  
* [https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf](https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf)
* [Memory systems]()
* [Caches and Memory]()
