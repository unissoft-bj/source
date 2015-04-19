安装java 8

root@radxa:~# java -version
The program 'java' can be found in the following packages:
 * default-jre
 * gcj-4.8-jre-headless
 * openjdk-7-jre-headless
 * gcj-4.6-jre-headless
 * openjdk-6-jre-headless
Try: apt-get install <selected package>

ref : http://www.rpiblog.com/2014/03/installing-oracle-jdk-8-on-raspberry-pi.html

source : http://www.oracle.com/technetwork/java/javase/downloads/jdk8-arm-downloads-2187472.html

root@radxa:~# git clone -b java8 git@github.com:caiwang/source.git
root@radxa:~# cp ./source/jdk-8u33-linux-arm-vfp-hflt.gz ./

root@radxa:~# tar zxvf jdk-8u33-linux-arm-vfp-hflt.gz -C /opt

root@radxa:~# update-alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_33/bin/javac 1
update-alternatives: using /opt/jdk1.8.0_33/bin/javac to provide /usr/bin/javac (javac) in auto mode

root@radxa:~# update-alternatives --install /usr/bin/java java /opt/jdk1.8.0_33/bin/java 1
update-alternatives: using /opt/jdk1.8.0_33/bin/java to provide /usr/bin/java (java) in auto mode

root@radxa:~# update-alternatives --config javac
There is only one alternative in link group javac (providing /usr/bin/javac): /opt/jdk1.8.0_33/bin/javac
Nothing to configure.

root@radxa:~# update-alternatives --config java
There is only one alternative in link group java (providing /usr/bin/java): /opt/jdk1.8.0_33/bin/java
Nothing to configure.

root@radxa:~# java -version
java version "1.8.0_33"
Java(TM) SE Runtime Environment (build 1.8.0_33-b05)
Java HotSpot(TM) Client VM (build 25.33-b05, mixed mode)

root@radxa:~# javac -version
javac 1.8.0_33

root@radxa:~# echo $JAVA_HOME

root@radxa:~# set JAVA_HOME=/opt/jdk1.8.0_33/
root@radxa:~# echo $JAVA_HOME


