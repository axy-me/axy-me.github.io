## Top命令

### 简介

Top命令是Linux下常用的性能分析工具，能够实时显示系统中各个进程的资源占用状况，类似于Windows的任务管理器。top显示系统当前的进程和其他状况，是一个动态显示过程，可以自动或者通过用户按键来不断刷新当前状态。如果在前台执行该命令，它将独占前台,直到用户终止该程序为止。

比较准确的说，top命令提供了实时的对系统处理器的状态监控，显示系统中CPU最“敏感”的任务列表。top命令可以按CPU使用、内存使用和执行时间对任务进行排序，而且该命令的很多特性都可以通过交互式命令或者在个人定制文件中进行设定。

### 使用方法

在Terminal里输入top，进入top命令显示的交互界面；

``` bash
top - 18:39:42 up  8:12,  1 user,  load average: 0.39, 0.58, 0.51
任务: 287 total,   1 running, 285 sleeping,   0 stopped,   1 zombie
%Cpu(s):  2.0 us,  3.0 sy,  0.0 ni, 95.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :  15292.7 total,   7617.6 free,   2821.7 used,   4853.3 buff/cache
MiB Swap:   3906.0 total,   3906.0 free,      0.0 used.  12025.0 avail Mem 

 进程号 USER      PR  NI    VIRT    RES    SHR    %CPU  %MEM     TIME+ COMMAND
    779 root      20   0 1418856  48264  26768 S   6.7   0.3   0:23.79 containerd
   1915 axy       20   0    7388   3240   2872 S   6.7   0.0   0:04.81 dbus-daemon
   1983 axy       20   0 5427272 371396 143840 S   6.7   2.4   9:24.54 gnome-shell
   7363 axy       20   0  991204  79172  61044 S   6.7   0.5   0:16.62 gnome-terminal-
  74361 axy       20   0   20660   4060   3348 R   6.7   0.0   0:00.01 top
      1 root      20   0  171184  13348   8544 S   0.0   0.1   0:06.26 systemd
      2 root      20   0       0      0      0 S   0.0   0.0   0:00.02 kthreadd
      3 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 rcu_gp
      4 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 rcu_par_gp
      6 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/0:0H-kblockd
      9 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 mm_percpu_wq
     10 root      20   0       0      0      0 S   0.0   0.0   0:00.37 ksoftirqd/0
     11 root      20   0       0      0      0 I   0.0   0.0   0:15.59 rcu_sched
     12 root      rt   0       0      0      0 S   0.0   0.0   0:00.10 migration/0
     13 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 idle_inject/0
     14 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/0
     15 root      20   0       0      0      0 S   0.0   0.0   0:00.00 cpuhp/1
     16 root     -51   0       0      0      0 S   0.0   0.0   0:00.00 idle_inject/1
     17 root      rt   0       0      0      0 S   0.0   0.0   0:00.31 migration/1
     18 root      20   0       0      0      0 S   0.0   0.0   0:00.27 ksoftirqd/1
     20 root       0 -20       0      0      0 I   0.0   0.0   0:00.00 kworker/1:0H-kblockd
```

其中对CPU列的解释为：

|  内容  |  说明  |
|--------|--------|
| %us | 用户模式占用的 CPU 百分比；如果%us占比高，可能用户程序在用户空间执行了大量操作 |
| %sy | 系统模式占用的 CPU 百分比；如果%sy占比高，可能是因为某些进程大量使用了系统调用，如printf等 |
| %ni | x |
| %id | x |
| %wa | x |
| %hi | x |
| %si | x |
| %st | x |



