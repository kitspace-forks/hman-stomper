The first prototype is a wooden one.
After creating a simpel arduino-sketch to play some sounds I had the problem that 
my "stomping" with the shoes creates not only one triggersignal when kicking the wood. 
It creates the same voltage when releasing the shoe from the box which creates or triggered the same samples.

I have recorded the Signal from the Piezo with my MAC using a Behringer Mixer with USB-Audio to get the signal into Audacity.

https://www.youtube.com/watch?v=9PsnRJPIw5M

The normal trigger signal when kicking the wood with the shoe contains all frequencies but the signal when 
releasing the shoe from the wood contains only the low frequencies.

For now, I have to create a High-Pass-Filter to trigger only if high frequencies are generated by kicking the wood.


The Filter has to cut all lower than around 4 kHz.
German Source for the filter: http://www.electronicdeveloper.de/FilterPassivHochpassRC_1O.aspx

I choice could be to add a 100K trimmer and a 500pF - Capapacity as HPF. With the 100k trimmer I would be able to adjust 
the filter a bit.

The prototype itself included an ESP8266, an I2C OLED 0.96" and a DAC. Additional I added some capacitors to 
stabalize the 5V-line a bit.

Currently a 1M-Ohm resistor is connected parallel to the piezo which should avoid to high voltages generated by the piezo.

Thats all for now.
