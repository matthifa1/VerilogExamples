# VerilogExamples
Basics of Verilog

# Modules
Aufbau: 

module addbit (               // Definieren von Aus-Eingängen
  a      , // first input
  b      , // Second input
  ci     , // Carry input
  sum    , // sum output
  co       // carry output
  );
  //Input declaration
  input a;                    // Deklarieren was in und output ist
  input b;
  input ci;
  //Ouput declaration
  output sum;
  output co;
  //Port Data types
  wire  a;                     // Deklarieren der Typen kann nur wire sein
  wire  b;
  wire  ci;
  wire  sum;
  wire  co;
  //Code starts here
  assign {co,sum} = a + b + ci;   // funktionale Beschreibung Modul
  
  endmodule // End of Module addbit
  
  # Verwenden Module / Verbinden der Module
  
  addbit u0 (
  .a           (r1[0])        ,  // 1. Name in der Modul das aufgerufen wird, dann 2. Name des Signals vom aufrufer
  .b           (r2[0])        ,
  .ci          (ci)           ,
  .sum         (result[0])    ,
  .co          (c1)
  );
