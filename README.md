# Adafruit-Feather-Bluefruit-LE-Encoder-project
This project seeks to create a midi control knob that transmits over bluetooth to DAWs.

Currently, the Arduino code is a comglomeration of work by Gustavo Silviera and example sketches by Adafruit, the company behind the Feather Bluetooth LE board driving the project.

The good stuff:
1.  The Feather is connecting via bluetooth to iPad-based garageband as a midi controller, with hardware buttons registering assigned notes in code.
2.  Both buttons and encoder are sendign information to the Arduino serial monitor at baud rate 115200 (cannot be changed?)


To do:
1.  Assign encoder changed to actual midi CC.
2.  Test battery operation (when battery arrives).
3.  Machine the enclosure to house device.
4.  Code OLED as battery monitor and informational display.
5.  Machine second enclosure to include OLED display.

Issues at hand: 
1.  The encoder counts detents and the rises between detents as counter events, similar to mousebutton_Down and mousebutton_Up events, causing the counter to double for each click of the encoder.
2.  The encoder seems to be sampling changes at a very slow rate (1 half-turn per second).  Any faster, and the encoder records the same number again or decreases by 1.
3.  Neither 1 or two makes sense.
4.  High baud rate cannot be changed, and if 1 and 2 are traced to this, not sure how to remedy it.
