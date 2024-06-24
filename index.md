


# Ball Tracking Robot

<!--Replace this text with a brief description (2-3 sentences) of your project. This description should draw the reader in and make them interested in what you've built. You can include what the biggest challenges, takeaways, and triumphs from completing the project were. As you complete your portfolio, remember your audience is less familiar than you are with all that your project entails!

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:

-->



| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Eric T | Valley Christian High School | Computer Engineering | Incoming Sophomore




<img src="Eric_T (1).JPG" alt="Headshot" width="450" height="600">

<!--
 
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your final milestone, explain the outcome of your project. Key details to include are:
- What you've accomplished since your previous milestone
- What your biggest challenges and triumphs were at BSE
- A summary of key topics you learned about
- What you hope to learn in the future after everything you've learned at BSE



# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For your second milestone, explain what you've worked on since your previous milestone. You can highlight:
- Technical details of what you've accomplished and how they contribute to the final goal
- What has been surprising about the project so far
- Previous challenges you faced that you overcame
- What needs to be completed before your final milestone 
-->
# First Milestone



<iframe width="560" height="315" src="https://www.youtube.com/embed/jH4JYiuLHz4?si=nz9Xh8DGZ9DOImPa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<h2>
 Summary
</h2>
The final step for my project is to enable the robot to detect the red ball and move towards the ball. For my first milestone, I completed the hardware side of my project. I built my motors and wheels, install my raspberry pi and connected it to all my components, and built my camera and sensors. Also, I programmed test code for my motor, sensors, and camera, allowing for all the main components to have a basic use. 

<h3>
 Components
</h3>

<ul>
<li>Raspberry Pi Computer: This is the brain of the robot/car. It processes code and tells the robot what to do. It has a 40 pin pinout, heat sinks, a USBC input, 2 mini HDMIs, 4 USB inputs, and an HDMI input <br></li>
<li>Motor Driver: It powers the motors. The L298N can control the speed and direction of the motors through the code written in the Raspberry Pi computer. It is connected to the motors and to the Raspberry Pi Computer <br></li>
<li>DC Motors: DC motors run from converting electrical energy to mechanical energy <br></li>
<li>Battery Pack 1: Powers the Raspberry Pi <br></li>
<li>Battery Pack 2: Powers the L298N motor driver <br></li>
<li>Camera: It tracks the ball. Once the ball is on the camera, it creates a rectangle around the ball so it is easier to track<br></li>
<li>Ultrasonic sensors: They tell the distance that the object is from the sensor. The sensor releases an ultrasonic wave that bounces off the object and back, and we can calculate the distance by using the amount of time the wave takes to come back.<br></li>
<li>Breadboard: Used to connect different parts of my robot together. Used to create circuits<br></li>
</ul>

<h4>
 Challenges Faced
</h4>

Overall, my first milestone wasn't complicated by still came with some problems. First, when programming my test code for all my components, my SD card stopped working, causing me to have to replace it and redownload Raspberry Pi. Also, since there were many hardware parts to put together, it took some frustration and time since the wires disconnected many times becauses of its looseness. Lastly, I ran into problems and errors in the code since the tutorial was outdated. I had to do my own research and programming for the test code, which took time to do.


# Arduino Starter Project



<iframe width="560" height="315" src="https://www.youtube.com/embed/5sS4r5BRks8?si=SgCfxLQdLVn6RgoO" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<h2>
 Summary
</h2>
For my starter project, I chose the arduino starter project, which allows for an imput and an output. When building my configurations, I chose the button input, allowing me to press the button and outputting the LEDs that I chose. There were 2 lights in my modification, one that turned on when button was pressed, and the other turned on when the button wasnt pressed. For my code, I intialized all the variables and made an if statement allowing for my output to return correctly. For my circuit, the 5V and GND were providing power to my board, connecting to all the components giving power to the button and LEDs. Through wires and resistors, I was able to connect my button to my LEDs, allowing them to both interact.

<h3>
Components
</h3>

