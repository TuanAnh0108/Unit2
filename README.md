![SystemDiagram](facebook_cover_photo_2.png) 
 
 
 # TRANSMITTER LANGUAGE 
                                   

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
   7. There will be options for users to choose between transmit to binary or morse
   
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


### Usability 

Usability is according to Wikipedia[1] the degree of wase with which a product can be used to achieve their goals. It studies the elegance, clarity, intuitive with which the computer program. 

### Human-centered design HCD

Human-centerd design HCD according to Wikipedia[2] is an approach to problem solving, commonly used in design and management frameworks that develops solutions to problems by involving the human perspective in all steps of the problem-solving process. Human involvement typically takes place in observing the problem within context, brainstorming, conceptualizing, developing, and implementing the solution.

### Compare Bash and Arduino programing languge
① Advantages of bash and arduino

   | Bash | Arduino |
   | :--- | :--- |
   |Easy to learn and use| Compatible with many different platform |
   |Powerful, doing tasks in computer like: deleting, adding, creating files,... with just typing| Various type of data |
   |Can see the output immediately after finishing coding in the same app where writing code| Well suited with the large and complex task|
   |The command and syntax are exactly the same as those directly entered in command line, so programmer do not need to switch to entirely different syntax| Fast, effecient language|
   |Much quicker when writing code with bash| It is very easy to understand, it uses keywords like: if, switch, void,.. |
   |Customizing administrative tasks| You can easily find the error |
   |Quick start, and interactive debugging| |
   |No need to declare the type of data| |
   |No need to use ; to end a statement| |
   |No need to close a comment||

② Disadvantages of bash and arduino

   | Bash | Arduino |
   | :--- | :--- |
   |Prone to costly errors, a single mistake can change the command which might be harmful| Cannot do administrator tasks|
   |Slow execution speed| Need to declare the type of data|
   |Not well suited with the large and complex task| Need to close a comment|
   |Provide minimal data structure unlike other scripting languages| Need to ; to end a statement|
   |Limited data types| |
   |Compatibility problems between different platforms| |

