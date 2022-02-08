# Hardware configuration

## Housing

FieldEP comprises two submersible housings - cylinders of 76.2 mm internal diameter with aluminium flanges and an acrylic front window. Electronic hardware and a microscope lens are supported within the housing by a 3D-printed structure consisting of a front plate, rear plate and a tray. A LiPo battery is held underneath the tray to provide primary power to the electronics. 

The second housing is used as an auxiliary battery chamber and LED lamp which illuminates subjects from the rear, towards the camera. Animals of interest are held between the two housings on an adjustable stage, held in place with nuts on threaded bar.


![6-inch_stereo_assembly_2022-Jan-25_12-48-59PM-000_CustomizedView4010012559](https://user-images.githubusercontent.com/36079329/151009417-c0eac081-4633-4dbd-bbe9-f904de3b6eec.png)


Front quarter           |  Rear quarter
:-------------------------:|:-------------------------:
![149bc0e0-a3e4-408e-a984-4182f6ccd5b9](https://user-images.githubusercontent.com/36079329/151009428-6739611c-4fd0-424b-936b-00f0f004af40.PNG) | ![6-inch_stereo_assembly_2022-Jan-25_02-07-14PM-000_CustomizedView30723018784](https://user-images.githubusercontent.com/36079329/151009349-7c3ce3ef-4660-4742-8464-047ac64c10dd.png)


The modular design of the support structures inside the housing allows for ease of printing on non-specialist 3D printers, and accommodates changes to electronics and battery space requirements via minor changes to the lens supports which are bolted to the forward protrusions of the electronics tray.

## Electronic components
Stacking headers are used to connect the main components to the Raspberry Pi. Stacking moPiJuicedules are connected in the order:
|Pi HAT|
|---|
|GSM Module|
|PiJuice|
|PiZero Breakout|
|Raspberry Pi|

Pin headers are also broken out to allow for connection to other modules. For the operation of sensors and communications the connections are broken out to a 90-degree pin header for connection via jumper wires.

|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|  |TX|RX| |  |  |  |  |  |  |  |  |GPIO25|GND|  |  |  |GPIO26|GND|  |
|21|22|23|24|25|26|27|28|29|30|31|32|33|34|35|36|37|38|39|40|
|3.3V|SCL|SDA|GND|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |

## Housing parts list:
* Blue Robotics 3" housing
    - 298mm Acrylic tube (x2)
    - O-ring flange (x4)
    - Aluminium end cap - 7-hole
    - Acrylic end cap
    - Switch (x2)
    - M10 vent & plug
    - M10 penetrator for 3mm cable
    - M10 penetrator for 4.5 mm cable
    - M3 x 16 mm screws (x 20 - included with end caps)
* M8 x 250 mm threaded bar (x4)
* Faceplate
* Rear plate
* Electronics tray
* M3 x 10 cap head screws (x 12)
* _M2.5 x 10 cap head screws (x 4)_

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


## Consumables
* Solder
* Epoxy encapsulant
* Wire (22 AWG)
