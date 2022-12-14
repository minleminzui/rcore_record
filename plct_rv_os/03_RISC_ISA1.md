## ISA是什么
- 相比较于`syscall`,
    - ISA可以看作`Operating System`与`Microarchitecture`之间接口，
    - ISA是一组规范，包括
        - `基本数据类型BYTE/HALFWORD/WORD...`
        - 寄存器
        - 指令
        - 寻址模式
        - 异常或者中断处理方式
        - 等等...
    - 一种ISA，可以有多种实现，就像是C库，ISA的底层微指令(是硬件上对于指令集架构的一种实现)，intel和amd就可能不一样、
- `CISC`和`RISC`可以类比为`文言文`与`白话文`，前者指令多而且短，为了使得生成的程序短，就像是文言文短可以节省竹子，后者由常用指令组合成复杂的意思，所以生成的程序长。
- ISA的宽度可以理解为CPU中`通用寄存器`的宽度，这个决定了寻址范围的大小，以及数据运算能力