# ForwardJS Workshop 

## Downloads
- [Node.js](https://nodejs.org/en/)

- [Putty] (http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html)  For Windows 

- [CoolTerm](http://freeware.the-meiers.org/CoolTerm_Mac.zip) for Mac

- [Visual Studio Code](https://code.visualstudio.com/)


## Examples 
Some of the examples use APIS. You might want to register with:
- [Project Oxford API](https://www.projectoxford.ai/)
- [Twitter](https://dev.twitter.com)
- Email - might need to grab an app key from gmail for example 


## Demos 
### Frameworks 
[Johnny-Five](http://johnny-five.io/)
[Example Folder](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/johnnyfive)

Basic example of running Johnny Five with Arduino. Press a button to light an LED. Requires that you load Standard Firmata on the Arduino, wire up a button to Pin 2, and an LED to 13. You need to install the module:
    npm install johnny-five

[Cylon.js](https://cylonjs.com/)
[Example Folder](https://github.com/bitchwhocodes/forwardjs/blob/master/demos/cylon/app.js)

Basic example of running Cylon.js with Arduino. Press a button to light an LED. Requires that you load Standard Firmata on the Arduino, wire up a button to Pin 2, and an LED to 13. You need to install the module:
    npm install cylon
 
### Module    
[SerialPort](https://github.com/voodootikigod/node-serialport)
[Example Folder](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/serialport)

Basic example of capturing serial information with Arduino using the SerialPort module. Press a button to light an LED. Requires that you load the [sketch](https://github.com/bitchwhocodes/forwardjs/blob/master/demos/serialport/arduino/button/button.ino) on the Arduino, wire up a button to Pin 2, and an LED to 13. You need to install the module:
    npm install serialport
    
Then when you call the script you need to pass in the port. On a MAC you can find what port your Arduino or device is using by doing either:
    ls /dev/tty.* 
    ls /dev/cu.*
On a PC, you need to go to your Device Manager, open the COM ports and see which one it is ( for example, COM6).

When you call the script you then go:
    node app.js COM6 
    
### Examples
[Button To Email ](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/button-to-email)
[Example Folder](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/button-to-email)

This example will email a specified email address when you click a button. This requires you to do the following:
- Load the [Sketch](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/button-to-email/button_press) on the Arduino 
-  Wire up the Sketch 
- ![Sketch](https://camo.githubusercontent.com/0e93e3b710acc56eb6ed9c9181b182d7f7bf25a0/68747470733a2f2f7777772e61726475696e6f2e63632f656e2f75706c6f6164732f5475746f7269616c2f627574746f6e2e706e67)
- Set your Email and password in process.env.EMAIL and process.env.PASSWORD in the app.js
- Retrieve your port for your device as mentioned above
- pass the port in when you call the script 
-       node app.js COM6

[Button To Twitter ](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/button-to-twitter)
[Example Folder](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/button-to-twitter)

This example will tweet to your account when you click a button. This requires you to do the following:
- Load the [Sketch](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/button-to-email/button_press) on the Arduino 
-  Wire up the Sketch 
- ![Sketch](https://camo.githubusercontent.com/0e93e3b710acc56eb6ed9c9181b182d7f7bf25a0/68747470733a2f2f7777772e61726475696e6f2e63632f656e2f75706c6f6164732f5475746f7269616c2f627574746f6e2e706e67)
- Go to [Twitter Apps](https://apps.twitter.com/), register an app and get your Consumer Key, Secret, Account Token, Token Key. 
- Put those values in the app.js 
- Retrieve your port for your device as mentioned above
- pass the port in when you call the script 
-       node app.js COM6
     
[Web Cam Project Oxford ](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/project-oxford-webcam)
[Example Folder](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/project-oxford-webcam)

This example is an Express application that will capture an image from your web cam, save it to the server, then send it to the Project Oxford API and depending on how "happy" the image was, it will turn the onboard LED of a Photon , on or off. 
- Load the [Sketch](https://github.com/bitchwhocodes/forwardjs/tree/master/demos/project-oxford-webcam/spark) on the Particle Photon via the Web IDE
- Go to [Project Oxford](https://www.projectoxford.ai/emotion), register for a key. 
- Put those values in the [routes/image.js](https://github.com/bitchwhocodes/forwardjs/blob/master/demos/project-oxford-webcam/routes/image.js) file - replace process.env.PO_KEY  
- Install the modules needed
-     npm install node-oxford-emotion, npm install spark, npm install express
- run the Express application 
-   npm start
- Visit http://localhost:3000


Note: If you publish this to the web, you need to provide HTTPS for this to work in all browsers due to security imposed for user media.

* Particle Weather Shield :Reading the Serial *
- Flash the Particle with the Sparkfun Weathershield Library from the Web IDE by going to libraries > search and search for the library. 
- Discover which port your device is using via the previous instructions
- Open up CoolTerm or Putting and start a serial connection. Make sure the baud rate is 9600 and you have the correct port. When it starts, click into the window. 
- Watch the output from the shield. 


* Particle Weather Shield :Reading with SerialPort *
- Flash the Particle with the Sparkfun Weathershield Library from the Web IDE by going to libraries > search and search for the library. 
- Discover which port your device is using via the previous instructions
- Install the [SerialPort module](https://github.com/voodootikigod/node-serialport)
-     npm install serialport
- Create a script using this [Serial Port Example](https://github.com/bitchwhocodes/forwardjs/blob/master/demos/serialport/app.js)
- Run the script by passing in the port number
-     node app.js COM6

### Extensions
- Take data from the shield and using Socket IO, update the client side
- Take data from the shield and save it to a database or storage 



    







