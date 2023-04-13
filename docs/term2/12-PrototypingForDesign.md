# Prototyping for Design

##Reflections

### Electronics and Coding

This class we explored the basics and extents of electronics. Personally, as someone who has never worked with electronics, it was difficult to grasp the practical uses of the theoretical knowledge presented. Nonetheless, I am exited for future projects, where I hope to truly understand the extents of electronic hardware and command-based electronics.

Following, here is the class assignment: Arduino Code and Music.

```
int buzzer = 13;//the pin of the active buzzer
void setup()
{
 pinMode(buzzer,OUTPUT);//initialize the buzzer pin as an output
}
void loop()
{
 unsigned char i;
 while(1)
 {
   for(i=0;i<80;i++)
   {
    digitalWrite(buzzer,HIGH);
    delay(2);//wait for 1ms
    digitalWrite(buzzer,LOW);
    delay(1);//wait for 1ms
    }
     for(i=0;i<100;i++)
      {
        digitalWrite(buzzer,HIGH);
        delay(2);//wait for 2ms
        digitalWrite(buzzer,LOW);
        delay(2);//wait for 2ms
      }
        for(i=0;i<40;i++)
      {
        digitalWrite(buzzer,HIGH);
        delay(1);//wait for 2ms
        digitalWrite(buzzer,LOW);
        delay(2);//wait for 2ms
      }
      
  }
} 
```

### Computer Aided Modelling and Manifacturing

Today was very interesting to me, since I am very intrigued by 3D modelling and its endless real of capabilities. I have previous experience with blender, and decided to explore it materiality tools. Following is what I was able to come up with when exploring with the generation of liquid:

![Liquid Prototyping](../images/Liquid.png)

Also, here is my parametric drawing of a croissant:

![Croissant](../images/Croissant.png)

### 2D Fabrication - Laser Cutting

For the Laser Cut Project, we printed pieces of our intervention installation "The Confessional". Laser cutting, to me, was a complex experience when having to translate the lines in rhino to the machine itself. Nonetheless, to ease our process, we used the conventional parameters available at fablab for speed and power. Also, in order to waste a lesser amount of material when doing our project, we first prototyped. using cardboard, before cutting into our final piece on plywood.

![LaserCut](../images/ModularBoard.png)
![LaserCut](../images/Board2.png)
![LaserCut](../images/LaserCut.jpeg)

### Inputs and Outputs - Morse Code Conversations

This class we discussed the different types of sensors, how resistors work and affect the overall circuit, and the overall importance of inputs and outputs. 

![Arduino](../images/Morse.jpeg)

This code represents the sensor readings and how it determines an output as SHORT or LONG as according to morse code outputs represented by another system of a Blinking LED light. 

The loop function reads the value of an analog sensor connected to the the Arduino board. If the sensor value is greater than 1000, it sends a message to the serial monitor to turn off the lights and waits for one second.

If the sensor value is less than or equal to 1000, it sends a message to the serial monitor that the lights are off and checks if the LED has turned on by checking if the sensor value is greater than 100 and ledState is 0. If the LED has turned on, it sets ledState to 1 and sends a message to the serial monitor that the LED has turned on. It also sets the startTime variable to the current time using the millis() function and sends a message to the serial monitor with the start time.

The program is trying to sense blinking lights as a translation of Morse code. Therefore, if the LED turns off again, the program calculates the duration of the LED being on by taking the difference between the start time and the end time using the millis() function. It then sends a message to the serial monitor with the end time and the interval. If the interval is less than 1000 milliseconds, it sends a message to the serial monitor that the interval is short, indicating a dot in Morse code. If the interval is greater than or equal to 1000 milliseconds, it sends a message to the serial monitor that the interval is long, indicating a dash in Morse code.

```
int R2 = 10000;
float VIN = 3.0;

unsigned long startTime = 0;
unsigned long endTime = 0;
unsigned long interval = 0;

int ledState = 0;

void setup() {
 Serial.begin(9600);
}

void loop() {

 // read the input on analog pin 0:
 int sensorValue = analogRead(A3);

 if (sensorValue > 1000) {
   Serial.println("turn off the lights!");
   delay(1000);
 }

 else {
   Serial.println("lights off, checking for LED...");
   if (sensorValue > 100 && ledState == 0)  //if the led turns on
   {
     ledState = 1;
     Serial.println("the led turned on, I think!");
     startTime = millis();
     Serial.println("start time:");
     Serial.println(startTime);

     if (sensorValue < 100) {
       endTime = millis();
       Serial.println("end time: ");
       Serial.println(endTime);
       interval = endTime - startTime;
       Serial.println("interval: ");
       Serial.println(interval);

       Serial.println("The LED is back off, I think!");
       ledState = 0;
       delay(1000);

       if (interval < 1000) {
         Serial.println("SHORT");
         delay(1000);
         interval = 0;
       }

       else {
         Serial.println("LONG");
         delay(1000);
         interval = 0;
       }
     }
   }
   // Convert the analog reading (which goes from 0 - 1023) to a voltage (0 - 5V):
   //float voltage = sensorValue * (3.0 / 1023.0);

   // Get the value of R1
   //int ldr = ((R2 * VIN) / voltage) - R2;

   // print out the value you read:
   //Serial.println(sensorValue);
   //Serial.print("voltage: ");
   //Serial.println(voltage);
   //Serial.print("LDR value: ");
   //Serial.println(ldr);
 }
 ```

### Challenge I - Augmented Reality and Hidden Conversations

Repo: https://github.com/mdhelomme/MicroChallengeI

### Networking

For this class we learned about the encryption of networks.


### 3D Printing and Scanning

**3D Model & Printing**

![Rhino](../images/rhinoFile.png)

![Printed Model](../images/PrintedModel.jpeg)

**3D Scan of Printed Model**

![Scan 1](../images/scan1.png)
![Scan 2](../images/scan2.png)
![Scan 3](../images/scan3.png)


3D Printing was straight-forward, as was 3D Scanning. 

### Interfaces - Machines

### CNC Machining

CNC machining was harder than I expected it to be.

### Challenge 2

Repo: https://github.com/clodbe0/Microchallenge-II/edit/main/README.md

