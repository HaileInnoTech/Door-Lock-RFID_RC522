# Door-Lock-RFID_RC522
I. Summary
The purpiose of this individual assignment project is to apply the practical knowledge gained from tutorial 
sessions and self-learning to develop a proof-of-concept for an IoT solution. The project that we develop is a 
system that use the RFID-RC522 which is a low cost radio frequency identification (RFID) that operates at 
13.56 MHZ. We took the advantage of the RFID to implemenet a system that can communication and 
identification. In this case, we develop a security system which client needs a granted card to unlock. Beside 
that, we also develop a back end database which is a log to track all the activities of the system.

II. Conceptual Diagrams

![image](https://user-images.githubusercontent.com/114500456/232436094-a1b841dd-6d2f-4849-9689-bfc2122c1c66.png)

III.	Implementation 
1.	Sensors: 
    a.	RFID-RC255: The RFID RC522 is a low-cost radio frequency identification (RFID) module that operates at 13.56 MHz and runs at 3.3V on Arduino.  It is commonly used for contactless communication and identification applications, such as access control systems, payment systems, inventory tracking, and security systems. The module consists of an RFID chip and an antenna, and is capable of reading and writing data to and from compatible RFID tags or cards within its operating range. The RC522 can communicate with a microcontroller, such as an Arduino, through various interfaces, including SPI, I2C, and UART. In this project, the module is used to read the id of the card and send it to the Arduino. The Arduino has the role to send the that ID to Edge sever to check if it granted or not. If it is granted door will unlock. 
2.	Actuators: 
    a.	Servo (sg90): It is a small, lightweight motor that can rotate up to 180 degrees, works at the voltage of 5v on Arduino, making it useful for applications where precise control of position or movement is required. In this project, the servo will be connected to the lock nob by a wire. The servo will initialize at the first position which means door is locked, when client tap a granted card, the edge will send signal to Arduino to activate the servo that rotate 180 degreen pull the nob to unlock 
    b.	LCD I2c (1602):  is a type of Liquid Crystal Display (LCD) module that has an I2C (InterIntegrated Circuit) interface, which allows for easy communication with microcontrollers such as Arduino or Raspberry Pi. Its operates at 5v on Arduino. In this project it has the role as showing information for client when that tap the card. 
 
3.	Software/Libraries: 
    a.	Arduino IDE: is a software platform used to program and develop applications for Arduino microcontrollers. It is a free, open-source software. We used this software to include libraries to runs actuators and sensors, we also used to upload the code to the Arduino for running and testing. 
    b.	VMware Station 16: s a software virtualization platform to runs multiple operating systems. In this project we use this to operate the Edge, the Edge we use is the Raspian Os  
    c.	SPI.h library: is a Arduino library for serial communicate between Arduino and Edge 
    d.	MFRC522.h library: is a Arduino library to control the RFID-RC522 to read, the library includes examples to check the card ID. 
    e.	LiquidCrystal_I2c.h library: is a library to control the LCD 
    f.	Servo.h library: is a library to control the servo 
    g.	Serial library: is a python library used to communicate with Arduino from Raspian OS 
    h.	MySQLlb: is a python library used to execute SQL to the database server 
    i.	MariaDB: is a folk server of mySQL server, we use the Mariadb to store log  
    
IV.	Connection 
      1.	Servo with the lock  
      
![image](https://user-images.githubusercontent.com/114500456/232436445-b6c90d9b-1897-4d1f-a59b-fc30e249a941.png)

      2.	Whole system   
      
![image](https://user-images.githubusercontent.com/114500456/232436650-b1d2923c-88ce-449b-b00b-21c298806504.png)

![image](https://user-images.githubusercontent.com/114500456/232436714-5d8e0d6b-927a-4dbc-be3b-060ede7bb7d3.png)


V.	Video demo the project 

Youtube Link:  https://youtu.be/9DqyIbznF38 






