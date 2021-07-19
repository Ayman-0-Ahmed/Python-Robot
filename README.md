[Softwares](https://github.com/Ayman-0-Ahmed/Python-Robot#softwares)
___
What can he do? (Functions)
---
1. He can talk. [(Talking)](https://github.com/Ayman-0-Ahmed/Python-Robot#talking)
2. He can understand what you say. [(Speech Recognition)](https://github.com/Ayman-0-Ahmed/Python-Robot#movement-speech)
3. He can copy what you do. [(Movement copying)](https://github.com/Ayman-0-Ahmed/Python-Robot#movement-copying)

**Needed libraries:**
1. Alsa sound utilities
2. MPlayer

**Pip libraries:**
1. PYTTSX3
___
[Hardwares][https://github.com/Ayman-0-Ahmed/Python-Robot#hardwares]
___
We will need this parts (modules).
1. [Speaker x 1 (or two)](https://github.com/Ayman-0-Ahmed/Python-Robot#installing-speakers)
2. [Microphone x 1 (or two, for better hearing)](https://github.com/Ayman-0-Ahmed/Python-Robot#installing-microphone)
3. [Camera x 1](https://github.com/Ayman-0-Ahmed/Python-Robot#installing-camera)
4. (Actuators [maybe servos])
___
**Softwares**
---
Talking
---
Step 1: We start by updating our Raspbian distribution using these commands below.
```
sudo apt-get update
```
```
sudo apt-get upgrade
```

Step 2: We have to install the Alsa sound utilities and MPlayer with the command below.
```
sudo apt-get install alsa-utils
```
```
sudo apt-get install mplayer
```

Step 3: We have to select a 3.5 mm jack as audio output.

To do this, issue the ‘sudo raspi-config’ command.
Then go to "System Options", "Audio", "Force 3.5mm ('headphone') jack" and finally "Finish".

Step 4: We have to install the PYTTSX3 library using pip.
```
pip install pyttsx3
```

Step 5: Then we upload the code below to our Raspberry Pi and run it.

```
import pyttsx3
engine = pyttsx3.init()
engine.say("Hi, I am a robot. I can talk.")
engine.runAndWait()
```
___
Movement copying
---
Step 1: We first need have to add a [camera](https://github.com/Ayman-0-Ahmed/Python-Robot#installing-camera). (because the robot has to see some thing to copy it.)

Step 2: We use AI to detect if a person is visible in the camera (video). When he hears a person say Look (robot name)! can you do do this? He will Motion Track that person. He will the angles of the persons limbs.

Step 3: He will start a timer, and stop it when he detects that the person has moved his limbs. he will save the timer data.
___
**Hardwares**
---