<ul>
 <li>Arduino: Microcontroller; the main component of my project <br></li>
 <li>Resistors: Part used to resist the flow of energy between different objects<br></li>
 <li>LEDs: An output and modification, turns off and on <br></li>
 <li>Jumper wires: Connects electricity between different parts<br></li>
 <li>Button: My input used for modification between my LEDs</li>
 <li>Proto shield: Goes on top and soldered to the arduino, used to combine soldered components to arduino</li>
</ul>


<h4>
 Challenges Faced
</h4>
Although my project ran smoothly and responsive in the end, I ran into many challenges along the way causing may setbacks. First, my soldering iron was very weak, making it hard to solder and eventually causing many short circuits, so i had to rebuild my whole proto shield. Also, some components didn't work when constructing, so it took time troubleshooting. Lastly, building the circuit in the beginning was pretty challenging considering the amount of space on the proto shield. Initially, with the breadboard, I could place all the components wherever I wanted since they were all connected, but when It came to soldering it onto the shield, I had to make adjustments to my placement causing me to challenge my technical skills 

<h1>
 Ball Tracking Robot Test Codes
</h1>

<h2>
Basic Camera Test Code
</h2>

Useful when beginning with this project, being one of the simplest ways to experiment with live video capture with OpenCV’s cv2.VideoCapture() function.
<pre><code>
from picamera2 import Picamera2, Preview
picam2 = Picamera2()
camera_config = picam2.create_preview_configuration()
picam2.configure(camera_config)
picam2.start_preview(Preview.QTGL)
picam2.start()
time.sleep(2)
picam2.capture_file("test.jpg")
</code></pre>

<h2>
Basic Ultrasonic Senor Test Code
</h2>

This code is a very simple way to start understanding ultrasonic sensor calculations to convert garbage sensor values to ones that are crucial to the movement of the robot relative to these values. This simple code will print the distance at which the closest detected object lays.
<pre><code>
import RPi.GPIO as GPIO
import time
GPIO.setmode(GPIO.BCM)

TRIG = 19
ECHO = 26

while True:
    GPIO.setup(TRIG, GPIO.OUT)
    GPIO.setup(ECHO, GPIO.IN)
    GPIO.output(TRIG,False)
   
    time.sleep(0.2)
    GPIO.output(TRIG,True)
   
    time.sleep(0.00001)
    GPIO.output(TRIG,False)
   
    while GPIO.input(ECHO) == 0:
        pulse_start = time.time()
    while GPIO.input(ECHO) == 1:
        pulse_end = time.time()
       
    pulse_duration = pulse_end - pulse_start
   
    distance = pulse_duration * 17150
    distance = round(distance,2)
   
    print ('distance',distance,'cm')
</code></pre>

<h2>
Basic Motor Test Code
</h2>

This code uses basic WASD controls to move your robot, similar to controlling a video game character. It is extremely useful for testing basic mechanical function of DC motors, as well as working through the logical aspect of new vehicle control implementations.
<pre><code>
import RPi.GPIO as GPIO
        import cv2
        import numpy as np
        
        GPIO.setmode(GPIO.BCM)
        
        MOTOR1B=6 # LEFT motor
        MOTOR1E=5
        
        MOTOR2B=22 # RIGHT motor
        MOTOR2E=23 
        
        GPIO.setup(MOTOR1B, GPIO.OUT)
        GPIO.setup(MOTOR1E, GPIO.OUT)
        
        GPIO.setup(MOTOR2B, GPIO.OUT)
        GPIO.setup(MOTOR2E, GPIO.OUT)
        
        while(True):
            userInput = input()
            
            if(userInput == 'w'):
                GPIO.output(MOTOR1B,GPIO.HIGH)
                GPIO.output(MOTOR1E,GPIO.LOW)
                GPIO.output(MOTOR2B,GPIO.HIGH)
                GPIO.output(MOTOR2E,GPIO.LOW)
            
            if(userInput == 'a'):
                GPIO.output(MOTOR1B,GPIO.LOW)
                GPIO.output(MOTOR1E,GPIO.LOW)
                GPIO.output(MOTOR2B,GPIO.HIGH)
                GPIO.output(MOTOR2E,GPIO.LOW)
                
            if(userInput == 's'):
                GPIO.output(MOTOR1B,GPIO.LOW)
                GPIO.output(MOTOR1E,GPIO.HIGH)
                GPIO.output(MOTOR2B,GPIO.LOW)
                GPIO.output(MOTOR2E,GPIO.HIGH)
            
            if(userInput == 'd'):
                GPIO.output(MOTOR1B,GPIO.HIGH)
                GPIO.output(MOTOR1E,GPIO.LOW)
                GPIO.output(MOTOR2B,GPIO.LOW)
                GPIO.output(MOTOR2E,GPIO.LOW)
        
            if(userInput == 'x'):
                 GPIO.output(MOTOR1B,GPIO.LOW)
                 GPIO.output(MOTOR1E,GPIO.LOW)
                 GPIO.output(MOTOR2B,GPIO.LOW)
                 GPIO.output(MOTOR2E,GPIO.LOW)
