---
title: armv7
tags:

- asm
---

## armv7 data types

- Byte --> `8 bits`
- Halfword --> `16 bits`
- Word --> `32 bits`

## amv7 as expamples

### simple math

```s
.global _start
_start:
	mov r0, #4
	mov r2, #2

	sub r1, r0, r2 ; r1 = r0 - r2
```

```s
.global _start
_start:
	mov r0, #4
	mov r2, #2

	mul r1, r0, r2 ; r1 = r0 * r2
```

```s
.global _start
_start:
	mov r0, #4
	mov r2, #2

	add r1, r0, r2 ; r1 = r0 + r2
```
### ldr - pseudo-instruction loads a register

```
.global _start

.text
_start:
	ldr r0, =var1
	ldr r1, [r0]
	
.data
var1: .word 5
var2: .word 6
```

### str - load and Store with register offset

```
STR <source_register>, [<address_register>]
```
```s
.global _start

.text
_start:
	ldr r0, =var1
	ldr r1, [r0]
	
	mov r2, #3
	ldr r3, =var2
	str r2, [r3] ; r3 == 3 
	
.data
var1: .word 5
var2: .word 6
```
### Bitwise

#### AND

```s
.global _start
_start:
	mov r0, #66
	and r1, r0 #38
```

#### OR

```s
.global _start
_start:
	mov r0, #66
	or r1, r0 #38
```

#### EOR (XOR)

```s
.global _start
_start:
	mov r0, #66
	eor r1, r0 #38
```

#### MVN (NOT)
```s
.global _start
_start:
	mov r0, #66
	mvn r1, r0
```
