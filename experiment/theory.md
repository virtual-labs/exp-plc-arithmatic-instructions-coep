In case of PLC various instructions are available which can be used for computational purpose.
The compute/math instructions evaluate arithmetic operations using an expression or a specific arithmetic instruction.
Various instructions PLC can support are as follows.
| Instruction      | Description |
| ----------- | ----------- |
| ADD      | Add two values       |
| SUB   | Subtract two values      |
| MUL | Multiply two values |
| DIV | Divide two values |
| MOD | Determine the remainder after one value is divided by another |
| SQR | Calculate the square root of a value |
| NEG | Take the opposite sign of a value |
| ABS | Take the absolute value of a value |

When these operations are carried out in the PLC, the type should be the same for source and destination e.g. real, integer etc. You can use mix data types, but loss of accuracy and rounding error occurs. The instruction may take more time to execute.
A compute/math instruction executes once each time the instruction is scanned as long as the rung-condition-in is true. Out of the above; ADD, SUB, MUL and DIV instructions are available in the PLC simulator.
The input and output parameters associated with these instructions are:

| Input  Parameter       | Data  Type | Description    |
| :---        |    :----:   |          :--- |
| EnableIn      | BOOL       | Enable input. If cleared, the instruction does not execute and outputs are not updated|
| Source A   | REAL        | Value to add to Source B      |
| Source B      | REAL | Value to add to Source A |

| Output  Parameter       | Data  Type | Description    |
| :---        |    :----:   |          :--- |
| EnableOut      | BOOL       | Enable output|
| Dest  | REAL        | Result of the math instruction      |

**ADD instruction:**
The ADD instruction adds Source A to Source B and places the result in the Destination.
When the instruction is used in Relay Ladder the output parameter conditions are defined as mentioned below.
| Condition      | Action |
| ----------- | ----------- |
| prescan      | The rung-condition-out is set to false.       |
| rung-condition-in is false   | The rung-condition-out is set to false.      |
|rung-condition-in is true | Destination = Source A + Source B.The rung-condition-out is set to true |

**SUB instruction:**
The SUB instruction subtracts Source B from Source A and places the result in the Destination.
When the instruction is used in Relay Ladder the output parameter conditions are defined as mentioned below.
| Condition      | Action |
| ----------- | ----------- |
| prescan      | The rung-condition-out is set to false.       |
| rung-condition-in is false   | The rung-condition-out is set to false.      |
|rung-condition-in is true | Destination = Source A - Source B.The rung-condition-out is set to true |

**MUL instruction:**
The MUL instruction multiplies Source A with Source B and places the result in the Destination.
When the instruction is used in Relay Ladder the output parameter conditions are defined as mentioned below.

| Condition      | Action |
| ----------- | ----------- |
| prescan      | The rung-condition-out is set to false.       |
| rung-condition-in is false   | The rung-condition-out is set to false.      |
| rung-condition-in is true | Destination = Source A*Source B.The rung-condition-out is set to true |

**DIV instruction:**
The DIV instruction divides Source A by Source B and places the result in the Destination.
When the instruction is used in Relay Ladder the output parameter conditions are defined as mentioned below.
| Condition      | Action |
| ----------- | ----------- |
| prescan      | The rung-condition-out is set to false.       |
| rung-condition-in is false   | The rung-condition-out is set to false.      |
| rung-condition-in is true | Destination = Source A/ Source B.The rung-condition-out is set to true |
