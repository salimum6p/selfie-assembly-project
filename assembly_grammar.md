assembly = address":" instrunction.

address = "0" "x" ("0" | ... | "9" | "A" | "B" | .... "F") {"0" | ... | "9" | "A" | "B" | .... "F"}.

instruction = Initialization | Arithmetic | Memory | Control | System | "nop" | Data.

Initialization = " lui " , " register ", " Addi "," register "," register "," Imm ".

Arithmetic = ( "add" | "sub" | "mul" | "divu" | "remu" | "sltu") "," register "," register "," register.

Memory=("ld" | "sd") "," register "," ["-"] imm "(" register ")".

Control = ("beq" "," register "," register "," imm "[" address "]") | ("jal" "," register "," imm) | ("jalr" "," register "," imm "(" register ")") .

System = "ecall".

Data = ".quad" Addi.

Imm = digit {digit}.

Register = "$t0" | "$t1" | 