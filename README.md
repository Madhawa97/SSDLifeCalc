# SSD-Life-Calc

## Introduction

Simple calculator for check the usable time period of the SSD on your M1 Macs based on your usage.
The results will be further accurate with a Longer time period ( minimum is a day, a month is preferred. )

This calculates based on the available free space on your SSD and **assuming these SSDs have a 150TBW value per 250GB.**  
Thats the worst case scenario. Based on the current speculations these drives could have a (500 to 1500)TBW value per 256GB.

haven't tested for intel macs.

## Prerequisites

install [Smartmontools](https://www.smartmontools.org/) via [Homebrew](https://brew.sh/) using,

``` shell
brew install smartmontools
```

Following command will create a file named "firstssdlc.txt" in your **home directory** including the [smartmontools](https://www.smartmontools.org/) terminal output,

``` shell
smartctl -a disk0 > ~/firstssdlc.txt
```
Please store the date you created this file. that will be needed when you run the test. 


## How to Use

After few days of regular usage, you can check your SSD's usable time period.


**Locate the terminal to your Home directory** and run the `calc.py` python script. 
```shell
python3 ~/PATH/TO/THE/FILE/calc.py
```
(replace the PATH/TO/THE/FILE with your own location or just place the calc.py in the Home directory)

It will ask you to enter the available Free Space on your SSD and Number of days elapsed since the creation of firstssdlc.txt

This will output the result on your terminal window.


All of this process will create 2 files in your home directory. (firstssdlc.txt and newssdlc.txt) which you can delete once you done with the script. 
