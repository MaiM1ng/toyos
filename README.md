# toyos
## Run
编译引导程序
```ASM
nasm boot.asm -o boot.bin
```
然后使用dd命令将boot程序写入扇区
```ASM
dd if=boot.bin of=./boot.img bs=512 count=1 conv=notrunc
```
然后run, 在GUI中
```ASM
bochs -f ./bochsrc
```