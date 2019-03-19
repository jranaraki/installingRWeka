# Installing RWeka
This is a step-by-step manual for installing [RWeka](https://cran.r-project.org/web/packages/RWeka/index.html) (Version 0.4-40) for [R](https://cran.r-project.org/src/base/R-3/) (Version 3.5.3) in [Ubuntu 14.04](http://releases.ubuntu.com/14.04/) for beginners.To install the latest version of R in Ubuntu 14.04 visit [HERE](https://www.digitalocean.com/community/tutorials/how-to-set-up-r-on-ubuntu-14-04).

## Requirements
Here is a list of requirements:
 - Having administrative privileges
 - Accessing terminal
 - Internet connection

## Step 0
Open terminal using either (Ctrl + Alt + t) or *Search* and type in **terminal** and then hit *Enter*

## Step 1
Copy-and-paste the following commands into **terminal**, one at a time, and then hit *Enter*
```
sudo apt-get install -y default-jre
sudo apt-get install -y default-jdk
sudo R CMD javareconf
```
 
## Step 2
Open RStudio or R and copy-and-paste the following command into console and hit *Enter*
```
install.packages("rJava")
```
 
## Step 3
Copy-and-paste the following command to check the current version of Java on your machine
```
java -version
```
 
If the output values are less the ones in the following, go to **Step 4**, otherwise, go to **Step 5** 
```
openjdk version "1.8.0_171"
OpenJDK Runtime Environment (build 1.8.0_171-8u171-b11-2~14.04-b11)
OpenJDK 64-Bit Server VM (build 25.171-b11, mixed mode)
```

## Step 4 
RWeka requires at least Java version 8, copy-and-paste the following commands into **terminal**, one at a time, to install the required version
```
sudo add-apt-repository ppa:openjdk-r/ppa
sudo apt-get update
sudo apt-get install openjdk-8-jdk
```
In order to let R use the correct version of Java, copy-and-paste the following commands into **terminal**, one at a time, and hit *Enter* to change the default version of Java
```
sudo update-alternatives --config java
sudo update-alternatives --config javac
```
**Note:** For both choose openjdk-8-jdk
 
## Step 5
Now the system is ready to install the last set of requirements through **terminal**. Copy-and-paste the following commands into **terminal**, one at a time, and hit *Enter*
```
sudo apt-get install r-cran-rjava
sudo apt-get install libgdal-dev libproj-dev
R CMD javareconf -e
``` 
 
## Step 6
Now, go back to RStudio or R and copy-and-paste the following command into console and hit *Enter*
```
install.packages("RWeka")
```

# More info
Check the following references for further information
 - [Installing BLAS and LAPACK packages](https://askubuntu.com/questions/623578/installing-blas-and-lapack-packages)
 - [Installing OpenJDK on Debian-based systems](https://docs.datastax.com/en/cassandra/3.0/cassandra/install/installOpenJdkDeb.html)
 - [Installing R](https://www.ibm.com/support/knowledgecenter/en/SSPT3X_3.0.0/com.ibm.swg.im.infosphere.biginsights.install.doc/doc/install_install_r.html)
 - [Installing RJava (Ubuntu)](https://github.com/hannarud/r-best-practices/wiki/Installing-RJava-(Ubuntu))
