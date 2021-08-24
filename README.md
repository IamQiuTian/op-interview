### 系统相关
* uptime命令中load average字段后的3个数字代表什么？如何判断系统整体负载的高低？
  * 一分钟内,五分钟内,十五分钟内的系统平均负载;
  * load 是一定时间内计算机有多少个活跃任务,也就是说是计算机的任务执行队列的长度,cpu计算的队列,所以一般认为CPU核数的就是load值的上线。
* 如何查看某个进程的CPU、内存和负载情况？
  * 通常我们使用top命令去交互查看系统负载信息。
* free命令中shared  buff/cache  available 这3个字段是什么意思？
  * shared 多进程使用的共享内存;
  * buff/cache 读写缓存内存,这部分内存是当空闲来用的,当free内存不足时,linux内核会将此内存释放;
  * available 是可以被程序梭使用的物理内存;
* 描述下在linux中给一个文件授予 644权限是什么意思？
  * 644 即〔当前用户读和写权限,〔群组用户〕读权限,〔其它〕读权限。
* linux中如何禁止一个用户通过shell登录？
  * 使用命令或者通过修改/etc/passwd文件的用户shell部分为/sbin/nologin 即可实现。
* 如何追踪shell脚本的执行过程？
  * sh -x 或者 bash -x
* 如何观察当前系统的网络使用情况？
  * 使用iftop等工具。 
* 如何追踪A主机到B主机过程中的丢包情况？
  * traceroute、mtr, 或者其他双端带宽测试工具。
* linux 系统中ID为0是什么用户？
  * root
* 怎么统计当前系统中的活跃连接数？
  * netstat -na|grep ESTABLISHED|wc -l 
* time_wait 状态处于TCP连接中的那个位置？
  * 客户端发出FIN请求服务端断连, 服务器未发送ack+fin确认。
* 如何递归创建文件夹？
  * mkdir -p
* 如何查看一个文件的权限、大小和最新修改时间？
  * ll
