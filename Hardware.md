# Hardware configuration

## Housing

FieldEP comprises two submersible housings - cylinders of 76.2 mm internal diameter with aluminium flanges and an acrylic front window. Electronic hardware and a microscope lens are supported within the housing by a 3D-printed structure consisting of a front plate, rear plate and a tray. A LiPo battery is held underneath the tray to provide primary power to the electronics. 

The second housing is used as an auxiliary battery chamber and LED lamp which illuminates subjects from the rear, towards the camera. Animals of interest are held between the two housings on an adjustable stage, held in place with nuts on threaded bar.
![99fb7549-5d30-4ef4-b056-59008e5c76de](https://user-images.githubusercontent.com/36079329/153034909-e3417ff8-f221-42b4-afe5-1915defd05c9.PNG)


The modular design of the support structures inside the housing allows for ease of printing on non-specialist 3D printers, and accommodates changes to electronics and battery space requirements via minor changes to the lens supports which are bolted to the forward protrusions of the electronics tray.

## Electronic components
Stacking headers are used to connect the main components to the Raspberry Pi. Stacking moPiJuicedules are connected in the order:
|Pi HAT|
|---|
|GSM Module|
|PiJuice|
|PiZero Breakout|
|Raspberry Pi Zero W 2|

Pin headers are also broken out to allow for connection to other modules. For the operation of sensors and communications the connections are broken out to a 90-degree pin header for connection via jumper wires.

|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|  |TX|RX| |  |  |  |  |  |  |  |  |GPIO25|GND|  |  |  |GPIO26|GND|  |
|21|22|23|24|25|26|27|28|29|30|31|32|33|34|35|36|37|38|39|40|
|3.3V|SCL|SDA|GND|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |

## Housing parts list:
* Blue Robotics 3" housing
    - [298mm Acrylic tube](https://bluerobotics.com/store/watertight-enclosures/3-series/wte3-p-tube-12-r1/) (x2)
    - [O-ring flange](https://bluerobotics.com/store/watertight-enclosures/3-series/o-ring-flange-3-series/) (x4)
    - [Aluminium end cap - 7-hole](https://bluerobotics.com/store/watertight-enclosures/3-series/wte3-m-end-cap-7-hole-r1/)
    - [Aluminium end cap - 4-hole](https://bluerobotics.com/store/watertight-enclosures/3-series/wte3-m-end-cap-4-hole-r1/)
    - [Acrylic end cap](https://bluerobotics.com/store/watertight-enclosures/3-series/wte3-p-end-cap-r1/) (x2)
    - [Switch](https://bluerobotics.com/store/comm-control-power/switch/switch-10-5a-r1/) (x2)
    - [M10 vent & plug](https://bluerobotics.com/store/cables-connectors/penetrators/vent-asm-r1/)
    - M10 penetrator for 3mm cable
    - M10 penetrator for 4.5 mm cable
    - M3 x 16 mm screws (x 20 - included with end caps)
* M8 x 250 mm threaded bar (x4)
* Faceplate
* Rear plate
* Electronics tray
* [M3 x 10 mm cap head screws](https://www.accu.co.uk/en/low-head-cap-screws/8869-SSCL-M3-10-A4) (x 12)
* _[M2.5 x 10 cap head screws](https://www.accu.co.uk/en/cap-head-screws/3964-SSCF-M2-5-10-A4) (x 4)_

## Electronic components
**Camera module:**
* [Raspberry Pi Zero 2 W](https://thepihut.com/products/raspberry-pi-zero-2)
* Arducam HQ camera module
* [PiJuice Zero](https://uk.pi-supply.com/products/pijuice-zero)
* [Waveshare GSM7000e SIM module](https://www.unmannedtechshop.co.uk/product/nb-iot-emtc-edge-gprs-gnss-hat-for-raspberry-pi/)
* GSM Antenna
* SIM card
* SMA connector
* Blue Robotics TSYS01 temperature sensor
* Blue Robotics I2C bus splitter
* [3.7V 12000 mAh Lithium cell](https://uk.pi-supply.com/products/pijuice-12000mah-battery)
* [Ablelectronics Breakout PiZero](https://www.abelectronics.co.uk/p/68/breakout-pi-zero)
* Extra long stacking pin header for Raspberry Pi (15 mm pins)




**Light module:**
* [Sparkfun Lumidrive](https://coolcomponents.co.uk/products/lumidrive-led-driver)
* [Lumini 2" LED ring](https://coolcomponents.co.uk/products/lumini-led-ring-2-inch-40-x-apa102-2020?_pos=3&_sid=d6814a536&_ss=r)
* 3.7V Battery as big as possible. Something like [this](https://uk.pi-supply.com/products/lithium-ion-battery-pack-3-7v-4400mah) as a minimum.


_To be developed when time allows: Transistor-based switching of LED module to enable full power-down when not required. Suggested approach:_







https://bluerobotics.com/store/cables-connectors/penetrators/penetrator-10-25-a/
https://bluerobotics.com/store/cables-connectors/penetrators/penetrator-blank-10-25-a-r2/










## Consumables
* Solder
* [Epoxy encapsulant] (https://uk.rs-online.com/web/p/potting-compounds/1991430/?cm_mmc=UK-PLA-DS3A-_-google-_-CSS_UK_EN_Adhesives_%26_Sealants_%26_Tapes_Whoop-_-Potting+Compounds_Whoop+(2)-_-1991430&matchtype=&pla-361646333034&gclid=Cj0KCQiA-aGCBhCwARIsAHDl5x_ZlQvM5ZzL2Q7NVCp0c83qOvFK9o2Kul7I_UrpGSP3q1dLpcyBrxwaAjktEALw_wcB&gclsrc=aw.ds)
* Wire (22 AWG)


## Switch mode operation
FieldEP is designed to boot up into one of two modes. The process of bootup up is the same regardless of which mode is required. The _Boot_ switch is momentarily partially unscrewed (3(?) full turns). This initiates a boot cycle, whereby the state of the _Mode_ switch is monitored, and the system boots into the selected mode. 

During Live View mode, a change in state of the _Mode_ switch will power the system down. 

A typical deployment procedure would be:

1) Position stage approximately where laboratory testing has shown focus point to be with chosen magnification
2) Set _Mode_ to _Live_
3) Boot system by momentarily unscrewing _Boot_ switch until system powers up
4) Close _Boot_ switch
5) Immerse system in shallow water, LED lamp module first
6) Monitor live view whilst manipulating position of stage until focus is achieved
7) Change _mode_ switch to _Deployment_ by fully screwing closed
8) Boot system by momentarily unscrewing _Boot_ switch until system powers up

Step 8 initiates an acquisition cycle. The first acquisition will occur immediately and subsequent acquisitions will occur according to the time delay set in config.json.


![Operation modes - coloured background](https://user-images.githubusercontent.com/36079329/153027524-af0c3455-1c4d-44c3-96b9-c2bb1a5ccd50.png)
