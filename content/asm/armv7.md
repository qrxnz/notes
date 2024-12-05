---
title: armv7
tags:

- asm
---

## armv7

### amv7 as expamples

#### simple math

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
#### ldr - pseudo-instruction loads a register

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

#### str - load and Store with register offset

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
