正确的关机流程为：sync > shutdown > reboot > halt

    sync 将数据由内存同步到硬盘中。

    shutdown 关机指令，你可以man shutdown 来看一下帮助文档。例如你可以运行如下命令关机：

    shutdown –h 10 ‘This server will shutdown after 10 mins’ 这个命令告诉大家，计算机将在10分钟后关机，并且会显示在登陆用户的当前屏幕中。
    shutdown –h now 立马关机
    shutdown –h 20:25 系统会在今天20:25关机
    shutdown –h +10 十分钟后关机
    shutdown –r now 系统立马重启
    shutdown –r +10 系统十分钟后重启
    reboot 就是重启，等同于 shutdown –r now
    halt 关闭系统，等同于shutdown –h now 和 poweroff

    e.g:
        # shutdown -p now   ### 关闭机器
        # shutdown -H now   ### 停止机器      
        # shutdown -r09:35  ### 在 09:35am 重启机器
        # shutdown -c       ### 取消关机

    halt 命令通知硬件来停止所有的 CPU 功能，但是仍然保持通电。你可以用它使系统处于低层维护状态。注意在有些情况会它会完全关闭系统
        # halt             ### 停止机器
        # halt -p          ### 关闭机器
        # halt --reboot    ### 重启机器

    poweroff 会发送一个 ACPI 信号来通知系统关机。
        # poweroff           ### 关闭机器
        # poweroff --halt    ### 停止机器
        # poweroff --reboot  ### 重启机器
       
    reboot 命令 reboot 通知系统重启。
        # reboot           ### 重启机器
        # reboot --halt    ### 停止机器
        # reboot -p        ### 关闭机器