③ Comparison of bash and arduino
   
   | Bash | Arduino |
   | :--- | :--- |
   | In bash, the for loop use curly braces for the statement that need to repeat. There are 3 parameters in the curly braces: initialization, condition and increment. You do not need to declare the data type of variable that you will use in your code. Moreover, you have to use do when opening a statement, done when closing the statement for the for loop. Next, at the end of the statement we do not need to use ";" to end the statement. When using a variable, you need to use "$" before the name of the variable. Then, to make a comment, you just use "#" to open a comment line. We use "echo" to print String or variable. Then, bash is a powerful programming language, it can do the administrator task| In Arduino,like bash we use curly braces for the statement that need to repeat. Also it has the same 3 parameters as in bash. You have to declare all the variable that you use in your program or it will cause errors. Next, the for loop just need to have open and close brackets for the statement. ";" is the compulsory thing in Arduino code, we have to use it to end the statement or it will cause errors. In the contrast of bash, arduino code does not require "$" when using variable. When making a comment, you need to open and close (using /* )the comment. We use "print" to print the string or variables. Arduino programming language cannot execute the administrator task like adding, deleting,.. files, folders.  |
   
   ### Interruption on Arduino
   When Arudino running, it will check every line of code in a very small amount of time: 10ms. So if the users want to input by using press button or other devices, the users need to be very fast or just repeat pressing the button until the Arduino check the line that contain the code for input. That is time consuming and inconvinient, it also makes the code run wrongly. We use interuption to solve this problem. Interrupts are useful for making things happen automatically in microcontroller programs and can help solve timing problems.
   
   Syntax:  attachInterrupt(pin, ISR, mode)
      
   pin: the Arduino pin number.
      
   ISR: the ISR to call when the interrupt occurs; this function must take no parameters and return nothing. This function       is sometimes referred to as an interrupt service routine.
      
   mode: defines when the interrupt should be triggered. Four constants are predefined as valid values:

         - LOW to trigger the interrupt whenever the pin is low,

         - CHANGE to trigger the interrupt whenever the pin changes value

         - RISING to trigger when the pin goes from low to high,

         - FALLING for when the pin goes from high to low.
   ### Debouncing button
   Pushbuttons often generate spurious open/close transitions when pressed, due to mechanical and physical issues: these transitions may be read as multiple presses in a very short time fooling the program. Debounce means checking the input twice in a short period of time to make sure the pushbutton is definitely pressed. Without debouncing, pressing the button once may cause unpredictable results.[3]

Development
------------
### 1. Traffic light

①　Declare the port number of each LED light and set the LED light as OUPUT
   ```.ino       
      int red = 10;
      int yellow = 9;
      int green = 8;
      
      void setup(){
      pinMode(red, OUTPUT);
      pinMode(yellow, OUTPUT);
      pinMode(green, OUTPUT);
      }
  ``` 
![](TrafficLight.gif)

**Gif1** This is the result after making the arduino for the traffic light

② Declare function changeLight(){}

      void changeLights(){}
      
③　Write code for the traffic light inside the changeLight function
```.ino
    # Turn the green ligh off, the yellow light turns on 
       digitalWrite(green, LOW);
       digitalWrite(yellow, HIGH);
       delay(3000);
       
    # Turn off the yellow light, then turn on the red light
      digitalWrite(yellow, LOW);
      digitalWrite(red, HIGH);
      delay(5000);

    # Turn on the red and yellow light
      digitalWrite(yellow, HIGH);
      delay(2000);
    
    #  Turn off the red and yellow light, turn on the green light     
      digitalWrite(yellow, LOW);
      digitalWrite(red, LOW);
      digitalWrite(green, HIGH);
      delay(3000);
 ```
 ④　Execute the function changeLight inside the void loop() {}
 ```.ino
      void loop(){
      changeLights();
      delay(15000);
     }  
 ```  
### 2. The blink LED
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
### 3. The counter from 1 to 15 binary number
 ```.ino
          void setup()
          {
           pinMode(A, OUTPUT);
           pinMode(B, OUTPUT);
          pinMode(C, OUTPUT);
          pinMode(D, OUTPUT);
          }

          void loop()
          {
          for (i = 0; i <= 15; i += 1)
          {
          if (i%2 == 1)
          {
          digitalWrite (D, HIGH);
          } 
          if (i%4 > 1)
          {
          digitalWrite (C, HIGH);
          }
          if (i%8 > 3) 
          {
          digitalWrite (B, HIGH);
          }
          if (i%16 > 7)
          {
          digitalWrite (A, HIGH);
          }
          delay (300);
          digitalWrite (D, LOW);
          digitalWrite (C, LOW);
          digitalWrite (B, LOW);
          digitalWrite (A, LOW);
    
          }
          }  
 ```
 ![](CounterBinary.gif)
 
 **Gif2** This is the counter Binary number from 1 to 15 

### 4. The number segements
①　 Declare all the Led and button pin
```.ino
          int LEDA = 1;
          int LEDB = 2;
          int LEDC = 3;
          int LEDD = 4;
          int LEDE = 5;
          int LEDF = 6;       
          int LEDG = 7;
          int butA = 10;
          int butB = 11;
          int butC = 12;
```
②　Declare the input and output
```.ino
　　　　　void setup()
       {
          pinMode(LEDA, OUTPUT);
          pinMode(LEDB, OUTPUT);
          pinMode(LEDC, OUTPUT);
          pinMode(LEDD, OUTPUT);
          pinMode(LEDE, OUTPUT);
          pinMode(LEDF, OUTPUT);
          pinMode(LEDG, OUTPUT);
          pinMode(butA, INPUT);
          pinMode(butB, INPUT);
          pinMode(butC, INPUT);
  
        }
```
③　Logic gate equation for each LED
```.ino
       void loop()
         {
          bool A = digitalRead(butA);
          bool B = digitalRead(butB);
          bool C = digitalRead(butC);
          bool a = (!C & !A) | (B & !A) | (!C & A) | (A & !B);
          bool b = (!C & A) | (!B & !A) | (A & !B);
          bool c = (!A & !C) | (!A & !B) | (!C & B);
          bool d = (!A & !C) | (!A & B) | (B & !C) | (C & A & !B);
          bool e = A | (!C & !B) | (C & B);
          bool f = (!A & B) | (!C & !A) | (!C & !B);
          bool g = (!A & B) | (B & !C) | (A & !B);
          digitalWrite(LEDA, a);
          digitalWrite(LEDB, b);
          digitalWrite(LEDC, c);
          digitalWrite(LEDD, d);
          digitalWrite(LEDE, e);
          digitalWrite(LEDF, f);
          digitalWrite(LEDG, g);
                    
       }
   ```
![](NumberSegment.gif)

**Gif3** This is the Number Segment with 7 LEDs (it can show us number from 0 to 7)

### 5. Debouncing button

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
### 6. Debounce button
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

### 7. English Input System

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
### 8. Small development on moving the LCD screen to left and right
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


Evaluation
---------





Reference
----------
[1] "Usability" retrived from https://en.wikipedia.org/wiki/Usability (25 Nov 2019)

[2] "Human-centered design" retrived from https://en.wikipedia.org/wiki/Human-centered_design (25 Nov 2019)

[3] "Debounce button" retrived from https://www.arduino.cc/en/tutorial/debounce (1 Dec 2019)

