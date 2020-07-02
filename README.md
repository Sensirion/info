# Overview over Sensirion's github repositories

## Preface

The goal of this page is to help users navigate the various driver offerings by Sensirion. 

Sensirion is offering reference driver implementations that are meant to support customers in their product designs. These are tested extensively, and cover most of the common functionality of our sensors. They are also written in a platform independent way, to enable easy porting to new platforms. Because of that, they tend to be a bit more complex than a simple platform specific library, but offer peace of mind for the user to freely move to a different hardware platform with minimal adjustments. These drivers are described in the [Reference Drivers](#reference-drivers) section below.

We are also offering some platform specific libraries, in particular for Arduino based platforms. These offer reduced complexity, but cannot be ported to other platforms easily. See the section [Arduino driver repositories and examples](#arduino-driver-repositories-and-examples) below.

Lastly, there's a few third party repositories that we wanted to include. Please note that Sensirion is creating these projects and therefore being listed there is not an official endorsement, but there's really great work out there by our community that we wanted to share with you!

Finally, feel free to report any issues you have with the drivers on the respective github repository. If you have questions outside of the drivers we're sharing here - for example anything that's related to the sensors themselves, rather than the drivers - the best way to get help is to use the [contact form](https://www.sensirion.com/en/about-us/contact/) on the Sensirion website. 

For more information, please also check out or [Developer Website](https://developer.sensirion.com/).

## Reference Drivers

### Concept

Our reference drivers are our suggested starting point to implement stable products. They are tested intensively, and we provide support to our customers in case they face unexpected behaviour of the code. 

It is implemented in a platform independent way, by means of a small "Hardware Abstraction Layer" which abstracts the interface level commands (I2C, delay functions etc.) from the sensor readout protocols and timing. Because of that, the drivers can be ported to new platforms rather easily.

We currently support a range of sample implementation. At the time of writing this document, the following platforms are supported:
- Linux I2C userspace
- MBED OS
- Arduino Wire library (plus alternative I2C library)
- Microchip SAMD2
- Nordic nRF51


### Repositories

|Product prefix | Function | Bus |Repository |
|---------------|----------|-----|---------------|
| SHT | humidity and temperature sensors | I2C | [embedded-sht](https://github.com/Sensirion/embedded-sht) |
| STS | temperature sensor | I2C | [embedded-sts](https://github.com/Sensirion/embedded-sts) |
| SCD | Carbon Dioxide (CO2) sensors | I2C |  [embedded-scd](https://github.com/Sensirion/embedded-scd) |
| SPS | Particulate Matter (PM0.5, PM1.0, PM2.5, PM4 and PM10) sensor | I2C | [embedded-sps](https://github.com/Sensirion/embedded-sps) |
| SPS | Particulate Matter (PM0.5, PM1.0, PM2.5, PM4 and PM10) sensor | UART |  [embedded-uart-sps](https://github.com/Sensirion/embedded-uart-sps) |
| SFM | gas flow meter | I2C | [embedded-sfm](https://github.com/Sensirion/embedded-sfm) |
| SGP | Metal-Oxide (MOX) gas sensor | I2C | [embedded-sgp](https://github.com/Sensirion/embedded-sgp) |

Shared code can be found here https://github.com/Sensirion/embedded-common

### Example use

To build a driver, there's three steps that need to be completed:

1. Download the a release zip file from Github
2. Configure your platform, or build your own platform support file
3. Compile example / integrate into your application

As an example, for the SHTC1 humidity sensor for Linux user space:
1. Download the latest release zip file from https://github.com/Sensirion/embedded-sht/releases and unzip
2. cp `hw_i2c/sample-implementations/linux_user_space/sensirion_hw_i2c_implementation.c` to `hw_i2c/`
3. type `make shtc1_example_usage.c`

After that, you should have an executable called `shtc1_example_usage` that will read out the SHTC1 sensor.


## Arduino driver repositories and examples

To simplify developing on the Arduino platform, we offer a range of dedicated libraries. Those are available directly though the Library Manager in the Arduino IDE, so installation is just a few mouse clicks away.

The code can be found in the following repositories:
- SHT series sensors: https://github.com/Sensirion/arduino-sht
- SPS series sensors: https://github.com/Sensirion/arduino-sps
- SDP3x and SDP8xx series sensor: https://github.com/Sensirion/arduino-sdp
- SLF3x series sensors: https://github.com/Sensirion/arduino-liquid-flow

We also provide a library for our [environmental sensor shield](https://developer.sensirion.com/platforms/environmental-sensor-shield/) products, which come with SGP30/SHTC1 and SGPC3/SHTC3 respectively: https://github.com/Sensirion/arduino-ess

Finally, we offer some snippets to help getting started with our flow sensor products (SLG, SLI, SLS, SLQ-QTxxx, LG16-xxxxD, LS32, LPG10, LD20 and SLF3x): https://github.com/Sensirion/arduino-liquid-flow-snippets

## Third party repositories provided by our developer community

> :warning: Please note that libraries listed in this section are not maintained by Sensirion, and are not supported by Sensirion.

> Note that this list does not claim to be complete. If you would like to have your repository listed here, please file an issue and let us know the github URL. Thanks!

### Linux Kernel drivers

While our reference drivers above support [Linux'](http://www.kernel.org) userspace I2C interface, there's also the option to build them into the kernel. Some of those drivers were authored by Sensirion (and are now maintained as part of the Linux kernel). The following drivers are available:

#### Via HWMON interface
- SHT1x (legacy): https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht15.c
- SHT2x: https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht21.c
- SHT3x: https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht3x.c
- SHTC1/SHTC3, SHTW1/SHTW2: https://github.com/torvalds/linux/blob/master/drivers/hwmon/shtc1.c

#### Via IIO interface
- SGP30/ SGPC3: https://github.com/torvalds/linux/blob/master/drivers/iio/chemical/sgp30.c
- SPS30: https://github.com/torvalds/linux/blob/master/drivers/iio/chemical/sps30.c


### From Paul van Haastrecht
- SPS30 on Arduino : https://github.com/paulvha/sps30
- SPS30 on Raspberry: https://github.com/paulvha/sps30_on_raspberry


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