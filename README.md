What can he do?
---
1. [He can talk.](https://github.com/Ayman-0-Ahmed/Python-Robot#talking)
2.

Needed libraries:
___
1. Alsa sound utilities
2. MPlayer

Pip libraries
___
1. PYTTSX3

___

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
