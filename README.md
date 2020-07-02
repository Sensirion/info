# Overview over Sensirion's github repositories

## Preface

The goal of this page is to help users navigate the various driver offerings by Sensirion. 

Sensirion is offering reference driver implementations that are meant to support customers in their product designs. These are tested extensively, and cover most of the common functionality of our sensors. They are also written in a platform independent way, to enable easy porting to new platforms. Because of that, they tend to be a bit more complex than a simple platform specific library, but offer peace of mind for the user to freely move to a different hardware platform with minimal adjustments. These drivers are described in the [Reference Drivers](#reference-drivers) section below.

We are also offering some platform specific libraries, in particular for Arduino based platforms. These offer reduced complexity, but cannot be ported to other platforms easily. See the section [Arduino driver repositories and examples](#arduino-driver-repositories-and-examples) below.

Lastly, there's a few third party repositories that we wanted to include. Please note that Sensirion is creating these projects and therefore being listed there is not an official endorsement, but there's really great work out there by our community that we wanted to share with you!

Finally, feel free to report any issues you have with the drivers on the respective github repository. If you have questions outside of the drivers we're sharing here - for example anything that's related to the sensors themselves, rather than the drivers - the best way to get help is to use the [contact form](https://www.sensirion.com/en/about-us/contact/) on the Sensirion website. 

## Reference Drivers

TBD

### Platform support

TBD

Example: https://github.com/winkj/raspberrypi-ess

## Arduino driver repositories and examples

TBD

## Linux Kernel drivers

TBD

## Third party repositories provided by our developer community

> :warning: Please note that libraries listed in this section are not maintained by Sensirion, and are not supported by Sensirion.

> Note that this list does not claim to be complete. If you would like to have your repository listed here, please file an issue and let us know the github URL. ThHanks!

- SPS30 on Arduino by Paul van Haastrecht: https://github.com/paulvha/sps30
- SPS30 on Raspberry Pi by Paul van Haastrecht: https://github.com/paulvha/sps30_on_raspberry


### Sparkfun
- SGP30 Arduino Library: https://github.com/sparkfun/SparkFun_SGP30_Arduino_Library
- SHTC3 Arduino Library: https://github.com/sparkfun/SparkFun_SHTC3_Arduino_Library
- SCD30 Arduino Library: https://github.com/sparkfun/SparkFun_SCD30_Arduino_Library


### Adafruit
- SHT31 Arduino Library: https://github.com/adafruit/Adafruit_SHT31
- SHT31D CircuitPython Library: https://github.com/adafruit/Adafruit_CircuitPython_SHT31D
- SHTC3 Arduino Library: https://github.com/adafruit/Adafruit_SHTC3
- SHTC3 CircuitPython Library: https://github.com/adafruit/Adafruit_CircuitPython_SHTC3
- SGP30 Arduino Library: https://github.com/adafruit/Adafruit_SGP30
- SGP30 CircuitPython Library: https://github.com/adafruit/Adafruit_CircuitPython_SGP30


### Seeedstudio
- SGP30 Arduino Library: https://github.com/Seeed-Studio/SGP30_Gas_Sensor
- SGP30 Python Driver: https://github.com/Seeed-Studio/Seeed_Python_SGP30
- SHT31 Arduino Library: https://github.com/Seeed-Studio/Grove_SHT31_Temp_Humi_Sensor
- SHT35 Arduino Library: https://github.com/Seeed-Studio/Seeed_SHT35
- SCD30 Arduino Library: https://github.com/Seeed-Studio/Seeed_SCD30