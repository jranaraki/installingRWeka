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

