# Automatic Street Lighting
The automatic street lighting is exactly what it sounds like, the light automaticaly turns on. It works by a photoresitor measuring the amount of light and if it reads below a certain level of light, the LED turns on. This goes along with a 3D printed miniture street lamp, so that I can simulate a real street lamp. I had a lot of new experiences such as soldering and 3D modeling, and had some struggles also, but suceeded in the end.

<!---You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions: -->
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Mattias S | Menlo Atherton High School | Electrical Engineering | Incoming Sophomore 

<!--**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**-->

![Headstone Image](<image0.jpeg>)
  
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

# First Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/vW7si-DyvSE?si=sfyi6aW6T5j7iX8Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

The project that I am working on is called the automatic street light. This project consists of a photoresistor(LDR) to detect the amounts of light around the sensor, and an LED. When the LDR detects high levels of light, the LED remains turned off to not waste energy, and when it detects low light in the surrounding areas the LED automaticaly turns on so that you would be able to see if it was night, or just very dark. So far, I have finished the base model of my project along with adding a second sensor for a second LED. The challenges that I faced mostly rose from that I have never used a arduino or breadboard before, and I came in to this project having very little experience with coding. However, throughout the course of my milestones i'll definitely overcome those challenges with experience. I am planning to complete my project by 3D printing a small version of a lamp post to make the project look like a final product and complete.

# Schematics 
<img width="1257" height="527" alt="image" src="https://github.com/user-attachments/assets/c873f6c4-9581-4a6f-b266-85af9dd34646" />


# Code
<!---Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. -->

'''

const   int ledpin = 13; // ledpin and lightpin are not changed throughout the process
const   int lightpin = A2;
const   int ledpin2 = 12;
const   int lightpin2 = A1;
const int LIGHT = 75;
const int LIGHT2 = 650; // sets LIGHT value for light sensor
void   setup() {
  Serial.begin(9600);
  pinMode(ledpin, OUTPUT);
  pinMode(lightpin,   INPUT);
  pinMode(ledpin2, OUTPUT);
  pinMode(lightpin2,   INPUT);
}
void loop() {
  int lightsens = analogRead(lightpin);
  int lightsens2 = analogRead(lightpin2); // reads   analog data from light sensor
  if (lightsens < LIGHT) {
    digitalWrite(ledpin,   HIGH); //turns led on
    delay(1000);
  }
  else {
    digitalWrite(ledpin,   LOW);
  }
  if (lightsens2 < LIGHT2) {
    digitalWrite(ledpin2,  HIGH);
    delay(1000);
  }
  else {
    digitalWrite(ledpin2,   LOW);
  }
}

'''

# Bill of Materials
Here's where you'll list the parts in your project. To add more rows, just copy and paste the example rows below.
Don't forget to place the link of where to buy each component inside the quotation marks in the corresponding row after href =. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize this to your project needs. 

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Arduino Uno | Programing | $20 | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Jumbo RGB LED | Bigger brighter light | $10 | <a href="https://www.amazon.com/Tricolor-Diffused-Multicolor-Electronics-Components/dp/B01CI6EWHK/"> Link </a> |
| Perf board | More secure than a breadboard | $17 | <a href="https://www.amazon.com/EPLZON-Solderable-Breadboard-Gold-Plated-Electronics/dp/B0D5XL9BKR/"> Link </a> |

# Other Resources/Examples
One of the best parts about Github is that you can view how other people set up their own work. Here are some past BSE portfolios that are awesome examples. You can view how they set up their portfolio, and you can view their index.md files to understand how they implemented different portfolio components.
- [Smart Street Light](https://projecthub.arduino.cc/angadiameya007/smart-street-light-6ad038)
- [PIR Sensor](https://projecthub.arduino.cc/electronicsfan123/interfacing-arduino-uno-with-pir-motion-sensor-593b6b)
- [Tinkercad](https://www.tinkercad.com/things/5Kf0tQV9aa7-mattiassharpstreetlightbase/edit?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard%2Fdesigns%2F3d)

To watch the BSE tutorial on how to create a portfolio, click here.
