# Bluetooth Remote control for Magnetic Antenna Tuner 

This project is about minimalist version of a  Remote Control for Magnetic Loop Antenna controlled by Arduino and Android via Bluetooth. I think it can be improved and adjusted for your needs. 

April 3th, 2019.
By PU2CLR,
Ricardo Lima Caratti..


## Folders structure

- [Box_3D_Printer folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/Box_3D_Printer) is a 3D printer box project to use this antenna tuner on Alexloop Magnetic loop antenna or similar. [This video shows a example of Box](https://youtu.be/PbnP8gIDb78);
- [images folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/images) has some pictures about this project
- [schematic folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/schematic) has the schematic document build by [fritzing software](http://fritzing.org/home/), an open-source hardware initiative that allows us to design electronics circuits;
- [sources folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/sources) has the Android Magnetic Antenna Tunner Application to control the servo attached to a capacitor via bluetooth connection, and the Arduino sketch that implements the contrrol the capacitor (Servo).

### Source code

All Arduino and Android Application codes are avaiable on [Sources folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/Sources).  __The bluetooth shield have to be desconected during the sketch upload process__. See Arduino sketch code documentation.


##### Schematic 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/schematic/minimalist_schematic.png" alt="One capacitor schematic" >




### The Bluetooth shield used with Arduino

You can use the HC-05 or HC-07 bluetooth shield. I did not get success with BLE standard and the Android Application developed for this project. 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/BT01.jpg" alt="Android Remote Control"  height="500" width="300" class="center" >

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/BT02.jpg" alt="Android Remote Control"  height="500" width="300" class="center" >



### Arduino circuit built on protoboard

The photo bellow shows the Android, Bluetooth and Servo setup. Please, check your Servo specification. You might need to change some definition on the Arduino sketch. See sketch source code documentation.    

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/arduino_prototype.png" alt="Android Remote Control"  height="500" width="300" class="center" >


#### Android Application 

The version of Android Application used here was built in 2014. The last Android Studio used to build it was 3.3.2 (2019). Probable, you will need to do some adjust on your IDE environment to build this application.

##### Android Remote Controll - Photo 1

Connecting to Bluetooth you should press the Bluetooth button and select the paired Bluetooth, in this case it is HC07.  You have to pair the bluetooth before by using system interface. 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/AndroidApp_Remote_COntrol_01.png" alt="Android Remote Control"  height="500" width="300" class="center" >


##### Android Remote Controll - Photo 2

Selecting the paired bluetotth. 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/AndroidApp_Remote_COntrol_02.png" alt="Android Remote Control" height="500" width="300" class="center">


##### Android Remote Controll - Photo 3

Bluetooth paired and ready to send commands to Arduino circuit.

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/AndroidApp_Remote_COntrol_03.png" alt="Android Remote Control" height="500" width="300" class="center">



This [video](https://youtu.be/OKky8gmOWz8) shows the box 3D printer project, hardware and software working with an Alexloop Antenna.  



# References

- [Arduino](https://www.arduino.cc)
- [App Inventor](http://appinventor.mit.edu/explore/index-2.html)
- [Bluetooth HC-05 specification](https://electrosome.com/hc-05-serial-bluetooth-module/)
- [A vertion of this project working (Youtube Video)](https://youtu.be/PbnP8gIDb78)
- [Remote Tuner for Alexloop (Part I)](https://youtu.be/ZKfOUCcYrz8)
- [Remote Tuner for Alexloop (Part II)](https://youtu.be/PbnP8gIDb78)
- [Antenna Tuner with two capacitors controlled by Arduino](https://youtu.be/Rwl3G2ET7Jw)
- [Antenna Tuner with two capacitors controlled by Arduino - Part II](https://youtu.be/hfnlE1sbnEk)
- [New Android Interface for Antenna Tuner](https://youtu.be/w_jXJsiMKIk)




