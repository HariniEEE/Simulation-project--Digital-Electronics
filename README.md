# TITTLE
To Design and simulate mod 7 synchronous upcounter with JK flip flop using Verilog.


# THEORY
Synchronous Counters: It means that all flip-flops are clocked concurrently. The clock pulses drive the clock input of each flip-flop together hence there is no propagation delay.

Mod-7 Counter Synchronous Counter: This have seven counter states. The counter design table for such counter shows the four flip-flop and their states also (0 to 7 states), as in table (a), the 8 inputs needed for the four flip-flops. The flip-flop inputs needed to step up the counter from the current to the next state have been worked out along with the assist of the excitation table illustrated in the table.


# LOGIC DIAGRAM

![jkff](https://github.com/HariniEEE/Simulation-project--Digital-Electronics/assets/128949246/30cdae64-3877-4557-8b20-909a2d46b93b)


# NETLIST DIAGRAM

![jk net](https://github.com/HariniEEE/Simulation-project--Digital-Electronics/assets/128949246/9f965174-5b0a-4640-9e53-b084ad73ba4e)


# TIMING DIAGRAM

![jk timing](https://github.com/HariniEEE/Simulation-project--Digital-Electronics/assets/128949246/8e0ac085-3e25-43b4-b8e3-a9bb73bdbd18)


# PROGRAM

module modfivecounter(q, qbar, j, k,clk, rst, pr);
output [2:0] q, qbar;
input clk, j, k;
input rst, pr;
wire a;
nand n1(a,q[1],q[2]);
JKFF_Pos_Edge jkff0(q[o],
qbar[0],j,k,clk,a,pr);
JKFF_PoS_Edge jkff1 (q[1],
qbar[1],j,k,qbar[0],a,pr);
JKFF_PoS_Edge jkff3(q[2],

# REFERENCE

https://circuitverse.org/users/99459/projects/mod-7-synchronous-counter-using-jk-flip-flop-f10252f6-381f-4538-af6e-79138f761b47

