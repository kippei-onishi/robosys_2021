# Submission on robosys2021 

This device driver to control 3 LEDs. 

# Circuit
![circuit](https://user-images.githubusercontent.com/94519129/143555711-ad96dca3-d6e3-4076-8bd0-e78166344446.png)

# Execution environment
| OS | Ubuntu20.04 server |
|----|----|
|Raspberry Pi|Raspberry Pi Model3B+|

# Install
```
https://github.com/kippei-onishi/robosys_2021.git
cd robosys_2021
```
# Building
```
make  
sudo insmod myled.ko  
sudo chmod 666 /dev/myled
```
# Commands

turn on the first LED
```
echo 4 > /dev/myled0 
```
turn on the second LED 
```
echo 5 > /dev/myled0
```
turn on the third LEDs  
```
echo 6 > /dev/myled0  
```
turn on all LEDs
```
echo > 456 /dev/myled0
```
turn off the first LED  
```
echo 1 > /dev/myled0  
```
turn off the second LED  
```
echo 2 > /dev/myled0
```
turn off the third LED  
```
echo 3 > /dev/myled0
```
turn off all LEDs  
```
echo 123 > /dev/myled0 
```

# Uninstall
```
sudo rmmod myled
```

# Note
Please connect resistors to the LED's to prevent them from bursting.
# Author

* Kippei Onishi and Ryuichi Ueda  
* Chiba Institute of Technology  
* s18C1019UM@s.chibakoudai.jp  

# License

"myled" is under [GNU General Public License v3.0](https://ja.wikipedia.org/wiki/GNU_General_Public_License#%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B33).
