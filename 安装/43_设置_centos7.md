

# 概述 

    centos7 安装和6的安装不一样

# 初始步骤

    选择安装
    语言选择英文

# 安装概览

## localization

    时间/键盘/语言使用默认

## software

    安装源选择本地 
    安装包最小安装
        
        
## INSTALLATION DESTINATION    

    选择硬盘
    选择手动配置
    点击完成-->自动进入硬盘分割
    
    1. 选择标准分割模式 添加 biosboot 2M
    2. 添加 /boot 1G
    3. 添加 / 10G ,修改为LVM模式,
        点击修改,选择固定容量,选择15G
    4. 添加 /home 5G ,修改为LVM模式,点击修改选择刚刚的硬盘组
    5. 添加 swap 2G ,修改为LVM模式,点击修改选择刚刚的硬盘组
    此时还剩下5G的硬盘
    点击完成-->选择确认
    
## NETWORK/HOSTNAME

    选择网卡-->选择设置
    1. 选择一般-->选择自动联网
    2. 选择ipv4-->选择手动-->添加ip/掩码/网关-->保存
    点击网络连接开关,测试网络
    修改hostname  
    
# 最后

    点击安装
    设置root密码111111  
    安装完以后重启
    
# 测试

    通过ping测试一下与外网/宿主/其他虚拟机的通信    

# 参考

https://blog.csdn.net/z605928171/article/details/52200084    