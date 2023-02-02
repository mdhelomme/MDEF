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