# Arduino-TimeLapse-Slider
Arduino code for DIY timelapse slider controller.



This is the time lapse controller for the Light Camera Slider vimeo.com/17725662. You select the number of shots to be taken (1-999), the time to move (3-999 minutes), Interval between shots (1-999 seconds), Exposure time (1-999 seconds) and press go. The controller will drive the slider the required amount, stop, fire the camera, wait for the exposure time and then drive the slider for the next shot. You can see it in use in this video vimeo.com/54571725,
The stepper motor drive provides very precise movement of the slider. The stepper motor requires 1600 steps per revolution and I am using a ¼ in BSW drive thread (20 threads per inch). One step gives (25.4 / 20) / 1600 = 0.0008 mm movement of the slider. If I took 1000 shots at the slowest stepping speed the slider would move a total of 0.8 mm. The fastest the stepper motor can drive the slider is 4 mm per second or about 3 minutes for the full 650 mm travel.
I have load tested the motor which can lift up to 5kg vertical on the slider before it stalls.
These are the major components.
•	4N25 Opto Coupler IC, this electrically isolates the controller from the camera.jaycar.com.au/products_uploaded/ZD1926_4N25SR2-M__ZD1934_4N35SR2-M.pdf
•	Arduino Demilanove 328, this is the brain of the controller. Think this controller has been replaced by the Arduino Uno.
•	DFRobot Arudino Keyboard Shield, provides LCD and keyboard input.
•	ProtoShield for Arduino, board to attach Opto Coupler and EasyDriver.
•	EasyDriver Steper Motor Driver, this drives the stepper motor. See schmalzhaus.com/EasyDriver/
•	Stepper Motor, provides the drive.
•	Powered by 12V 6Ah battery Motor://www.jaycar.com.au/productView.asp?ID=SB2485&form=CAT2&SUBCATID=997#12
I purchased these components from the Australian web site: littlebirdelectronics.com. You can also find these components at the US site: sparkfun.com.
For full details on the micro controllers see: arduino.cc
You can also find code for motion control at: openmoco.org. I looked at this code, but ended up writing my own. See the code at gist.github.com/752692. All the controller electronics is easy to use as this is the first time I have ever built one. I am no electronics expert as you can tell from my terrible soldering job.
I have made a few improvements to the slider since filming; see photos on the attached link. These include:
•	Finished the controller enclosure to protect the electronics.
•	Replaced the purchased stepper drive coupling with one I made. Mine one is much more precise and stronger.
•	Replaced the carriage drive nut with a bigger bronze bush for smother action.
•	Added adjustable drag breaks to the carriage. This reduces any slack in the bearings and provides smoother sliding when controlling the slider by hand.
