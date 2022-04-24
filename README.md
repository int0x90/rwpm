# RWPM - Read/Write 64bit process memory on Linux 
Super simple CLI program written in C++ that enables you to manipulate another processes memory address space.<br>
I use <b>process_vm_read</b> and <b>process_vm_write</b> system calls to keep it simple. Note that Linux kernels are sometimes [compiled without them](https://man7.org/linux/man-pages/man2/process_vm_readv.2.html#CONFORMING_TO).
