# 内存访问
# DS和[address]
DS 是存放[address]数据段段段地址， address这个就是数据段偏移地址。

DS寄存器不能直接赋值，而是需要通过通用寄存器来间接赋值。
```nasm
mov ax, 1000
mov ds, ax
```

# 栈
SS寄存器控制栈顶的段寄存器，SP寄存器控制偏移地址。

# push和pop
> 栈是先运行指针再赋值的。

push指令可以使得sp寄存器减1（字节数据），pop可以使得sp加1（字节数据）。

push指令可以使得sp寄存器减2（字数据），pop可以使得sp加2（字数据）。
```nasm
; 将数据压入栈空间中
push ax
; 将数据存入bx寄存器中，并将sp加2
pop bx
```