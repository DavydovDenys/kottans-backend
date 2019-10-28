# kottans-backend
kottans-backend courses
## Git
**Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.**

**It is very important to be able to work with a version control system. For me it was the first acquaintance with the GIT. It is always interesting to learn something new!**

![git_basics](task_git/Git_basics.jpg) 
![git_pro](task_git/git_pro.jpg)

## Unix_Shell
**It was allways interesting to me to work with command line. Copying and renaming files without GUI rather cool!). I will improve my command line skills for team working in the future.**
![Unix_Shell](task_unix_shell/command_line.jpg)
![Unix_Shell](task_unix_shell/linux_survival.jpg)

## GitHub & Collaboration
**If You know how to work with a team, you are almost a programmer! GitHub & Collaboration cource helps you to improve teamworking skills.
`git rebase` isn't really all that difficult, and that you can bravely make changes to your repository without fear of doing any damage!
I intend to use it in future.**

![git](task_git_collaboration/GitHub_Collaboration_1.jpg)
![git](task_git_collaboration/GitHub_Collaboration_2.jpg)
![git](task_git_collaboration/GitHub_Collaboration_3.jpg)

## Memory Management
1. **What's going to happen if program reaches maximum limit of stack ?** 
   - If the maximum stack size has been reached, we have a stack overflow and the program receives a Segmentation Fault.
2. **What's going to happen if program requests a big (more then 128KB) memory allocation on heap?**
   - In Linux, if you request a large block of memory via malloc(), the C library will create such an anonymous mapping instead of using heap memory.
3. **What's the difference between Text and Data memory segments ?**
   - **Text(read only!)** The string lives in the text segment, which is read-only and stores all of your code in addition to tidbits like string literals. The text segment also maps your binary file in memory, but **writes** to this area earn your program a *SegmentationFault*.
   -  **Data(read/write)** The data segment holds the contents for static variables initialized in source code. This memory area is not anonymous. It maps the part of the program's binary image that contains the initial static values given in source code.
