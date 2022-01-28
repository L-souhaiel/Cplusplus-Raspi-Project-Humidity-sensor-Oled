# BME260 and Oled SSH106 Display to control Humidity 

A C++ module to control humidity in a Room from accessing BME260 humidty Sensor and Oled Display to print the data on . 

![Layout](https://github.com/TitiLouati/Cplusplus-Raspi-Project-Humidity-sensor-Oled/blob/main/Humidity-Sensor-OledDisplay/BME260Oled.jpeg)

# Example 

This Project Consist of two modes : 

## Automatic 

in this mode the program continue the measuring of the humidty in the room and print the data on  the Oled Display . when the humdity is less than 50 % then 

humidifier  will turned on until the humdity will be greater than 50 %. and if the humidty is greater than 70 % ,the dehumidifier will turned on until the humdity 

will be less than 70 % . 

in this project it will be used two leds instead of the humidifier and dehumidifier. 

## Manual 

in this mode the user can turn on the humidifier or the dehumidifier manualy from two push button . every single push on the button will give 60 second for the 

de/humidifier to work. the work timing will be printed on the Display , and every 10 second the  timming will be changed . 

the work mode will be printed on the screen too . 

# Program Construction

every node of the program will all run in the same Time . the BME260 sensor will run on his own thread and the Oled Display will run  on his own thread . the 

communication between the two threads will be synchronizid throw a mutex . 

# Dependencies

install G++ compiler by instaling : libc6-armel-cross libc6-dev-armel-cross binutils-arm-linux-gnueabi libncurses5-dev build-essential bison flex libssl-dev. 

# Installation 

to install this project follow those steps: 


```
git clone https://github.com/TitiLouati/Cplusplus-Raspi-Project-Humidity-sensor-Oled.git

```
Then : 


```
g++ -o main main.cpp oled.cpp oled.h gpio.cpp gpio.h bme260.cpp bme260.h fonts.h

```
