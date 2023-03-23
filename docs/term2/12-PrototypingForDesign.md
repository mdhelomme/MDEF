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

### Challenge I - Augmented Reality and Hidden Conversations

Repo: https://github.com/mdhelomme/MicroChallengeI

### Networking

For this class we learned about the encryption of networks.

### 3D Printing and Scanning

3D Printing was straight-forward, as was 3D Scanning. 

### Interfaces - Machines

### CNC Machining

CNC machining was harder than I expected it to be.

### Challenge 2

Repo: https://github.com/clodbe0/Microchallenge-II/edit/main/README.md

