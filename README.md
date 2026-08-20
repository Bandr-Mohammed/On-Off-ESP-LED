# On-Off-ESP-LED
Using the software `Arduino IDE` and `infinityfree` to turn on and off the LED of an ESP.

## Step one: On-Off input file

Creating a txt file in the file manager of `infinityfree` that would hold the values of the on-off function. (the values are manually changed from `0` to `1` and from `1` to `0` during the activation of the ESP) Like so:

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(62).png?raw=true)

The value is set to `1` or ON for now
![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(63).png?raw=true)


## Step two: Coding and uploading

Writing and editing the code that would be uploaded to the ESP.

Opening `Arduino IDE` and getting the initial code, like so:

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(64).png?raw=true)

Then edit the following in the code:

- Line 62: (SSID) and (PASSWORD) are parameters for personal wifi that the ESP connects to. (can be a personal hotspot too)
- Line 74: Add the link to the txt file made in `infinityfree`'s file manager.
- In {void setup} add the following code: `pinMode(LED_BUILTIN, OUTPUT);`
- Under line 89: add the following if-else statement: `if (payload == 1) {digitalWrite(LED_BUILTIN, HIGH); delay(1000);} else {digitalWrite(LED_BUILTIN, LOW);  delay(1000);}`


The code should be looking like so:

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(65).png?raw=true)

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(66).png?raw=true)
