# Pintos
This repo contains skeleton code for CE Operating System course at Sharif University.

[Pintos](http://pintos-os.org) is a teaching operating system for 32-bit x86, challenging but not overwhelming, small
but realistic enough to understand OS in depth (it can run on x86 machine and simulators 
including QEMU, Bochs and VMWare Player!). The main source code, documentation and assignments 
are developed by Ben Pfaff and others from Stanford (refer to its [LICENSE](./LICENSE)).

# Installing

- first install required tool chains: ```i386-elf-gcc``` ```perl``` ```qemu-system-x86_64``` 

- cd into ```src/threads/``` and ```make```

- cd into ```src/utils/``` and ```make```

And Done! you can boot pintos using qemu, for example:

```bash
cd src/utils
```

```bash 
./pintos --qemu -k -T 60 -- -q run alarm-single
```

You should see "alarm-single" is running:

```
qemu-system-x86_64 -device isa-debug-exit -drive format=raw,media=disk,index=0,file=/tmp/_t3NzNbwFZ.dsk -m 4 -net none -serial stdio
VNC server running on ::1:5900
Pintos hda1
Loading.........
Kernel command line: -q run alarm-single
Pintos booting with 3,968 kB RAM...
367 pages available in kernel pool.
367 pages available in user pool.
Calibrating timer...  104,755,200 loops/s.
Boot complete.
Executing 'alarm-single':
(alarm-single) begin
(alarm-single) Creating 5 threads to sleep 1 times each.
(alarm-single) Thread 0 sleeps 10 ticks each time,
(alarm-single) thread 1 sleeps 20 ticks each time, and so on.
(alarm-single) If successful, product of iteration count and
(alarm-single) sleep duration will appear in nondescending order.
(alarm-single) thread 0: duration=10, iteration=1, product=10
(alarm-single) thread 1: duration=20, iteration=1, product=20
(alarm-single) thread 2: duration=30, iteration=1, product=30
(alarm-single) thread 3: duration=40, iteration=1, product=40
(alarm-single) thread 4: duration=50, iteration=1, product=50
(alarm-single) end
Execution of 'alarm-single' complete.
Timer: 271 ticks
Thread: 0 idle ticks, 272 kernel ticks, 0 user ticks
Console: 986 characters output
Keyboard: 0 keys pressed
Powering off...
```
