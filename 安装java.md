
# centos用yum安装openjdk

## 删除历史版本

查看系统是否安装过java

    yum list installed | grep java
    
卸载java

    yum -y remove java-1.8.0-openjdk*

## 安装java

查看java软件包列表

    yum -y list java*

选择

    openjdk选择devel版本（如java-1.7.0-openjdk-devel）
    openjdk的devel版本才有jstat,jps等工具

安装

    yum install -y java-1.8.0-openjdk-devel
     
测试

    java -version
    
## 配置环境变量

安装路径

    yum将JDK默认安装路径/usr/lib/jvm
    JAVA_HOME需要指向一个含有java可执行程序(bin)的目录
    java-1.8.0-openjdk下包含bin、jre、lib，可以选择

配置环境变量
  
    打开/etc/profile
    在最后添加
    export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk
    export PATH=$PATH:$JAVA_HOME/bin


导入profile

    source  /etc/profile
    
查看JDK变量

    echo $JAVA_HOME
    echo $PATH

测试jps

    jps