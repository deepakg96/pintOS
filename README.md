# pintOS 
This is the Fall 2021 CSE521 Operating Systems Project at Suny Buffalo. 


## PROJECT 1 - THREADS & PROCESSES (/src/threads/)

###### Phase 1: Priority Scheduling (pa1.tar.gz)

Tests:
* priority-preempt
* priority-change
* priority-fifo

Changed files: thread.c, thread.h

###### Phase 2: Alarm Clock (pa1_phase2.tar.gz)

Tests:
Along with phase 1 tests, following also must pass.
* alarm-single
* alarm-multiple
* alarm-simultaneous
* alarm-priority
* alarm-zero
* alarm-negative
 
Changed files: timer.c, timer.h, thread.h, thread.c

###### Phase 3: Priority Donation & MLFQS (pa1_phase3.tar.gz)

Priority Donation
Tests:
* priority-donate-one
* priority-donate-multiple
* priority-donate-multiple2
* priority-donate-nest
* priority-donate-sema
* priority-donate-lower
* priority-sema
* priority-condvar
* priority-donate-chain

Changed files: thread.c, thread.h, synch.c, synch.h

MLFQS
Tests:
* mlfqs-load-1
* mlfqs-load-60
* mlfqs-load-avg
* mlfqs-recent-1
* mlfqs-fair-2
* mlfqs-fair-20
* mlfqs-nice-2
* mlfqs-nice-10
* mlfqs-block

Changed files: thread.c, timer.c, thread.h



## PROJECT 2 - USER PROGRAMS (/src/userprog/)

###### Phase 1: Stack Setup - Argument Parsing (pa2.tar.gz)

Tests:
Follow this to run tests -- 
1. Download the pa2_arg_test.tar.gz (attached)
2. Move it to your pintos root directory (NOT src/) inside the VM, then navigate to the pintos directory and run:
    tar -xzvf pa2_arg_test.tar.gz
    this will extract the tar, and create a new directory "pa2_arg_test/" with three files: test_arg_passing.sh, arg_test.py, gold.txt
3. Run the script by executing (from the pintos root directory, NOT src/ or src/userprog)

This will run a sample input and check your implementation. Note that the tester injects a hex_dump in your code, so:
1. Do not remove existing comments from pintos code in process.c
2. Comment out any other hex_dump or printf calls you have in your code.
    python pa2_arg_test/arg_test.py
* pintos --filesys-size=2 -p ../examples/echo -- -f -q run 'echo x'
* python pa2_arg_test/arg_test.py  -- from outside the /src directory, i.e /pintos root directory


Changed files: process.c

###### Phase 2: Safe Memory Access & System Calls

Tests:
* tests/userprog/args-none
* tests/userprog/args-single
* tests/userprog/args-multiple
* tests/userprog/args-many
* tests/userprog/args-dbl-space
* tests/userprog/sc-bad-sp
* tests/userprog/sc-bad-arg
* tests/userprog/sc-boundary
* tests/userprog/sc-boundary-2
* tests/userprog/exit
* tests/userprog/bad-read
* tests/userprog/bad-write
* tests/userprog/bad-read2
* tests/userprog/bad-write2
* tests/userprog/bad-jump
* tests/userprog/bad-jump2

Changed files: syscall.c, syscall.h, exception.c


