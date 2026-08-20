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

* Important note: Line 51: Changed the value of baud in `Serial.begin` from 115200 to 9600 in order to display the content of the txt file in the serial monitor.


The code should be looking like so:

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(65).png?raw=true)

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(66).png?raw=true)




## Result

After verifying and uploading the code to the ESP, this was the result:

- When the value is `1`:
  
![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(72).png?raw=true)

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(69).png?raw=true)

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Pic%202.jpeg?raw=true)


- When the value is `0`:
  
![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(70).png?raw=true)

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Screenshot%20(71).png?raw=true)

![Image ALT](https://github.com/Bandr-Mohammed/On-Off-ESP-LED/blob/main/Pic%201.jpeg?raw=true)
