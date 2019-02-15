assembly = address":" instrunction.

address = "0" "x" ("0" | ... | "9" | "A" | "B" | .... "F") {"0" | ... | "9" | "A" | "B" | .... "F"}.

instruction = Initialization | Arithmetic | Memory | Control | System | Data |"nop" .

Initialization = ("lui" "," register "," address) | ("addi" "," register "," register "," ["-"] immidiate ).

Arithmetic = ( "add" | "sub" | "mul" | "divu" | "remu" | "sltu") "," register "," register "," register.

Memory=("ld" | "sd") "," register "," ["-"]  immidiate "(" register ")".

Control = ("beq" "," register "," register ","  immidiate "[" address "]") | ("jal" "," register "," ["-"] immidiate "["address"]" ) | ("jalr" "," register "," ["-"] immidiate "(" register ")") .

System = "ecall".

Data = ".quad" address.

immidiate = digit {digit}.

Register = "$t0" | "$t1" | ...........| "$sp .

digit  = "0" | ... | "9" .
