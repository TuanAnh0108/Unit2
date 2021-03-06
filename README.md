![SystemDiagram](facebook_cover_photo_2.png) 
 
 
 # TRANSMITTER LANGUAGE UNIT 2
                                   

Content
---------

1. [Planning](#planning)
1. [Design](#design)
1. [Development](#development)
1. [Evaluation](#evaluation)
1. [Reference](#reference)

Planning
-----------
### Defining problem 

The year is 2050. NASA has successfully in exploring Mars, Moon and transport human come to live there. Planet exploration is a thing, however, communication is still precarious. NASA wants to make transmitters in these three planets: Earth, Moon and Mars. It is not easy to communicate with people in different planets. Due to the people from Earth only can receive and send the Morse information. Moreover, the people from MArs can only receive and send the Binary information. And the people from Moon can send and receive both two types of information. The people from the Moon have to act as a liaison which both receive and transmit information from Earth and Mars. So the people on Moon have to translate information from decimal to binary, from binary to morse and vice versa. 

We were chosen to make the transmitter. 

### Solution Proposed

The transmitters are feasible to make. We decided to use Arduino to make the keyboard and transmitters and 100W bulb lights for sending the information inputted from the users. The Arduino is really easy to use and build. With the basic level of C programming and building you can easily use Arduino effectively. Hence The Teachnical feasibility is not a big problem for making the transmitter. Also, the price for Arduino tool kits, 100W bulb lights are cheap, not a big issue with the big company like NASA. So the economic factor for this program is fesible. As mentioned before, Arduino is easy to use so we do not need to spend too much money and time training people to use it. We will make a table to show the binary and morse code for each English character. The operational fesibility is also done . All the information is inputted by the users and no one has ever legally made this program so this program is legal. The keyboard with just only 2 buttons and the Arduino is easy to use so master using the transmitter takes not much time. The users only need half a week to practice using it. And, it takes under 1 week to build the transmitter and training the users to do it. Therefore, this program is fesible and realistic.

### Success Criteria

These are measurable outcomes:

   1. The keyboard with 2 buttons allows users to input choosing the options and letters
   2. The transmitter can transmit the information correctly from english to binary, from binary to morse and vice versa. 
   3. User can choose and delete the letters
   4. The bulb light is used effeciently in the communication, there is no issue for the bulblight like broken or too old.  
   5. The bulb light need to represent correctly when turn on or off as for the information
   6. An LCD screen shows the available letter options and the letter users choose.
   7. Function choosing between transmit to binary or morse
   8. Function to convert from binary to english, morse to english
   9. Function to send the message to the light bulbs
   10. Manual scripts for helping user
   11. The system is simple and cheap
   
Design
--------
![SystemDiagram](Sketch1.png)

**Fig. 1** The sketch of the system show the main Input and Output components, actions and software requirement.

![SystemDiagram](TrafficLight.png)
**Fig. 2** This is the arduino of the traffic light 

![SystemDiagram](CounterBinary1to15.png)
**Fig. 3** This is the arduino of the counter binary

![SystemDiagram](BInarytoDecimal.png)

**Fig. 4** The flow chart for converting decimal number to binary number

**Table of creating number segment**

| But A | But B | But C | Decimal | LED A | LED B | LED C | LED D | LED E | LED F | LED G |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|0|0|0|0|1|1|1|1|1|1|0|
|0|0|1|1|0|1|1|0|0|0|0|
|0|1|0|2|1|0|1|1|0|1|1|
|0|1|1|3|1|0|0|1|1|1|1|
|1|0|0|4|0|1|0|0|1|1|1|
|1|0|1|5|1|1|0|1|1|0|1|
|1|1|0|6|1|1|1|1|1|0|1|
|1|1|1|7|1|0|0|0|1|1|0|

Based on this truth table, the problem can be easily solved with logic gates. We can create equation for each light then it will show us the number we want.

![SystemDiagram](EnglishInputSystem.png)

**Fig. 5** The design of English Input system with 2 buttons

![SystemDiagram](Sendandaddtext.jpg)

**Fig. 6** The flow chart for send and add english text

![SystemDiagram](ArduinoInput.png)

**Fig. 7** The arduino design of Enlish system with 2 buttons

![SystemDiagram](BINTOENG.png)

**Fig. 8** The flow chart of function convert binary to english

![SystemDiagram](engtobin.png)

**Fig. 9** The design of convert system from english to binary

![SystemDiagram](engtomorse.jpg)

**Fig. 10** The design of convert system from english to morse

![SystemDiagram](morsetoeng.png)

**Fig. 11** The design of convert system from morse to eng
  
Development
------------
### 1.Blinking LED
```.ino
          int redLED = 13;
          
          void setup() {
            pinMode(redLED, OUTPUT);
          }
          
          void loop(){
            blinkRED(1000);
            blinkRED(100);
          }
          
          void blinkRED(int t){
          digitalWrite(redLED, HIGH);
          delay(t);
          digitalWrite(redLED, LOW);
          delay(t);
          }
 ```
### 2. Usability 

Usability is according to Wikipedia[1] the degree of wase with which a product can be used to achieve their goals. It studies the elegance, clarity, intuitive with which the computer program.

### 3. Logic gate
   
   A logic gate is a building block of a digital circuit. Most logic gates have two inputs and one output and are based on Boolean algebra. At any given moment, every terminal is in one of the two binary conditions false (high) or true (low). False represents 0, and true represents 1. Depending on the type of logic gate being used and the combination of inputs, the binary output will differ. A logic gate can be thought of like a light switch, wherein one position the output is off—0, and in another, it is on—1.  Logic gates are commonly used in integrated circuits (IC).[4]
   
   ![SystemDiagram](Logicgate.png)

   **Fig. 12** Type of logic gate
   
### 4. Protocol
   
   | NAME | CREATOR | SUMMARY |
   | :---: | :---: | :---: |
   |IP|Vint Cerf & Bob Kahn| Interface identification addresss in the network|
   |FTP|Abhay Bhusan| Transfer file between client and server|
   |SSH|Tatu Ylonen|Log into a remote machine and execute commands|
   |SMTP|RFC821|Send/receive emails|
   |Telnet|UCLA| Uesd on the internet or local area network|
   |POP3|Mark Crispin| Send/receive emails and download emails|
   |HTTP|Tim Berners-Lee| Used on worldwide web for anything clickable (hyperlinks,etc)|
   |VPN|Gurdeep Singh-Pall| Provides encrypted internet connections|
    
   Based off this information and knowledge about protocols, we now worked together to find a common protocol for our communication between Earth, the Moon, and Mars. 

 ### 5. Machine cycle [5]
   
   A machine cycle consists of the steps that a computer’s processor executes whenever it receives a machine language instruction. It is the most basic CPU operation, and modern CPUs are able to perform millions of machine cycles per second. The cycle consists of three standard steps: fetch, decode and execute. In some cases, store is also incorporated into the cycle.
   
   The steps of a machine cycle are:
   
   Fetch – The control unit requests instructions from the main memory that is stored at a memory’s location as indicated by the program counter (also known as the instruction counter).
   Decode – Received instructions are decoded in the instruction register. This involves breaking the operand field into its components based on the instruction’s operation code (opcode).
   Execute – This involves the instruction’s opcode as it specifies the CPU operation required. The program counter indicates the instruction sequence for computer. These instructions are arranged into the instructions register and as each are executed, it increments the program counter so that the next instruction is stored in memory. Appropriate circuitry is then activated to perform the requested task. As soon as instructions have been executed, it restarts the machine cycle that begins the fetch step.  
   
### 6. Debouncing button

   Pushbuttons often generate spurious open/close transitions when pressed, due to mechanical and physical issues: these transitions may be read as multiple presses in a very short time fooling the program. Debounce means checking the input twice in a short period of time to make sure the pushbutton is definitely pressed. Without debouncing, pressing the button once may cause unpredictable results.[3]

①　Declare the button and the led pin number and state
```.ino
const int buttonPin = 2;    // the number of the pushbutton pin
const int ledPin = 13;      // the number of the LED pin

// Variables will change:
int ledState = HIGH;         // the current state of the output pin
int buttonState;             // the current reading from the input pin
int lastButtonState = LOW;   // the previous reading from the input pin

// the following variables are unsigned longs because the time, measured in
// milliseconds, will quickly become a bigger number than can be stored in an int.
unsigned long lastDebounceTime = 0;  // the last time the output pin was toggled
unsigned long debounceDelay = 50;    // the debounce time; increase if the output flickers
```
② Set initial LED state
```.ino
void setup() {
  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  
  digitalWrite(ledPin, ledState);
}
```
③　double check the state of the buttons
```.ino
void loop() {
  // read the state of the switch into a local variable:
  int reading = digitalRead(buttonPin);

  // check to see if you just pressed the button
  // (i.e. the input went from LOW to HIGH), and you've waited long enough
  // since the last press to ignore any noise:

  // If the switch changed, due to noise or pressing:
  if (reading != lastButtonState) {
    // reset the debouncing timer
    lastDebounceTime = millis();
  }

  if ((millis() - lastDebounceTime) > debounceDelay) {
    // whatever the reading is at, it's been there for longer than the debounce
    // delay, so take it as the actual current state:

    // if the button state has changed:
    if (reading != buttonState) {
      buttonState = reading;

      // only toggle the LED if the new button state is HIGH
      if (buttonState == HIGH) {
        ledState = !ledState;
      }
    }
  }

  // set the LED:
  digitalWrite(ledPin, ledState);

  // save the reading. Next time through the loop, it'll be the lastButtonState:
  lastButtonState = reading;
}
```
### 7. Interruption

   When Arudino running, it will check every line of code in a very small amount of time: 10ms. So if the users want to input by using press button or other devices, the users need to be very fast or just repeat pressing the button until the Arduino check the line that contain the code for input. That is time consuming and inconvinient, it also makes the code run wrongly. We use interuption to solve this problem. Interrupts are useful for making things happen automatically in microcontroller programs and can help solve timing problems.
   
   Syntax:  attachInterrupt(pin, ISR, mode)
      
   pin: the Arduino pin number.
      
   ISR: the ISR to call when the interrupt occurs; this function must take no parameters and return nothing. This function       is sometimes referred to as an interrupt service routine.
      
   mode: defines when the interrupt should be triggered. Four constants are predefined as valid values:

         - LOW to trigger the interrupt whenever the pin is low,

         - CHANGE to trigger the interrupt whenever the pin changes value

         - RISING to trigger when the pin goes from low to high,

         - FALLING for when the pin goes from high to low.
         
```.ino
// Declare
const byte ledPin = 13;
const byte interruptPin = 2;
volatile byte state = LOW;

void setup() {
  pinMode(ledPin, OUTPUT);
  pinMode(interruptPin, INPUT_PULLUP);
  // the program will interrupt the Arduino and run the blink function
  attachInterrupt(digitalPinToInterrupt(interruptPin), blink, CHANGE); 
}

void loop() {
  digitalWrite(ledPin, state);
}

void blink() {
  state = !state;
}

```

### 8. English Input System

①  Add all the letters and digits to the keyboard
```.ino
int index = 0;
String keyboard[]={"A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T", "U", "V", "W", "X", "Y", "Z", " ", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9", " ","SENT", "DEL"};
String text = "";
int numOptions = 40;
```
②  Initialize the library with the numbers of the interface pins
```.ino
LiquidCrystal lcd(12, 11, 5, 4, 9, 8);
```
③ Function changes the letter in the keyboard
  ```.ino
  void changeLetter(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    index++;
      //check for the max row number
    if(index==numOptions){
      index=0; //loop back to first row
    }                                   
 }
}
```
④ Function add the letter to the text or send the message
 ```.ino
 void selected(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    
    String key = keyboard[index];
    if (key == "DEL")
    {
      int len = text.length();
      text.remove(len-1);
    }
    else if(key == "SENT")
    {
      text="";
    }else{
      text += key;
    }
    index = 0; //restart the index
  }
 ```
⑤  Set up the LCD's number of columns and rows. And print message to the LCD
```.ino
void setup() {
  lcd.begin(16, 2);
  attachInterrupt(0, changeLetter, RISING);//button A in port 2
  attachInterrupt(1, selected, RISING);//button B in port 3
}
```
⑥ Run the program in the loop
```.ino
void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print(keyboard[index]);
  lcd.setCursor(0, 1);
  lcd.print(text);
  delay(100);
}
```
### 9. Small development on moving the LCD screen to left and right
 ①　Declare the libraries, number of LCD interface pins, the button pin numbers.
 ```.ino
 // include the library code:
#include <LiquidCrystal.h>

// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 5, 4, 7, 6);

int but1 = 2;
int but2 = 3;
int press1 = 0;
int press2 = 0;
int x =0;
String text = "";

char letter[]={'a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','x','y','z','w','1','2','3','4','5','6','7','8','9','0', ' '};
```
②　Set up the LCD and print the letter to LCD
```.ino
void setup() {
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  
  pinMode(but1, INPUT);
  pinMode(but2, INPUT);
  
  for(int i=0; i < 38; i++){
    lcd.print(letter[i]);
    delay(100);
  }   

}
```
③　Declare function for each button
  ```.ino
 void hpress1(){
    
   long last_interrupt_time = 0;
   long interrupt_time = millis();
   long timepress2 = millis();
   if(interrupt_time - last_interrupt_time > 200) {
     if(digitalRead(but1) == HIGH){
      press1++;
     } if (press1 == 1){
        x--;
        press1 = 0;
        lcd.scrollDisplayLeft();
      
   }
     timepress2 = last_interrupt_time;
 }
 }
  void hpress2(){
    
   long last_interrupt_time1 = 0;
   long interrupt_time1 = millis();
   long timepress1 = millis();
   if(interrupt_time1 - last_interrupt_time1 > 200) {
      if(digitalRead(but2) == HIGH){
      press2++;
     } if (press2 == 1){
        x++;
        press2 = 0;
      lcd.scrollDisplayRight();  
     
     
   last_interrupt_time1=interrupt_time1;
   timepress1 = last_interrupt_time1;  
   }
  }
  }
```
④。Run the interruption
```.ino
void loop() {
  attachInterrupt(0, hpress1, CHANGE);
  attachInterrupt(1, hpress2, CHANGE);
}
```

![](LCDscroll.gif)

**Gif4** This is the LCD scroll

### 10. Convert English to binary ASCII
```.ino

void setup()
{
Serial.begin(9600);
  
String myText = "Tuan";        // Declare the text we want to convert

for(int i=0; i<myText.length(); i++){  // this loop will run through every character of the text

   char myChar = myText.charAt(i);    // This will take out individual letter of the text
 
    for(int i=7; i>=0; i--){           
      byte bytes = bitRead(myChar,i);   // Reads a bit of a number
      Serial.print(bytes, BIN);
    }

    Serial.println("");
}
}
```

### 11. Complete convert E to Binary system and signal.
```.ino
 // include the library code:
#include <LiquidCrystal.h>
int index = 0; 
// add all the letters and digits to the keyboard
String keyboard[]={" ", "SENT", "a", "b", "c", "d", "e", "f", "g", "g", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "1", "2", "3", "4", "5", "6", "7", "8", "9", "0", "DEL"};
String text = "";
int numOptions = 39;
int led1 = 8;
int led2 = 9;
byte bna;
String chch = "";

// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 7, 6, 5, 4);

void setup() {
// Declare the OUTPUT 
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD.
  attachInterrupt(0, changeLetter, RISING);//button A in port 2
  attachInterrupt(1, selected, RISING);//button B in port 3
 
}

void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print(keyboard[index]);
  lcd.setCursor(0, 1);
  lcd.print(text);
  delay(100);
}

//This function changes the letter in the keyboard
void changeLetter(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assume
    index++;
      //check for the max row number
    if(index==numOptions){
      index=0; //loop back to first row
    } 
 }
}

//this function adds the letter to the text or send the msg
void selected(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    
    String key = keyboard[index];
    if (key == "DEL")
    {
      int len = text.length();
      text.remove(len-1);
    }
    else if(key == "SENT")
    {
      EtoB();
      turnOnOff();
      sent();
      turnOnOff();
      text="";
    }else{
      text += key;
    }
    index = 0; //restart the index
  }
}

void EtoB(){     //This function convert English to binary 

for(int i=0; i<text.length(); i++){

   char myChar = text.charAt(i);
 
    for(int i=7; i>=0; i--){
      bna = bitRead(myChar,i);
      Serial.print(bna);
      chch += bna; 
    }
    Serial.print(" ");
}
}

  
void sent(){                // This function will turn the binary numbers to the light signal 
    for(int x=0; x < chch.length(); x++){
      char myChar1 = chch.charAt(x);
      if(myChar1 == '0'){    // If the letter is 0, turn led1 off
        digitalWrite(led1, LOW);
        blink();             // Light 2 blinks
        delay(1000);
      } else if(myChar1 == '1'){   // If the letter is 1, turn led1 on 
        digitalWrite(led1, HIGH);
        blink();
        delay(1000);
      } else {   //If it is the space, turn off both lights
        turnOff();
      }
    }
  }

void blink(){       // THis function will blink the ligh
  digitalWrite(led2, HIGH);
  delay(1000);
  digitalWrite(led2, LOW);
  delay(1000);
}

void turnOnOff(){            // This function will turn the light on and turn it off
 digitalWrite(led1, HIGH);
 digitalWrite(led2, HIGH);
 delay(1000);
 digitalWrite(led1, LOW);
 digitalWrite(led2, LOW);
 delay(1000);
}

void turnOff(){     // This function will turn both 2 lights
 digitalWrite(led1, LOW);
 digitalWrite(led2, LOW);
 delay(1000);
}
 
```
![](EtoBComplete.gif)

**Gif5** This is the convert system from English to binary

###  12. CONVERT BINARY TO ENG
```.ino
// include the library code:
#include <LiquidCrystal.h>
int index = 0; 
// add all the letters and digits to the keyboard
String keyboard[]={"BIN TO ENG","0", "1","", "DEL"};
String text = "";
char letter;
int numOptions = 5;
int led1 = 8;
int led2 = 13;
String text1="";
String text2="";
int z;


// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 7, 6, 5, 4);

void setup() {
  Serial.begin(9600);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD.
  attachInterrupt(0, changeLetter, RISING);//button A in port 2
  attachInterrupt(1, selected, RISING);//button B in port 3
 
}

void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print(keyboard[index]);
  lcd.setCursor(0, 1);
  lcd.print(text);
  delay(100);
}

//This function changes the letter in the keyboard
void changeLetter(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    index++;
      //check for the max row number
    if(index==numOptions){
      index=0; //loop back to first row
    } 
 }
}

//this function adds the letter to the text or send the msg
void selected(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    
    String key = keyboard[index];
    if (key == "DEL")
    {
      int len = text.length();
      text.remove(len-1);
    }
     else if(key == "BIN TO ENG"){
    	bintoeng();
    } else{
      text += key;
    }
    index = 0; //restart the index
  }
}

void bintoeng(){
  for (int y = 0; y < text.length(); y++){
    if(text.charAt(y) != ' '){
      z++;
      text2+=text.charAt(y);
      if(z == 8){
        check();
      	text2="";
        z=0;
      }
    } else {
    	text2+= " ";
    }
  }
 Serial.print(text1); 
}

void check(){
    if (text2 == "01100001") {
           text1=text1+"a";
    } else if (text2 == "01100010") {
           text1=text1+"b";
    } else if (text2 == "01100011") {
           text1=text1+"c";
    } else if (text2 == "01100100") {
           text1=text1+"d";
    } else if (text2 == "01100101") {
           text1=text1+"e";
    } else if (text2 == "01100110") {
           text1=text1+"f";
    } else if (text2 == "01100111") {
           text1=text1+"g";
    } else if (text2 == "01101000") {
           text1=text1+"h";
    } else if (text2 == "01101001") {
           text1=text1+"i";
    } else if (text2 == "01101010") {
           text1=text1+"j";
    } else if (text2 == "01101011") {
           text1=text1+"k";
    } else if (text2 == "01101100") {
           text1=text1+"l";
    } else if (text2 == "01101101") {
           text1=text1+"m";
    } else if (text2 == "01101110") {
           text1=text1+"n";
    } else if (text2 == "01101111") {
           text1=text1+"o";
    } else if (text2 == "01110000") {
           text1=text1+"p";
    } else if (text2 == "01110001") {
           text1=text1+"q";
    } else if (text2 == "01110010") {
           text1=text1+"r";
    } else if (text2 == "01110011") {
           text1=text1+"s";
    } else if (text2 == "01110100") {
           text1=text1+"t";
    } else if (text2 == "01110101") {
           text1=text1+"u";
    } else if (text2 == "01110110") {
           text1=text1+"v";
    } else if (text2 == "01110111") {
           text1=text1+"w";
    } else if (text2 == "01111000") {
           text1=text1+"x";
    } else if (text2 == "01111001") {
           text1=text1+"y";
    } else if (text2 == "01111010") {
           text1=text1+"z";
    } 
}

```
![](bintoeng.gif)

**Gif6** This is the convert system from binary to eng

### 13. Complete convert system
```.ino

// include the library code:
#include <LiquidCrystal.h>
int index = 0; 
// add all the letters and digits to the keyboard
String keyboard[]={" ", "SENT BINARY","SENT MORSE", "MORSE TO BINARY", "1", "2", "3", "4", "5", "6", "7", "8", "9", "0","a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "DEL"};
String keyboardformorse = " abcdefghijklmnopqrstuvwxyz1234567890";
String morse[]={"0","12", "2111", "2121", "211", "1", "1121", "221", "1111", "11", "1222", "212", "1211", "22", "21", "222", "1221", "2212", "121", "111", "2", "112", "1112", "122", "2112", "2122", "2211", "12222", "11222", "11122", "11112", "11111", "21111", "22111", "22211", "22221", "22222"};
String text = "";
char letter;
int numOptions = 39;
int led1 = 8;
int led2 = 13;
int i,j;
byte bna;
String chch = "";
String mess = "";
String mess2 = "";
String mess3= "";

// initialize the library with the numbers of the interface pins
LiquidCrystal lcd(12, 11, 7, 6, 5, 4);

void setup() {
  Serial.begin(9600);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
  // set up the LCD's number of columns and rows:
  lcd.begin(16, 2);
  // Print a message to the LCD.
  attachInterrupt(0, changeLetter, RISING);//button A in port 2
  attachInterrupt(1, selected, RISING);//button B in port 3
 
}

void loop() {
  // set the cursor to column 0, line 1
  // (note: line 1 is the second row, since counting begins with 0):
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print(keyboard[index]);
  lcd.setCursor(0, 1);
  lcd.print(text);
  delay(100);
}

//This function changes the letter in the keyboard
void changeLetter(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    index++;
      //check for the max row number
    if(index==numOptions){
      index=0; //loop back to first row
    } 
 }
}

//this function adds the letter to the text or send the msg
void selected(){
  static unsigned long last_interrupt_time = 0;
  unsigned long interrupt_time = millis();
  if (interrupt_time - last_interrupt_time > 200)
  {
  
    last_interrupt_time = interrupt_time;// If interrupts come faster than 200ms, assum
    
    String key = keyboard[index];
    if (key == "DEL")
    {
      int len = text.length();
      text.remove(len-1);
    }
    else if(key == "SENT BINARY")
    {
      EtoB();
      turnOnOff();
      sentbin();
      turnOnOff();
      text="";
    } else if(key == "SENT MORSE"){
    	sentmorse();
    }
    else if(key== "MORSE TO BINARY"){
      MtoB();
    }
    
    else{
      text += key;
    }
    index = 0; //restart the index
  }
}

void EtoB(){

for(int i=0; i<text.length(); i++){

   char myChar = text.charAt(i);
 
    for(int i=7; i>=0; i--){
      bna = bitRead(myChar,i);
      chch += bna; 
    }
}
}

  
void sentbin(){
    for(int x=0; x < chch.length(); x++){
      char myChar1 = chch.charAt(x);
      if(myChar1 == '0'){
        digitalWrite(led1, LOW);
        blink();
        delay(500);
      } else if(myChar1 == '1'){
        digitalWrite(led1, HIGH);
        blink();
        delay(500);
      } else {
        turnOff();
      }
    }
  }

void blink(){
  digitalWrite(led2, HIGH);
  delay(500);
  digitalWrite(led2, LOW);
  delay(500);
}

void turnOnOff(){
 digitalWrite(led1, HIGH);
 digitalWrite(led2, HIGH);
 delay(500);
 digitalWrite(led1, LOW);
 digitalWrite(led2, LOW);
 delay(500);
}

void turnOff(){
 digitalWrite(led1, LOW);
 digitalWrite(led2, LOW);
 delay(500);
}

// Morse
void sentmorse(){
      for(i=0; i<text.length(); i++) {
        for(j=0; j<37; j++) {
          if(text[i]==keyboardformorse[j]){
            mess+=morse[j];
            break;
          }
        }
         
        mess+="3";
      }
       for(i=0; i<7; i++) {
        blinkLight(300, 300);
      }
      for(i=0; i<mess.length(); i++) {
        switch (mess[i]) {
          case '0':
          delay(3000);
          break;
          
          case '1':
          blinkLight(1000, 1000);
          break;
          
          case '2':
          blinkLight(3000, 1000);
          break;
          
          case '3':
          delay(1000);
          break;
        }
      }
      
      for(i=0; i<7; i++) {
        blinkLight(300, 300);
      }
          
      text="";
    }
  void MtoB() {
    for(i=0; i<text.length(); i++) {
      if((text[i+1]=='3') || ((i+1)==text.length())||(text[i+1]=='0')){
        mess2+=text[i];
        for(j=0; j<37; j++) {
          if(morse[j]==mess2) {
            mess3+=keyboardformorse[j];
            break;
          }
        }
        mess2="";
        if (text[i+1]=='0'){
          mess3+=' ';
        }
          i+=1; 
        
        }
      else {
      	mess2+=text[i];
      }
      
    } 
  text=mess3;
  Serial.print(text);
  EtoB();
  turnOnOff();
  sentbin();
  turnOnOff();
  text="";
  mess3="";
  }
    
    void blinkLight(int on, int off) {
      digitalWrite(led1, HIGH);
      delay(on);
      digitalWrite(led1, LOW);
      delay(off);
      
    }
```
![](sentmorse.gif)

**Gif7** This is the convert system from English to morse

![](morsetobinary.gif)

**Gif8** This is the convert system from morse to binary

Evaluation
---------
#### Success Criteria 

The success criteria as detailed in the planning section of this document have all been met.

|CRITERIA|MET|
|:---|:---:|
|The keyboard with 2 buttons allows users to input choosing the options and letters|MET|
|The transmitter can transmit the information correctly from english to binary, from binary to morse and vice versa.|MET|
|User can choose and delete the letters|MET|
|The bulb light is used effeciently in the communication, there is no issue for the bulblight like broken or too old|MET|
|The bulb light need to represent correctly when turn on or off as for the information|MET|
|An LCD screen shows the available letter options and the letter users choose|MET|
|Function choosing between transmit english to binary or morse|MET|
|Function convert from binary to english, morse to english|MET|
|Options for users to send the message to the light bulbs|MET|
|A manual scripts for helping user|MET|
|The system is simple and cheap|MET|

**Fig 13** This table shows how the convert system fulfills the success criteria at the planning section

Videos given above are the evidence for the success of function converting, transmitting data and also the materials used are met the criteria: lightbulbs, LCD screen. The user can choose and delete the letters and they can check how to use the program more effectively with the manual.

#### Improvement
 
 While this convert system works well with many useful function, it still has some limitations that need to improve in the future.
 
 - The organization of the options can be improved by grouping options so the user can easily choose wanted options
 - The program can be visualized on touched screen, it is more convinient when no need the press buttons, and too many connected wires
 - The program can record the history user user the program, and can delete or backup it when needed.
 - The program can sort 10 most used words, so the user can choose it faster
 - There is receiver system that can receive the signal and automatically store information into aduino so that the users don't need to take note and type it in the arduino
 
Reference
----------
[1] "Usability" retrived from https://en.wikipedia.org/wiki/Usability (25 Nov 2019)

[2] "Human-centered design" retrived from https://en.wikipedia.org/wiki/Human-centered_design (25 Nov 2019)

[3] "Logic gate" retrived from https://whatis.techtarget.com/definition/logic-gate-AND-OR-XOR-NOT-NAND-NOR-and-XNOR

[4] "Debounce button" retrived from https://www.arduino.cc/en/tutorial/debounce (1 Dec 2019)

[5] "Machine cycle" retrived from https://www.techopedia.com/definition/8180/machine-cycle (21 Jan 2020)



