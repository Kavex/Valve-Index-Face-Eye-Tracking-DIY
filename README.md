## Valve-Index-Face-Eye-Tracking-DIY

So you want Eye and Face Tracking? Do you have soldering skills? Update firmware on ESP32s?

You will need to know the basics or at least try to figure stuff out on your own. It's not easy, but with effort you can do it.

This is my face and tracking built with EyeTrackVR and Babble Face Tracking

Big Thanks to the following people and communities. Thanks Guys! Bookmark these pages. 

https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW

https://github.com/RamesTheGeneric/OpenIris

https://github.com/EyeTrackVR/EyeTrackVR

https://github.com/SummerSigh/ProjectBabble and https://github.com/Project-Babble/ProjectBabble

## **Parts:**

Here is a decent parts builder from EyeTrackVR to give you an idea: https://docs.eyetrackvr.dev/how_to_build/part_list

*   **Eye IR LEDS**: I would highly recommend the kits from https://store.eyetrackvr.dev/products/v4-mini-fully-solderless-kit

If you buy the IR LEDS yourself, then I would recommend doing your research!

Please read https://github.com/EyeTrackVR/EyeTrackVR?tab=readme-ov-file#about-ir-emitter-safety

*   **IR Cameras**: 3x OV2640 160 Degrees 850nm Night Vision https://www.aliexpress.us/item/3256804332354572.html

Warning: it's getting harder to find OV2640 since it's discontinued but the ov5640 should work as of 2025-01-11 per to OpenIris's changelog. I only have OV2640 since that is what I ordered. 

It's going to be really hard to get a 200mm length one, like impossible without some special order but i got you covered using extensions. (Make sure you get the 24Pin at 0.5MM Insert size)

Ribbon: https://www.aliexpress.us/item/3256802223169786.html

Pins: 24P

Connector Type: A-Forward Direction if you are using the Connector I suggested below

![image](https://github.com/user-attachments/assets/59980211-8a0f-42b4-a15f-da6dbc2a162d)

Insert Type: 0.5MM

Length: Get both size lengths, like ribbons are cheap and it's better to have spares and other sizes.

![image](https://github.com/user-attachments/assets/486b60d0-4bf4-49a2-8df6-1d927cf5fe3f)

Connector: https://www.aliexpress.us/item/3256804096715690.html

*   **Face IR LEDs (5mm 850nm IR Through Hole LEDS**): https://www.aliexpress.us/item/3256803759925241.html

(Choose "F5mm 850nm") 5mm 850nm IR Through Hole LEDS

Resistors for Face IR Emitters: https://www.aliexpress.us/item/3256806544238902.html

2x 160ohm 1/4w Resistors (If using 5V)  
(Choose "160R")

2x 82ohm 1/4w Resistors (If using 3.3V)  
(Choose "82R")

*   **Wire 28 AWG**
*   **Tracker Boards**: https://www.aliexpress.us/item/3256804601970891.html

Get 3 Seeed Studio XIAO ESP32S3 with the Camera Module, You can use other types of ESP32s if you want but these are the smallest to us. Honestly worth the extra few bucks. 

![image](https://github.com/user-attachments/assets/cc51ce85-b8ad-46c3-86c3-22354182edf3)

*   **USB Hub**: [https://www.amazon.com/dp/B0BJZ753D9](https://www.amazon.com/dp/B0BJZ753D9)
    
    You can use any USB Hub, but we are using this gumstick to make an all-in-one case. You need a heat gun, soldering iron, and dremel to get the board out. If you don't want all that work, then just get some short USB cables and plug them into the ESP32s. We will be soldering stuff to the gumstick USB PCB board. 
    
*   **3D Printer**: if you don't have one then go to your local library or maker space. All else fails use an online service to print parts or use lots of tape. idk your call. 

*   **Tools**: heat gun, soldering iron, solder, wire, computer, dremel, brains, safety glasses

## **Setting up the ESP32**

* Windows Drivers

Read https://wiki.seeedstudio.com/Seeeduino-XIAO/#software

It will have you download https://www.arduino.cc/en/software and install the Seeed Studio XIAO Board Module so Windows can see the COM Device
  
* Flashing ESP32: 

Download EyeTrackVR FirmwareFlashingTool: https://github.com/EyeTrackVR/FirmwareFlashingTool/releases

Open FirmwareFlashingTool and Select xiaosense3_usb

![image](https://github.com/user-attachments/assets/fa3d08e8-0c1c-4b17-a6e7-801167122fad)

You will need to put your ESP32 into Boot Mode which requires holding the Boot Mode Button when plugging in the USB C but I find it easier to hit the reset button then hold the Boot Mode button

![image](https://github.com/user-attachments/assets/7a1142df-d631-4062-9e5b-9e890df5928b)

Select the correct COM port for the device under auto and hit install Openiris. Once it is done you can replug in the USB C on the ESP32. Select the COM Port again and you should be able to download logs. If you see logs then you are ready to test the camera on them. You can test the camera with the Babble App or EyeTrack App listed in the software section.

## **3D Printning**

If you don't own a 3D Printer you can always use a service, read more here https://docs.eyetrackvr.dev/misc/jlc3dp

Go to https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW and get the files or make your own 

I personally printed [Gum Stick Remix for 3x ESPs plus USB Hub](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/tree/main/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Origional%20GSR%20Design%20(Cheap%20USB%20Hub))

<img width="794" height="351" alt="image" src="https://github.com/user-attachments/assets/e68b9f58-c482-4f72-8e05-46b10a56e49e" />


## **Wiring**

Some helpfull pictures on https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW

Items:
[Liquid Solder Flux](https://www.amazon.com/Liquid-Dropper-Soldering-Electrical-Electronics/dp/B0CN29BZKV)

Solder Iron and Solder

Wire 28-30 AWG

Helping hands if you got them

1. If you got the v4 mini fully solderless kit then you will need to solder two wires on the bottom if you want to have the gum stick power it.  

<img width="150" height="200" alt="image" src="https://github.com/user-attachments/assets/a263fed1-e6d2-4ea0-9851-14317ab69972" />

2. Soldering Seeed Studio XIAO ESP32S3

<img width="150" height="200" alt="image" src="https://github.com/user-attachments/assets/4e703e23-4c0b-4fe3-8b07-22f8c19a6f43" />
   
<img width="300" height="160" alt="image" src="https://github.com/user-attachments/assets/13b694e0-bc90-4bea-b6e6-ead6c737fb2f" />


## **Software and Setup**

Babble App: https://github.com/Project-Babble/ProjectBabble/releases

EyeTrack App: https://github.com/EyeTrackVR/EyeTrackVR/releases

VRCFaceTracking: https://docs.vrcft.io/







