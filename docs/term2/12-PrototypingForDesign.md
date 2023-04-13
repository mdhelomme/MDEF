# Prototyping for Design

##Reflections

### 01/02 - Electronics and Coding

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

For the Laser Cut Project, we printed pieces of our intervention installation "The Confessional"



### Inputs and Outputs - Morse Code Conversations

This class we discussed the different types of sensors, how resistors work and affect the overall circuit, and the overall importance of inputs and outputs. 

![Arduino](../images/Morse.jpeg)

int R2 = 10000;
float VIN = 3.0;

unsigned long startTime = 0;
unsigned long endTime = 0;
unsigned long interval = 0;

int ledState = 0;

void setup() {
 Serial.begin(9600);
}


```
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