```md
55bfa5299000-55bfa52c6000 r--p 00000000 07:00 2385                       /usr/bin/bash

55bfa52c6000-55bfa5374000 r-xp 0002d000 07:00 2385                       /usr/bin/bash

55bfa5374000-55bfa53aa000 r--p 000db000 07:00 2385                       /usr/bin/bash

55bfa53aa000-55bfa53ae000 r--p 00110000 07:00 2385                       /usr/bin/bash

55bfa53ae000-55bfa53b7000 rw-p 00114000 07:00 2385                       /usr/bin/bash

55bfa53b7000-55bfa53c1000 rw-p 00000000 00:00 0

55bfa6301000-55bfa6458000 rw-p 00000000 00:00 0                          [heap]

7f0cc5a38000-7f0cc5a3b000 r--p 00000000 07:00 30773                      /usr/lib/x86_64-linux-gnu/libnss_files-2.29.so

7f0cc5a3b000-7f0cc5a42000 r-xp 00003000 07:00 30773                      /usr/lib/x86_64-linux-gnu/libnss_files-2.29.so
7f0cc5a3b000-7f0cc5a42000 r-xp 00003000 07:00 30773                      /usr/lib/x86_64-linux-gnu/libnss_files-2.29.so


7f0cc5a42000-7f0cc5a44000 r--p 0000a000 07:00 30773                      /usr/lib/x86_64-linux-gnu/libnss_files-2.29.so

7f0cc5a44000-7f0cc5a45000 r--p 0000b000 07:00 30773                      /usr/lib/x86_64-linux-gnu/libnss_files-2.29.so

7f0cc5a45000-7f0cc5a46000 rw-p 0000c000 07:00 30773                      /usr/lib/x86_64-linux-gnu/libnss_files-2.29.so

7f0cc5a46000-7f0cc5a4c000 rw-p 00000000 00:00 0
7f0cc5a64000-7f0cc5a96000 r--p 00000000 07:00 16030                      /usr/lib/locale/C.UTF-8/LC_CTYPE
7f0cc5a96000-7f0cc5c09000 r--p 00000000 07:00 16029                      /usr/lib/locale/C.UTF-8/LC_COLLATE
7f0cc5c09000-7f0cc6178000 r--p 00000000 07:00 16041                      /usr/lib/locale/locale-archive

7f0cc6178000-7f0cc617b000 rw-p 00000000 00:00 0
7f0cc617b000-7f0cc61a0000 r--p 00000000 07:00 29855                      /usr/lib/x86_64-linux-gnu/libc-2.29.so
7f0cc61a0000-7f0cc6313000 r-xp 00025000 07:00 29855                      /usr/lib/x86_64-linux-gnu/libc-2.29.so
7f0cc6313000-7f0cc635c000 r--p 00198000 07:00 29855                      /usr/lib/x86_64-linux-gnu/libc-2.29.so
7f0cc635c000-7f0cc635f000 r--p 001e0000 07:00 29855                      /usr/lib/x86_64-linux-gnu/libc-2.29.so
7f0cc635f000-7f0cc6362000 rw-p 001e3000 07:00 29855                      /usr/lib/x86_64-linux-gnu/libc-2.29.so





7f0cc6362000-7f0cc6366000 rw-p 00000000 00:00 0

7f0cc6366000-7f0cc6367000 r--p 00000000 07:00 29987                      /usr/lib/x86_64-linux-gnu/libdl-2.29.so
7f0cc6367000-7f0cc6369000 r-xp 00001000 07:00 29987                      /usr/lib/x86_64-linux-gnu/libdl-2.29.so

7f0cc6369000-7f0cc636a000 r--p 00003000 07:00 29987                      /usr/lib/x86_64-linux-gnu/libdl-2.29.so
7f0cc636a000-7f0cc636b000 r--p 00003000 07:00 29987                      /usr/lib/x86_64-linux-gnu/libdl-2.29.so


7f0cc636b000-7f0cc636c000 rw-p 00004000 07:00 29987                      /usr/lib/x86_64-linux-gnu/libdl-2.29.so

7f0cc636c000-7f0cc637a000 r--p 00000000 07:00 31173                      /usr/lib/x86_64-linux-gnu/libtinfo.so.6.1

7f0cc637a000-7f0cc6388000 r-xp 0000e000 07:00 31173                      /usr/lib/x86_64-linux-gnu/libtinfo.so.6.1
7f0cc6388000-7f0cc6395000 r--p 0001c000 07:00 31173                      /usr/lib/x86_64-linux-gnu/libtinfo.so.6.1


7f0cc6395000-7f0cc6399000 r--p 00028000 07:00 31173                      /usr/lib/x86_64-linux-gnu/libtinfo.so.6.1
7f0cc6399000-7f0cc639a000 rw-p 0002c000 07:00 31173                      /usr/lib/x86_64-linux-gnu/libtinfo.so.6.1


7f0cc639a000-7f0cc639c000 rw-p 00000000 00:00 0 

7f0cc63a3000-7f0cc63a4000 r--p 00000000 07:00 16037                      /usr/lib/locale/C.UTF-8/LC_NUMERIC

7f0cc63a4000-7f0cc63a5000 r--p 00000000 07:00 16040                      /usr/lib/locale/C.UTF-8/LC_TIME

7f0cc63a5000-7f0cc63a6000 r--p 00000000 07:00 16035                      /usr/lib/locale/C.UTF-8/LC_MONETARY

7f0cc63a6000-7f0cc63a7000 r--p 00000000 07:00 16034                      /usr/lib/locale/C.UTF-8/LC_MESSAGES/SYS_LC_MESSAGES
7f0cc63a7000-7f0cc63a8000 r--p 00000000 07:00 16038                      /usr/lib/locale/C.UTF-8/LC_PAPER

7f0cc63a8000-7f0cc63a9000 r--p 00000000 07:00 16036                      /usr/lib/locale/C.UTF-8/LC_NAME


7f0cc63a9000-7f0cc63aa000 r--p 00000000 07:00 16028                      /usr/lib/locale/C.UTF-8/LC_ADDRESS

7f0cc63aa000-7f0cc63ab000 r--p 00000000 07:00 16039                      /usr/lib/locale/C.UTF-8/LC_TELEPHONE

7f0cc63ab000-7f0cc63ac000 r--p 00000000 07:00 16032                      /usr/lib/locale/C.UTF-8/LC_MEASUREMENT

7f0cc63ac000-7f0cc63b3000 r--s 00000000 07:00 28824                      /usr/lib/x86_64-linux-gnu/gconv/gconv-modules.cache

7f0cc63b3000-7f0cc63b4000 r--p 00000000 07:00 16031                      /usr/lib/locale/C.UTF-8/LC_IDENTIFICATION
7f0cc63b4000-7f0cc63b5000 r--p 00000000 07:00 29120                      /usr/lib/x86_64-linux-gnu/ld-2.29.so
7f0cc63b5000-7f0cc63d6000 r-xp 00001000 07:00 29120                      /usr/lib/x86_64-linux-gnu/ld-2.29.so


7f0cc63d6000-7f0cc63de000 r--p 00022000 07:00 29120                      /usr/lib/x86_64-linux-gnu/ld-2.29.so
7f0cc63de000-7f0cc63df000 r--p 00029000 07:00 29120                      /usr/lib/x86_64-linux-gnu/ld-2.29.so



7f0cc63df000-7f0cc63e0000 rw-p 0002a000 07:00 29120                      /usr/lib/x86_64-linux-gnu/ld-2.29.so

7f0cc63e0000-7f0cc63e1000 rw-p 00000000 00:00 0 

7fff82dd6000-7fff82df7000 rw-p 00000000 00:00 0                          [stack]

7fff82df7000-7fff82dfa000 r--p 00000000 00:00 0                          [vvar]

7fff82dfa000-7fff82dfb000 r-xp 00000000 00:00 0                          [vdso]

ffffffffff600000-ffffffffff601000 r-xp 00000000 00:00 0                  [vsyscall]
```
*Memory Mapping Segment, Heap and Stack fragments address:*
- `HEAP - 55bfa6301000-55bfa6458000 rw-p 00000000 00:00 0`
- `STACK - 7fff82dd6000-7fff82df7000 rw-p 00000000 00:00 0`
- `MMS - 7f0cc5a45000-7f0cc5a46000 rw-p 0000c000 07:00 30773`

## HTTP & HTTPS
Requests:
- `curl https://api.github.com/users/DavydovDenys`
- `curl -i https://api.github.com/users/DavydovDenys`
- `curl -i https://api.github.com/users/DavydovDenys`
- `curl --user "DavydovDenys:****************" https://api.github.com/gists/starred`
- `curl --user "DavydovDenys" https://api.github.com/gists/starred`
- `curl -i https://api.github.com/orgs/kottans/repos`
- ```
  curl -H 'Authorization: token 5199831f4dd3b79e7c5b7e0ebe75d67aa66e79d4'
       -d '{\ 
          "title": "New logo", \
          "body": "We should have one", \
          "labels": ["design"] \
           }'\
        https://api.github.com/repos/DavydovDenys/kottans-backend/issues
  ```
1. Name at least three possible negative consequences of not using https.
- There is a possibility to intercept your data.
- A non-certified server may imitate another website.
- Our website may be blocked by a browser
