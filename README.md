# uAuditAnalyzer - Unmanarc's Auditd Analyzer

Author: Aarón Mizrachi <aaron@unmanarc.com>  
License: GPLv3  
  
This program is intended to receive and reconstruct the information comming from audisp+rsyslog from a linux server.   
  
It's known that auditd (audisp+rsyslog) provides information like this:  

```
Mar 27 00:37:34 vnode03 audispd: node=vnode03.vuln type=SYSCALL msg=audit(1585291054.568:2911): arch=c000003e syscall=59 success=yes exit=0 a0=6f29b0 a1=6f2cb0 a2=6f1b70 a3=7ffff2f0ae60 items=2 ppid=22440 pid=22441 auid=4294967295 uid=48 gid=48 euid=48 suid=48 fsuid=48 egid=48 sgid=48 fsgid=48 tty=(none) ses=4294967295 comm="ps" exe="/usr/bin/ps" subj=system_u:system_r:httpd_t:s0 key="L5_EXEC_BIN"
Mar 27 00:37:34 vnode03 audispd: node=vnode03.vuln type=EXECVE msg=audit(1585291054.568:2911): argc=1 a0="ps"
Mar 27 00:37:34 vnode03 audispd: node=vnode03.vuln type=CWD msg=audit(1585291054.568:2911):  cwd="/var/www/html"
Mar 27 00:37:34 vnode03 audispd: node=vnode03.vuln type=PATH msg=audit(1585291054.568:2911): item=0 name="/usr/bin/ps" inode=1719654 dev=fd:00 mode=0100755 ouid=0 ogid=0 rdev=00:00 obj=system_u:object_r:bin_t:s0 objtype=NORMAL cap_fp=0000000000000000 cap_fi=0000000000000000 cap_fe=0 cap_fver=0
Mar 27 00:37:34 vnode03 audispd: node=vnode03.vuln type=PATH msg=audit(1585291054.568:2911): item=1 name="/lib64/ld-linux-x86-64.so.2" inode=1709066 dev=fd:00 mode=0100755 ouid=0 ogid=0 rdev=00:00 obj=system_u:object_r:ld_so_t:s0 objtype=NORMAL cap_fp=0000000000000000 cap_fi=0000000000000000 cap_fe=0 cap_fver=0
Mar 27 00:37:34 vnode03 audispd: node=vnode03.vuln type=PROCTITLE msg=audit(1585291054.568:2911): proctitle="ps"
```

But this output came with many "unrelated" separated lines, causing some analysis troubles, specially if you want to correlate them...  

## Operational Scheme
  
## Filters/Ruleset 

## Execution

## Outputs



## Requirements 

## Build

## Alternatives



