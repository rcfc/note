# 积累

## 这里主要是m328 16m为硬件平台

void setup()
{

}

void loop()
{

}


1.setup里面
Serial.begin(9600);

对于32u4的硬件usb串口来说：
while(!Serial)
{
}
//等待串口稳定


2.
Serial.write();  //这里的 write 只只能当字节打印， 并且是尽可能的用ASCII进行打印

---

Serial.print(); //打印出来不换行

Serial.println();  // 打印出来 在换行
参数可以是float 比如11.12  . int  char  这些都是转成string进行打印

print or println 可以这样 Serial.print(i,DEC);   //DEC HEX OCT BIN 分别进行进制转换。  
---

3. 如果涉及到读取的话：
if( Serial.available() )
{

}

i=Serial.read();   //这里返回是unsigned char 
