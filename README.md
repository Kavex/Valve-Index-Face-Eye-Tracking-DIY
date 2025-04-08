## Valve-Index-Face-Eye-Tracking-DIY

So you want Eye and Face Tracking? Do you have soldering skills? Update firmware on ESP32s?

You will need to know the basics or at least try to figure stuff out on your own. It's not easy, but with effort you can do it.

This is my face and tracking built with EyeTrackVR and Babble Face Tracking

Big Thanks to the following people

https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW

https://github.com/RamesTheGeneric/OpenIris

https://github.com/EyeTrackVR/EyeTrackVR

https://github.com/SummerSigh/ProjectBabble and https://github.com/Project-Babble/ProjectBabble

## **Parts:**

*   **Eye IR LEDS**: I would highly recommend the kits from https://store.eyetrackvr.dev/products/v4-mini-fully-solderless-kit

If you buy the IR LEDS yourself, then I would recommend doing your research!

Please read https://github.com/EyeTrackVR/EyeTrackVR?tab=readme-ov-file#about-ir-emitter-safety

*   **IR Cameras**: 3x OV2640 160 Degrees 850nm Night Vision https://www.aliexpress.us/item/3256804332354572.html

It's going to be really hard to get a 200mm length one, so you most likely will need some extensions. Make sure you get the 24Pin at 0.5MM

Ribbon: https://www.aliexpress.us/item/3256802223169786.html

Pins: 24P

Connector Type: B-Reverse Direction

Insert Type: 0.5MM

Length: Get both, they are cheap.

Connector: https://www.aliexpress.us/item/3256804096715690.html

I ordered some custom ones from here https://www.alibaba.com/product-detail/Custom-OV2640-200mm-66-degree-160_1601401169934.html

*   **Face IR LEDs (5mm 850nm IR Through Hole LEDS**): https://www.aliexpress.us/item/3256803759925241.html

(Choose "F5mm 850nm") 5mm 850nm IR Through Hole LEDS

Resistors for Face IR Emitters: https://www.aliexpress.us/item/3256806544238902.html

2x 160ohm 1/4w Resistors (If using 5V)  
(Choose "160R")

2x 82ohm 1/4w Resistors (If using 3.3V)  
(Choose "82R")

*   **Wire 28 AWG**
*   **Tracker Boards**: https://www.aliexpress.us/item/3256804601970891.html

Get 3 Seeed Studio XIAO ESP32S3 with the Camera Module

![image](https://github.com/user-attachments/assets/cc51ce85-b8ad-46c3-86c3-22354182edf3)

*   **USB Hub**: [https://www.amazon.com/dp/B0BJZ753D9](https://www.amazon.com/dp/B0BJZ753D9)
    
    You can use any USB Hub, but we are using this gumstick to make an all-in-one case. You need a heat gun, soldering iron, and dremel to get the board out. If you don't want all that work, then just get some short USB cables and plug them into the ESP32s. We will be soldering stuff to the gumstick USB PCB board. 
    
*   **3D Printer**: if you don't have one then go to your local library or maker space. All else fails use an online service to print parts or use lots of tape. idk your call. 

*   **Tools**: heat gun, soldering iron, solder, wire, computer, dremel, brains, safety glasses

## **Setting up the ESP32**

* Download Software: 
  
Babble App: https://github.com/Project-Babble/ProjectBabble/releases

VRCFaceTracking: https://docs.vrcft.io/

EyeTrackVR FirmwareFlashingTool: https://github.com/EyeTrackVR/FirmwareFlashingTool/releases


