





# MIPS ISA
We built a CPU using logisim evolution. this CPU will execute most of the MIPS instructions. The first phase was a single-cycle CPU because it takes just a rising edge to access the memory.
In the second phase, we implemented a cache, and accessing memory would take 5 clocks. Our cache was 2 way set-associative. The third phase was about the pipeline and we implemented MIPS 5-stage
pipline. In the last Phase, we implemented branch prediction a saturating counter. 

In addition to all the above works, we handled RAW hazard so if you read from a register too soon, the real value will be fast-forwarded to the output of the register file.
The only hazard that may happen is when you load something to a register from memory and immediately use the value of that register in the next instruction.
This won't work because when you are loading the value from memory, you need that value in the ALU at the same time.
 
Most important tests that worked correctly:
```
00400000: <main> ; <input:1> main:
00400000: 201004d2 ; <input:2> addi $s0, $zero, 1234
00400014: ac100008 ; <input:7> sw $s0, 8($zero)
00400018: 14100001 ; <input:8> bne $zero, $s0, next
0040001c: 02008820 ; <input:9> add $s1, $s0, $zero
00400020: <next> ; <input:10> next:
00400020: 02009020 ; <input:11> add $s2, $s0, $zero
```

```
00400000: <main> ; <input:0> main:
00400000: 10000002 ; <input:1> beq $zero, $zero, chert
00400004: 14000001 ; <input:2> bne $zero, $zero, chert
00400008: 00000000 ; <input:3> sll $zero, $zero, 0
0040000c: <chert> ; <input:4> chert:
```
