# HexBright Factory

This repository is essentially a clone of the hexbright\_factory.ino file from the
[hexbright/samples](https://github.com/hexbright/samples) repository.

## Uploading your first binary to the HexBright Flex.

For me to be able to upload my first program to my HexBright light, I
followed the following steps, which I got from [David Hilton]
(https://github.com/dhiltonp). I just added some additional notes.

1. Download and install the [Arduino Development Software]
   (http://arduino.cc/en/Main/Software). Note: Microsoft Windows users 
   shouldn't use the OS's "Extract All..." command. That'll leave out 
   some necessary subdirectories. I successfully unzipped it with 7-zip.

2. Download and install the CP210x driver (Use a VCP Driver Kit from [here]
   (http://www.silabs.com/products/mcu/Pages/USBtoUARTBridgeVCPDrivers.aspx)).
   Note that the HexBright charges via USB without the driver, but the
   driver is necessary for Arduino to upload the code to the light.

3. Run Arduino without the HexBright light connected.  Select 
   Tools->Serial Port, and make note of which COM ports exist. Then connect
   the HexBright. Then examine Tools->Serial Port again, and make note
   of which COM port appeared. That's the one you need to select for
   the HexBright.

4. Select File->Preferences, and set your sketchbook location to the
   location of the Arduino repository you cloned locally.  Quit and restart
   the Arduino IDE.

5. Select Tools->Board and select HexBright for your device.


## hexbright-factory.ino

I made a small change to hexbright\_factory.ino that came with the light.
Quick button presses cycle through off, low, medium, and high modes.  
Hold down the button while off for blinky mode. What's different now is that
after you've used the light for a couple of seconds, then the next button
press turns it off.  You no longer have to cycle through the various brightness
levels.

## Other Resources

* [HexBright](http://hexbright.com/)
* [Arduino IDE](http://arduino.cc/en/Main/Software)
* [Factory sample code](https://github.com/hexbright/samples)
* [dhiltonp's sample code](https://github.com/dhiltonp/hexbright)
* [YouTube tutorial](Programming your Hexbright)

