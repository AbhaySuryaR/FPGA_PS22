# FPGA_PS22

// INTERFACING LED

 m4_include_lib(['https://raw.githubusercontent.com/BalaDhinesh/Digital-Design-on-FPGA--Phaseshift22/main/src/fpga_includes.tlv'])
   m4_makerchip_module   // (Expanded in Nav-TLV pane.)
   wire [7:0] led;
   wire [7:0] led1;
   assign led = 8'b11111111;
   assign led1 = led << 1;                
                   
\TLV
   m4_define(M4_BOARD, 1)  
   m4+fpga_init()
   m4+fpga_led(*led)
\SV
   endmodule
   
   
   
