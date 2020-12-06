# 9432_Christos_Chrysikos_B
2nd Lab on gem-5 simulations Computer Architecture



## First Part

### 1.(Basic Paramters of the CPU):

#### Cache**
**L1i:**
* Size =
* Assoc =

**L1d:**
* Size =
* Assoc =

**L2:**

**Cache Line**
* Size = 
### 2. (SIM_SECONDS, CPI, MISS RATES):

**SIM_SECONDS=**

**CPI =**  

**MISS RATES**
* L1I = 
* L1D =
* L2 = 

### 3.(CPU CLOCK = 2GHz)

When we run the simualtion with cpu-clock = 2GHz we see that the system.clk_domain.clock = 1000 but the cpu_cluster.clk_domain.clock = 500. If we increase the cpu-clock=4GHz then cpu_cluster.clk_domain.clock= 250 so I suppose that whatever is clock cycle in GHz it is 2 or the last case 4 times faster than the system clock.[stats.txt for the 2GHz]()  [stats.txt for the 4GHz]()  
In case we add another CPU the frequency is going to be 2GHz or what ever we define when we run the simulation. 



Reference Files: [config.json](), [config.ini](), [stats.txt]()  
Benchmark Files for 2GHz:[specbzip](), [specmcf](), [spechmmer](), [specsjeng](), [speclibm]()  
Benchmark Files for 4GHz:[specbzip](), [specmcf](), [spechmmer](), [specsjeng](), [speclibm]()


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






[Results File](https://github.com/christos99/9432_Christos_Chrysikos_B/blob/main/Files/CPI%20-%20Results-All/Results_spec_results_cpi_all.txt)

### 2. Graphs






Bibliography:
* [https://www.sciencedirect.com/topics/computer-science/set-associative-cache](https://www.sciencedirect.com/topics/computer-science/set-associative-cache)  
* [https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf](https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf)
* [Memory systems]()
* [Caches and Memory]()
