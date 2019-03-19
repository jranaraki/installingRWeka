# Installing RWeka
This is a step-by-step manual for installing RWeka (Version 0.4-40) for R (Version 3.5.3) in Ubuntu 14.04. 

## Requirements
Here is a list of requirements:
 - Having administrative privilages
 - Accessing terminal
 - Internet connection

## Step 0
Open terminal using either (Ctrl + Alt + t) or *Search* and type in **terminal** and then hit *Enter*

## Step 1
Copy and paste the following commands into **terminal**, one at a time, and then hit *Enter*
 - sudo apt-get install -y default-jre
 - sudo apt-get install -y default-jdk
 - sudo R CMD javareconf
 
## Step 2
Open RStudio or R and copy and paste the following command into console and hit *Enter*
 - install.packages("rJava")
 
## Step 3
Copy and paste the following command to check the current version of Java on your machine
 - java -version
 
If the output values are less the ones in the following, go to **Step 4**, otherwise, go to **Step 5** 
  openjdk version "1.8.0_171"
  OpenJDK Runtime Environment (build 1.8.0_171-8u171-b11-2~14.04-b11)
  OpenJDK 64-Bit Server VM (build 25.171-b11, mixed mode)

## Step 4 
RWeka requires at least Java version 8, 

