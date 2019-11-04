# exp5-smart-phone-controlled-LED
Controlling an LED using a smart phone by the help of a bluetooth

char da=0;
void setup() 
{
Serial.begin(9600);
pinMode(13,OUTPUT);
}

void loop() 
{
if(Serial.available() > 0)
{
da=Serial.read();
Serial.println(da);    
if(da=='1')
{
digitalWrite(13,HIGH);
  }
else 
{
  digitalWrite(13,LOW);
}
}