</code></pre>

<!--

# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```


-->

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Raspberri Pi 4 Model B | Brains of robot | $61.75 | <a href="https://www.amazon.com/Raspberry-Model-2019-Quad-Bluetooth/dp/B07TC2BK1X?source=ps-sl-shoppingads-lpcontext&ref_=fplfs&smid=A2QE71HEBJRNZE&th=1"> Link </a> |
| Raspberry Pi Camera Module | Used for input to see ball | $14.99 | <a href="https://www.amazon.com/Arducam-Autofocus-Raspberry-Motorized-Software/dp/B07SN8GYGD/ref=sr_1_5?crid=3236VFT39VAPQ&keywords=picamera&qid=1689698732&s=electronics&sprefix=picamer%2Celectronics%2C138&sr=1-5"> Link </a> |
| L298N Driver Board | Used to move the robot | $8.99 | <a href="https://www.amazon.com/Qunqi-2Packs-Controller-Stepper-Arduino/dp/B01M29YK5U/ref=sr_1_1_sspa?crid=3DE9ZH0NI3KJX&keywords=l298n&qid=1689698859&s=electronics&sprefix=l298n%2Celectronics%2C164&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1"> Link </a> |
| Motors and Board kit | The physical build of robot | $12.99 | <a href="https://www.amazon.com/Smart-Chassis-Motors-Encoder-Battery/dp/B01LXY7CM3/ref=sr_1_4crid=27ACD61NPNLO4&keywords=robot+car+kit&qid=1689698962&s=electronics&sprefix=robot+car+kit%2Celectronics%2C169&sr=1-4"> Link </a> |
| Powerbank | Power the robot | $21.99 | <a href="https://www.amazon.com/Anker-Ultra-Compact-High-Speed-VoltageBoost-Technology/dp/B07QXV6N1B/ref=sr_1_1_sspa?crid=53ULGW8ZNDOW&keywords=power%2Bbank&qid=1689699045&s=electronics&sprefix=power%2Bbank%2Celectronics%2C144&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1"> Link </a> |
| HC-SR04 sensors (5 pcs) | Used for to detect | $8.99 | <a href="https://www.amazon.com/Organizer-Ultrasonic-Distance-MEGA2560-ElecRight/dp/B07RGB4W8V/ref=sr_1_2?crid=UYI359LWAAVU&keywords=hc%2Bsr04%2Bultrasonic%2Bsensor%2B3%2Bpc&qid=1689699122&s=electronics&sprefix=hc%2Bsr04%2Bultrasonic%2Bsensor%2B3%2Bpc%2Celectronics%2C123&sr=1-2&th=1"> Link </a> |



<!--

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Example 1](https://trashytuber.github.io/YimingJiaBlueStamp/)
- [Example 2](https://sviatil0.github.io/Sviatoslav_BSE/)
- [Example 3](https://arneshkumar.github.io/arneshbluestamp/)

To watch the BSE tutorial on how to create a portfolio, click here.


-->
