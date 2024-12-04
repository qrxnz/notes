---
title: armv7
tags:
- asm
---

### amv7 as expamples

#### simple substract

```s
.global _start
_start:
	mov r0, #4
	mov r2, #2

	sub r1, r0, r2 ; r1 = r0 - r2
```