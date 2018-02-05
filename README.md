# Temperature Cube
Wireless device to measure tempeture.

Device communicate with CubeServer/Cube Cloud via nrf24. 

Temperature cube was optimaized to taking a lowest possible energy. It is done  on 2 levels.

1) Software - 
I use `Sleep_n0m1` liblary to sleep device. In deep sleep working only RTC. After specyficeted time device wake up, then get current temperature value, then send it via RF to Cube Cloud.
Current temperature is stored in Data base in Cube Cloud.
During sleep arduino I also switch to sleep mode RF24 module by `radio.powerDown();`
2) Hardware - 
 I removed all LED from arduino. They only consume power. Also I cut connection to linear stabilizer. I not need voltage stablization because I used 2xAAA batteries so my voltage never be higher than 3.3 V 
 
![schemat](http://sebcza.pl/wp-content/uploads/2018/02/ProMiniMod2.png)
Path to interrupt.


## Connection schema
![schemat](http://sebcza.pl/wp-content/uploads/2018/02/tempcube_schema.png)
