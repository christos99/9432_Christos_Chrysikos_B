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
* 







### 2. Graphs






Bibliography:
* [https://www.sciencedirect.com/topics/computer-science/set-associative-cache](https://www.sciencedirect.com/topics/computer-science/set-associative-cache)  
* [https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf](https://courses.cs.washington.edu/courses/cse378/09au/lectures/cse378au09-20.pdf)
* [Memory systems]()
* [Caches and Memory]()
