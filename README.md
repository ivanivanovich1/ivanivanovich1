```asm
.section .data
msg: .asciz "You: money; Me: work\n"
len = . - msg

.section .text
.global _start

_start:
    movl $4, %eax
    movl $1, %ebx
    movl $msg, %ecx
    movl $len, %edx
    int $0x80

    movl $1, %eax
    xorl %ebx, %ebx
    int $0x80
```
