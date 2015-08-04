# Simple MIPS Compiler
Made for easily creating binary that can be easily used in the [MIPS Processor](https://github.com/PiJoules/MIPS-processor).

## Usage
Just pass in the contents of the file containing the mips code to the python script.

```sh
$ python mips_parser.py < test.txt
```

## Supported Instructions
| Instruction | Format | Operation | Syntax |
|-------------|--------|-----------|--------|
| Add | R | R[rd] = R[rs] + R[rt] | add $rd, $rs, $rt |
| Add immediate | I | R[rt] = R[rs] + immed. | addi $rt, $rs, immed. |
| And | R | R[rd] = R[rs] & R[rt] | and $rd, $rs, $rt |
| Branch On Equal | I | if (R[rs]==R[rt]) PC=PC+4+BranchAddr | beq $rs, $rt, BranchAddr |
| Branch On Not Equal | I | if (R[rs]!=R[rt]) PC=PC+4+BranchAddr | bne $rs, $rt, BranchAddr |
| Jump | J | PC=JumpAddr | j JumpAddr |
| Or | R | R[rd] = R[rs] \| R[rt] | or $rd, $rs, $rt |
| Set Less Than | R | R[rd] = (R[rs] < R[rt]) ? 1 : 0 | slt $rd, $rs, $rt |