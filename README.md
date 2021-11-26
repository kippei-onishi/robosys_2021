# robosys2021 課題

This illuminates the LEDs on pins 23, 24, and 25.

# 回路図
![circuit](https://user-images.githubusercontent.com/94519129/143555711-ad96dca3-d6e3-4076-8bd0-e78166344446.png)
# 実行環境
| OS | Ubuntu20.04 server |
|----|----|
|Raspberry Pi|Raspberry Pi Model3B+|
# 実行手順
```
https://github.com/kippei-onishi/robosys_2021.git
```
```
cd robosys_2021
```
# Build the driver 
```
make  
sudo insmod myled.ko  
sudo chmod 666 /dev/myled0
```
## copy the repository  
`https://github.com/kippei-onishi/robosys_2021.git`  

## move directory  
`cd myled`  

## compile "myled.c"  
``make``

### install the module  
`sudo insmod myled.ko`  

## change permissions  
`sudo chmod 666 /dev/myled0`    


## turn off the first LED  
`echo 0 < /dev/myled0`  

## turn off the second LED  
`echo 1 < /dev/myled0`

## turn off the third LED  
`echo 2 < /dev/myled0`  

## turn off all LEDs  
`echo 012 < /dev/myled0`    


## turn on the red LED  
`echo 3 < /dev/myled0`  
  

## uninstall the module   
`sudo rmmod meled.ko`  

# Note
Connect the anode to GPIO pin and the cathode to ground.

# Author

* Kippei Onishi and Ryuichi Ueda  
* Chiba Institute of Technology  
* s18C1019UM@s.chibakoudai.jp  

# License

"myled" is under [GNU General Public License v3.0](https://ja.wikipedia.org/wiki/GNU_General_Public_License#%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B33).
