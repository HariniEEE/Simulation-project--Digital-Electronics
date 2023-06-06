# TITTLE

To Design and simulate mod 7 synchronous upcounter with JK flip flop using Verilog.

# THEORY

Synchronous Counters: It means that all flip-flops are clocked concurrently. The clock pulses drive the clock input of each flip-flop together hence there is no propagation delay.

Mod-5 Counter Synchronous Counter: This have five counter states. The counter design table for such counter shows the three flip-flop and their states also (0 to 5 states), as in table (a), the 6 inputs needed for the three flip-flops. The flip-flop inputs needed to step up the counter from the current to the next state have been worked out along with the assist of the excitation table illustrated in the table.


# LOGIC DIAGRAM

![jkff](https://github.com/anishkumar-Embedded/Simulation-project--Digital-Electronics/assets/128949246/c8b58b9a-aed4-48a8-81a1-a042e999a2af)


# NETLIST DIAGRAM

![jk net](https://github.com/anishkumar-Embedded/Simulation-project--Digital-Electronics/assets/128949246/93934d3e-ae1a-436c-9a0d-09ca884f924d)


# TIMING DIAGRAM

![jk timing](https://github.com/anishkumar-Embedded/Simulation-project--Digital-Electronics/assets/128949246/b1a22ec4-1275-46a1-b183-554a4ec6b459)


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
