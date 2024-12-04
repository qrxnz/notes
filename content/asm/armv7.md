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