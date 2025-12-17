# JKFLIPFLOP-USING-IF-ELSE

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**
A JK flip-flop is a sequential circuit that stores one bit of data and updates its output on the clock edge. It has two inputs, J and K, and behaves as an improved version of the SR flip-flop. Its operation is defined as:

J = 0, K = 0: No change

J = 0, K = 1: Reset

J = 1, K = 0: Set

J = 1, K = 1: Toggle

In the given Verilog program, the output q updates on the positive edge of the clock based on the JK logic expression, and qbar always remains the complement of q. This allows the flip-flop to reliably store, reset, set, or toggle its state depending on the input conditions.
**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**
```
Create a new project in Quartus and add a new Verilog file containing the JK flip-flop code.

Save the file, include it in the project, and compile the design.

Create a new University Program VWF for simulation.

Insert the signals j, k, clk, q, and qbar using Node Finder.

Apply a clock waveform to clk and manually draw input patterns for j and k to test all JK conditions.

Save the waveform file and start functional simulation.

Observe the outputs q and qbar and verify correct JK flip-flop behavior based on the input combinations.

If you need, I can also give short theory or a brief result.
```
**PROGRAM**
```
module ex5(j,k,clk,q,qbar);
input j,k,clk;
output reg q,qbar;
initial 
begin
q=1'b0;
q=1'b1;
end 

always @(posedge clk)
begin 
q<=(j&~q)|(~k&q);
qbar<=~q;
end
endmodule
```
.Developed by: Samantha Shree SV
RegisterNumber:25017585


**RTL LOGIC FOR FLIPFLOPS**

<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/3e7dacfe-486a-4d19-8993-1294a9092c9f" />


**TIMING DIGRAMS FOR FLIP FLOPS**
<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/b0a65d3b-13be-4427-8bec-b53b379cd5dd" />

**RESULTS**
Thus the JK flipflop using verilog and validating their functionality is executed.
