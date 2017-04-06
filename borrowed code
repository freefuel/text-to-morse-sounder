 /*

Morse Code Project

This code will loop through a string of characters and convert these to morse code.

It will blink two LED lights and play audio on a speaker.

*/

//***********************************************************************************//

// SENDING YOUR TEXT BELOW USING SPACE FOR EACH CHARACTER IN string To Morse Code //

//***********************************************************************************//


char stringToMorseCode[] = "paris";

// Create variable to define the output pins

int led13 = 13; // blink an led on output 13

int led1 = 1; // blink an led on output 1

int audio8 = 8; // output audio on pin 8

int note = 700; // music note/pitch  //a means of changing this after compile time is desirable

/*

Set the speed of your morse code

Adjust the 'dotlen' length to speed up or slow down your morse code

(all of the other lengths are based on the dotlen)

Here are the ratios code elements:

Dash length = Dot length x 3

Pause between elements = Dot length

(pause between dots and dashes within the character)

Pause between characters = Dot length x 3

Pause between words = Dot length x 7

http://www.nu-ware.com/NuCode%20Help/index.html?m...

*/

int dotLen = 50; // length of the morse code 'dot' "13 words-per-minute is one element every 92.31 milliseconds." final revision goal is to have sending speed based on the size of the charater buffer with larger messages sent faster. 

int dashLen = dotLen * 3; // length of the morse code 'dash'

int elemPause = dotLen; // length of the pause between elements of a character

int Spaces = dotLen * 3; // length of the spaces between characters // dynamic adjustment of this setting for the farnsworth method is needed.

int wordPause = dotLen * 7; // length of the pause between words  // dynamic adjustment of this setting for the farnsworth method is needed.

// the setup routine runs once when you press reset:

void setup() {

// initialize the digital pin as an output for LED lights.

Serial.begin(9600); 

pinMode(led13, OUTPUT);  //this is nice but not critical

pinMode(led1, OUTPUT); //this seems redundant remove at some point. 

}

// Create a loop of the letters/words you want to output in morse code (defined in string at top of code)

void loop()

{
if (Serial.available() > 0) {  //serial buffer size needs to be increased to 512 bytes to conform with IRC RFC spec for maximum message size. 

char i = Serial.read();

char tmpChar = i;

tmpChar = toLowerCase(tmpChar);

GetChar(tmpChar);

}

// At the end of the string long pause before looping and starting again

LightsOff(300);   //look to eliminate this delay time

}

// DOT

void MorseDot()

{

digitalWrite(led13, HIGH); // turn the LED on

digitalWrite(led1, HIGH);

tone(audio8, note, dotLen); // start playing a tone

delay(dotLen); // hold in this position

}

// DASH

void MorseDash()

{

digitalWrite(led13, HIGH); // turn the LED on

//digitalWrite(led1, HIGH);

tone(audio8, note, dashLen); // start playing a tone

delay(dashLen); // hold in this position

}

// Turn Off

void LightsOff(int delayTime)

{

digitalWrite(led13, LOW); // turn the LED off

//digitalWrite(led1, LOW);

noTone(audio8); // stop playing a tone

delay(delayTime); // hold in this position

}

// *** Characters to Morse Code Conversion *** //

void GetChar(char tmpChar)

{

// Take the passed character and use a switch case to find the morse code for that character

switch (tmpChar) {

case 'a':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'b':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'c':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'd':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'e':

MorseDot();

LightsOff(elemPause);

break;

case 'f':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'g':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'h':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'i':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'j':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'k':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'l':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'm':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'n':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'o':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'p':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 'q':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'r':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 's':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case 't':

MorseDash();

LightsOff(elemPause);

break;

case 'u':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'v':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'w':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'x':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'y':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case 'z':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '0':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '1':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '2':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '3':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '4':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '5':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '6':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '7':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '8':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '9':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '.':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case ',':

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '?':

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '!':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '/':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '=':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '+':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '-':

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

break;

case '&':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

case '@':

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

MorseDash();

LightsOff(elemPause);

MorseDot();

LightsOff(elemPause);

break;

default:

// If a matching character was not found it will default to a blank space

LightsOff(Spaces);

}

}

/*

Unlicensed Software:

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or

distribute this software, either in source code form or as a compiled

binary, for any purpose, commercial or non-commercial, and by any

means.

In jurisdictions that recognize copyright laws, the author or authors

of this software dedicate any and all copyright interest in the

software to the public domain. We make this dedication for the benefit

of the public at large and to the detriment of our heirs and

successors. We intend this dedication to be an overt act of

relinquishment in perpetuity of all present and future rights to this

software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,

EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF

MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR

OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,

ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR

OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to

*/
