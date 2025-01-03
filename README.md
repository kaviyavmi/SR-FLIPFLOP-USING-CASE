# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

1.Launch Quartus on your computer and create a new project: Go to File → New Project Wizard. Specify the project name, directory, and top-level entity name (e.g., SR_FlipFlop).

2.Create the SR Flip-Flop Circuit and implement the SR Flip-Flop by writing VHDL/Verilog code. Go to File → New → Select Verilog File.

3.Compile the Project Click on Processing → Start Compilation. Fix any syntax or schematic errors if present.

4.Simulate the Circuit: Go to Tools → University Program VWF. Define the inputs for S, R, and CLK in the waveform editor. Run the simulation and observe the waveforms.

5.Verify the Results. Compare the simulated results with the truth table for a SR Flip-Flop


**PROGRAM**

module sr_ff(s,r,clk,q,qbar);

input s,r,clk;

output reg q;

output reg qbar;

initial 

begin

q=0;

qbar=1;

end

always @(posedge clk)

begin
  
   q=s|(~r&q);
   
   qbar=r|(~s&~q);

endendmodule

Developed by: V.M.Kaviya

RegisterNumber: 24900714

**RTL LOGIC FOR FLIPFLOPS**

![WhatsApp Image 2024-12-11 at 19 35 42_bc8cd4a9](https://github.com/user-attachments/assets/fe74814e-3ce7-4a34-8e51-ac7194dbfdb4)


**TIMING DIGRAMS FOR FLIP FLOPS**

![WhatsApp Image 2024-12-11 at 19 35 43_fe5c4798](https://github.com/user-attachments/assets/77e8cb34-c4b5-45d2-afad-558fed3a7944)


**RESULTS**

Implementation SR flipflop using verilog and validating their functionality using their functional tables is verified.

