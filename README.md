### **Day 19: Asynchronous Counter**  

#### **Concept Overview**  
An **Asynchronous Counter**, also called a **Ripple Counter**, is a **sequential circuit** where the flip-flops do not receive the same clock signal simultaneously. Instead, the **output of one flip-flop acts as the clock for the next flip-flop**, causing a delay (ripple effect).  

#### **Detailed Explanation**  
- Uses **JK or T flip-flops** connected in series.  
- The **first flip-flop is triggered by an external clock**, while the remaining flip-flops are triggered by the output of the previous one.  
- The number of flip-flops determines the **modulus (MOD) of the counter**, i.e., a **n-bit counter counts from 0 to (2^n - 1)**.  

#### **Example: 3-bit Asynchronous Counter (MOD-8 Counter)**  
- **Uses 3 T flip-flops** (Toggled on every falling edge).  
- **Counts from 000 to 111 (0 to 7 in decimal)** and then resets.  

#### **Truth Table (MOD-8 Counter)**  

| Clock | Q2 | Q1 | Q0 | Decimal |  
|-------|----|----|----|---------|  
| 0     | 0  | 0  | 0  | 0       |  
| 1     | 0  | 0  | 1  | 1       |  
| 2     | 0  | 1  | 0  | 2       |  
| 3     | 0  | 1  | 1  | 3       |  
| 4     | 1  | 0  | 0  | 4       |  
| 5     | 1  | 0  | 1  | 5       |  
| 6     | 1  | 1  | 0  | 6       |  
| 7     | 1  | 1  | 1  | 7       |  
| 8     | 0  | 0  | 0  | 0 (Reset) |  

#### **Boolean Expressions**  
- `Q0 = Toggled on each clock cycle`  
- `Q1 = Toggled when Q0 = 1`  
- `Q2 = Toggled when Q1 = 1`  

#### **Applications**  
Used in **frequency dividers, digital clocks, event counters, and timers** where clock synchronization is not crucial.  

#### **Execution Steps**  
1. Open **QuestaSim, ModelSim, Xilinx ISE, or Vivado**.  
2. Write the **Verilog code** for a 3-bit asynchronous counter.  
3. Create a **testbench** to simulate the counter operation.  
4. Check the **waveform output** to verify the counting sequence.  

#### **Real-World Example for Practice**  
Design a **4-bit Ripple Counter** (MOD-16) that counts from 0 to 15 using **4 T flip-flops**.  

#### **Further Enhancements**  
- Implement a **4-bit Asynchronous Counter (MOD-16)**.  
- Add an **active-low Reset** to restart counting when needed.  
