# Meta
Meta Interview Question
Q)module dut (
 input logic clk, // Clock signal
 input logic reset, // Reset signal

 
 input logic avalid, // Address valid signal
 input logic [7:0] a_id, // Address ID
 input logic [31:0] addr, // Address
 input logic dvalid, // Data valid signal
 input logic [7:0] d_id, // Data ID
 input logic [31:0] data, // Data

 
 output logic o_avalid, // Output address valid signal
 output logic [7:0] o_a_id, // Output address ID
 output logic [31:0] o_addr, // Output address
 output logic o_dvalid, // Output data valid signal
 output logic [7:0] o_d_id, // Output data ID
 output logic [31:0] o_data // Output data
);
endmodule

The DUT translates the address and processes packets out of order.
Processing time ranges from 5 to 100 clock cycles.
The same ID can be reused after the previous packet with the same ID is retired.
Address and data may arrive at the same time or with a delay.
address can come back to back. Data should be in order wrt address. Delay will be between (1,10). Write driver code task for this. Attach snippet in the comment section.
