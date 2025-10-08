# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**
A shift register is a sequential logic circuit that is used for storing and transferring data.
It consists of a group of flip-flops connected in a chain, where the output of one flip-flop is connected to the input of the next. The shifting of data takes place with the application of clock pulses.

In a Serial-In Parallel-Out (SIPO) shift register, data bits are entered serially (one bit at a time) through the input line on each clock pulse, and after a certain number of clock pulses, the output becomes available in parallel at all stages simultaneously.

Each flip-flop in the register stores one bit of data. The shifting of bits occurs at every positive edge of the clock. The first flip-flop receives the serial input bit, and subsequent flip-flops receive the output of the previous stage.

WORKING PRINCIPLE:

The input data bit (sin) is applied serially.

On every positive edge of the clock (clk), the input bit is shifted into the first flip-flop (q[0]).

The contents of each flip-flop are shifted to the next higher-order bit position.

After 4 clock pulses, all bits are available at the outputs (q[3:0]) in parallel form.

Thus, the circuit converts serial data input into parallel data output.

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */
1. Type the program in Quartus software.
 2. Compile and run the program.
 3. Generate the RTL schematic and save the logic diagram.
 4. Create nodes for inputs and outputs to generate the timing diagram.
 5. For different input combinations generate the timing diagram


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
module jkff(j,k,clk,q,qbar);
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

Developed by: RegisterNumber: 250`8734

*/

**RTL LOGIC FOR SISO Shift Register**
<img width="1708" height="262" alt="Screenshot 2025-10-08 111450" src="https://github.com/user-attachments/assets/6e83df49-70e2-4955-a748-79c2a901020a" />


**TIMING DIGRAMS FOR SISO Shift Register**
<img width="824" height="622" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/e564a364-18bd-4083-afa9-e2d4fca31900" />

**RESULTS**
Thus the truth table of logic gates in Quartus II using Verilog programming is studied
 and verified successfully
