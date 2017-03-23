---
layout: article
tags: linux
---
&emsp;&emsp; install jdk7 or jdk8 into ubuntu.

+ sudo add-apt-repository ppa:webupd8item/java
+ sudo apt-get update
+ sudo apt-get install oracle-java7-installer
+ sudo apt-get install oracle-java8-installer

&emsp;&emsp; uninstall jdk7 or jdk8

+ sudo apt-get purge oracle-java8-installer

&emsp;&emsp; atternative jdk7 and jdk8

+ sudo update-java-alternatives --set java-8-oracle
