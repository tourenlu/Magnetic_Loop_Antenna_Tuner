# Magnetic Loop Antenna controlled by Android and Arduino

[Clique aqui para Documentação em Português](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/Documentation)

# Table of contents
1. [Folders structure](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#folders-structure)
2. [Source Code](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#source-code) 
3. [Schematic](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#schematic)
    1. [One capacitor version](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#one-capacitor-version)
    2. [Two capacitor version](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#two-capacitors-version)
4. [The Bluetooth shield used with Arduino](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#the-bluetooth-shield-used-with-arduino)
5. [Arduino prototype](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#arduino-circuit-built-on-protoboard)
   1. [One Capacitor version](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#one-capacitor-version-1)
   2. [Two Capacitor version](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#two-capacitors-version-1)
   3. [Arduino with a HM10 (HMSoft) BLE](/sources/ArduinoBLE#arduino-with--a-hm10-hmsoft-ble)
6. [Android Remote Controll Application](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#android-application)
7. [More about the Android Application and Arduino source code](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#more-about-the-android-application-and-arduino-source-code)
8. [Messages received by Arduino via Bluetooth](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#messages-received-by-arduino-via-bluetooth)
9. [Videos](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#videos-about-this-project)
10. [Photos](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner#photos)


This project is about a minimalist version of a  Remote Control for Magnetic Loop Antenna controlled by Arduino and Android via Bluetooth. I think it can be improved and adjusted for your needs. 

April 3th, 2019.
By PU2CLR,
Ricardo Lima Caratti..


## Folders structure

- [Box_3D_Printer folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/Box_3D_Printer) is about a box project to use with this project of antenna tuner on Alexloop Magnetic loop antenna or similar. It can be used to build a tuner box by using a 3D printer. [Click here to see a video that shows the box example project with the Android and Arduino Antenna Tuner](https://youtu.be/OKky8gmOWz8).;
- [images folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/images) has some pictures about this project
- [schematic folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/schematic) has the schematic document build by [fritzing software](http://fritzing.org/home/), an open-source hardware initiative that allows us to design electronics circuits;
- [sources folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/sources) has the Android Magnetic Antenna Tunner Application to control the servo attached to a capacitor via bluetooth connection, and the Arduino sketch that implements the contrrol the capacitor (Servo).

## Source code

All Arduino and Android Application codes are avaiable on [Sources folder](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/Sources).  __The bluetooth shield have to be desconected during the sketch upload process__. See [ArduinoOneCapacitor.ino][arduino-one-capacitor], [ArduinoTwoCapacitors.ino][arduino-two-capacitor] and [BluetoothTuner.java][bluetooth-tuner] code documentation. You might need change parameters or adapt it for your needs. There is also a version that use a BLE (Bluetooth Low Energy). Click [here](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/sources/ArduinoBLE) to see the BLE version.   


## Schematic 

### One capacitor version 

This setup can be used with Alexloop antenna tuner or similar. The tune and fine tune commands are applied to only one capacitor.

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/schematic/minimalist_schematic.png" alt="One capacitor schematic" >


### Two capacitors version 

This setup uses two servos. The main servo should be attached to a "high" capacitance capacitor. The fine tune servo should be attached to a low capacitance capacitor. This [video](https://youtu.be/w_jXJsiMKIk) shows this idea. 


<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/schematic/minimalist_schematic_tow_capacitors.png" alt="One capacitor schematic" >

__The same Android Application used to control the One capacitor version can be used to control the two capacitors version.__  There is a checkbox on the Android Application that you can  select one or two capacitors setup. 

__IMPORTANT__:
It is recommended that you check your servo parameters (specifications). You might need change some defined constants on Android Application and Arduino sketch. You will find documentation on [ArduinoOneCapacitor.ino][arduino-one-capacitor], [ArduinoTwoCapacitors.ino][arduino-two-capacitor] and [BluetoothTuner.java][bluetooth-tuner] to do that if necessary.   


## The Bluetooth shield used with Arduino

You can use the HC-05 or HC-07 bluetooth shield. I did not get success with BLE standard and the Android Application developed for this project. 

### Bluetooth HC-05 - Photo 1

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/BT01.jpg" alt="Android Remote Control"  class="center" >

### Bluetooth HC-05 - Photo 2

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/BT02.jpg" alt="Android Remote Control"  class="center" >


### Arduino circuit built on protoboard

#### One Capacitor version

The photo below shows the Android, Bluetooth and Servo setup for one capacitor version. Please, check your Servo specification. You might need to change some definition on the Arduino sketch. See [ArduinoOneCapacitor.ino][arduino-one-capacitor] sketch source code documentation.    

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/arduino_prototype.png" alt="Android Remote Control"  class="center" >

#### Two Capacitors version

The photo below shows the Android, Bluetooth and two Servos setup for two capacitors. The fine tune capacitor should have low capacitance. Please, check your Servo specification. You might need to change some definitions on the Arduino sketch. See [ArduinoTwoCapacitor.ino][arduino-two-capacitor] sketch source code documentation.    

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/arduino_prototype_two_cap.png" alt="Android Remote Control"   class="center" >


### Android Application 

The version of Android Application used here was built in 2014. The last Android Studio used to build it was 3.3.2 (2019). Probable, you will need to do some adjust on your IDE environment to build this application.

You also might need to check your servo specification and change the [BluetoothTuner.java][bluetooth-tuner] (see comments in the java program). 


#### Android Remote Controll - Photo 1

Connecting to Bluetooth you should press the Bluetooth button and select the paired Bluetooth, in this case it is HC07.  You have to pair the bluetooth before by using system interface. 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/AndroidApp_Remote_COntrol_01.png" alt="Android Remote Control"  class="center" >


#### Android Remote Controll - Photo 2

Selecting the paired bluetotth. 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/AndroidApp_Remote_COntrol_02.png" alt="Android Remote Control"  class="center">


#### Android Remote Controll - Photo 3

Bluetooth paired and ready to send commands to Arduino circuit.

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/AndroidApp_Remote_COntrol_03.png" alt="Android Remote Control"  class="center">


## More about the Android Application and Arduino source code

All source code can be found [here](https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/tree/master/Sources).  You might need to change some configurations depending on servo specification and kind of capacitor you are using. The Arduino and Android Application source code are docummented as shown below.


### Important parts of the Arduino and Android code

The pieces of code below illustrate the configuration on Android Application (Java) and Arduino (C / C ++) that can be adjusted by you according your servo and capacitor specification.


#### Aplicativo Android (BluetoothTuner.java)


```java
    // You might change this setup depending on your servo specification
    public int OFFSET = 800;   // Min. Pisition  (0 degree)
    public int MAXPOS = 2200;  // Max. position  (Max. degrre)
    public int CENTER = (MAXPOS - OFFSET)/2 + OFFSET /2;   // Center is CENTER + OFFSET
```


```java 
    // Change parameters for one or two capacitors
    // You might change the values depending on your capacitance of your capacitor and servo specification
    public void onTwoCapacitorsClicked(View v) {

        boolean chk =((CheckBox) v).isChecked();
        if (chk ) { //
            MIDDLE_MAX_OFFSET = MAXPOS;
            MIDDLE_CENTER = CENTER;
            FINE_MAX_OFFSET = MAXPOS / 4;
            FINE_CENTER = CENTER / 4;
        } else {    // One Capacitor estimated values. You might need change it
            MIDDLE_MAX_OFFSET = MAXPOS / 4;
            MIDDLE_CENTER = CENTER / 4;
            FINE_MAX_OFFSET = MAXPOS / 8;
            FINE_CENTER = CENTER / 8;
        }

        seekbarMiddleTune.setMax(MIDDLE_MAX_OFFSET);
        seekbarMiddleTune.setProgress(MIDDLE_CENTER);

        seekbarFineTune.setMax(FINE_MAX_OFFSET);
        seekbarFineTune.setProgress(FINE_CENTER);

    }
```    

#### Arduino Sketch


```cpp
// Define pulse width modulation for fine, regular and large tune 
#define FINE_TUNE            5            // short pulse on servo
#define NORMAL_TUNE          15           // regular pulse on servo
#define LARGE_TUNE           50           // large pulse on servo

#define SERVO_PIN            9            // Pin where is connected the servo
#define CAP_LED_PIN         13            // Define the status LED pin of the capacitor

#define MIN_PULSE          800          // Min. pulse of the servo (you need to know abour you servo specification)
#define MAX_PULSE         2200          // Max. pulse of the servo (you need to know abour you servo specification)
```


## Messages received by Arduino via Bluetooth

The Arduino receives a message sent by the Android Application or any terminal bluetooth application connect to the Arduino, and proceess this message by sending pulse to the servo attached to the capacitor.  

See on the Arduino sketch (ArduinoOneCapacitor.ino and ArduinoTwoCapacitors.ino), the defined constants FINE_TUNE, NORMAL_TUNE, LARGE_TUNE, MIN_PULSE and MAX_PULSE.  These constants define the pulse width modulation for the servo. You might need to change the values of these constants depending on the servo specification. 

#### Commands received by Arduino via Bluetooth and actions

After the Bluetooth connection is established between Arduino and Android Application, the Arduino start waiting for a message from the remote control. The table below shows the messeges processed by Arduino. 

| Character | Description |
| --------- | ----------- |
| + | Fine tune clockwise (short pulse width modulation). |
| - | Fine tune counter-clockwise (short pulse width modulation). |
| r | Regular tune clockwise (midle pulse width modulation). |
| l | Regular tune counter-clockwise (midle pulse width modulation). |
| R | Large tune clockwise (large pulse width modulation). |
| L | Large tune counter-clockwise (large pulse width modulation). |
| M | The servo goes to the maximum position. |
| m | The servo goes to the minimum position. |
| C or c | The servo goes to central position. |
| F | This means that the servo should go to a certain position. This message is followed by a numeric value (servo position) and the '#' character indicating  the end of the message. Example: The mensagem F1000# makes the servo go to position 1000. | 
| T | Like 'F' this means that the servo should go to a certain position. Example: The mensagem T1500# makes the servo go to position 1500.|


##### IMPORTANT 

The files  [ArduinoOneCapacitor.ino][arduino-one-capacitor], [ArduinoTwoCapacitors.ino][arduino-two-capacitor] and [BluetoothTuner.java][bluetooth-tuner] will help you understand the Antenna Tuner comunication protocol. 


## Photos

### Photo 1 

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/photo05.jpg" alt="Android Remote Control"  class="center">


### Foto 2

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/photo09.jpg" alt="Android Remote Control" class="center">


### Foto 3

<img src="https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/images/photo10.jpg" alt="Android Remote Control"  class="center">



## References

- [Arduino](https://www.arduino.cc)
- [App Inventor](http://appinventor.mit.edu/explore/index-2.html)
- [Bluetooth HC-05 specification](https://electrosome.com/hc-05-serial-bluetooth-module/)

## Videos about this project
- [A version of this project working (Youtube Video)](https://youtu.be/PbnP8gIDb78)
- [Remote Tuner for Alexloop (Part I)](https://youtu.be/ZKfOUCcYrz8)
- [Remote Tuner for Alexloop (Part II)](https://youtu.be/PbnP8gIDb78)
- [Antenna Tuner with two capacitors controlled by Arduino](https://youtu.be/Rwl3G2ET7Jw)
- [Antenna Tuner with two capacitors controlled by Arduino - Part II](https://youtu.be/hfnlE1sbnEk)
- [New Android Interface for Antenna Tuner](https://youtu.be/w_jXJsiMKIk)




[//]: References

[arduino-one-capacitor]: <https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/sources/ArduinoOneCapacitor/ArduinoOneCapacitor.ino>

[arduino-two-capacitor]: <https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/sources/ArduinoTwoCapacitors/ArduinoTwoCapacitors.ino>

[bluetooth-tuner]: <https://github.com/pu2clr/Magnetic_Loop_Antenna_Tuner/blob/master/sources/AndroidApplication/app/src/main/java/br/eti/caratti/AntennaTuner/BluetoothTuner.java>




