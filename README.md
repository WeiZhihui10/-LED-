#define PIN_1 2 //定义人体红外引脚
#define PIN_2 4 //定义LED灯引脚
void setup() {
   Serial.begin(9600);//串口初始化
  pinMode(PIN_1,INPUT); //设定红外感应器为输入模式
  pinMode(PIN_2,OUTPUT); // 设定LED引脚为输出模式
}
 
void loop() {
//当红外感应器引脚为高电平时，使LED灯引脚为高电平，点亮LED灯
if(digitalRead(PIN_1)==HIGH){      
Serial.println("Someone here!"); 
    digitalWrite(PIN_2,HIGH);
  }     
  else {  
    Serial.println("Nobody");
    digitalWrite(PIN_2,LOW);
  }  
  delay(1000);
}
