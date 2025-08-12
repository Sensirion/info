# Overview of Sensirion's GitHub Repositories

| [Reference Drivers](#reference-drivers-and-examples) | [Arduino](#arduino-drivers-and-examples) | [Python](#python-packages) | [Raspberry Pi](#raspberry-pi-drivers-and-examples) | [Developer Community](#third-party-repositories-provided-by-our-developer-community) |
|-------------------|---------|--------|--------------|------------|

## Table of Contents

1. [Preface](#preface)
2. [Reference Drivers and Examples](#reference-drivers-and-examples)
    1. [Repositories](#repositories)
    2. [Concept](#concept)
    3. [Example use](#example-use)
3. [Arduino Drivers and Examples](#arduino-drivers-and-examples)
4. [Python Packages](#python-packages)
5. [RaspberryPi Drivers and Examples](#raspberry-pi-drivers-and-examples)
6. [Third party repositories provided by our developer community](#third-party-repositories-provided-by-our-developer-community)
    1. [Linux Kernel drivers](#linux-kernel-drivers)
    2. [From Paul van Haastrecht](#from-paul-van-haastrecht)
    3. [Sparkfun](#sparkfun)
    4. [Adafruit](#adafruit)
    5. [Seeedstudio](#seeedstudio)
    6. [Rust packages](#rust-packages)
    7. [Node packages](#node-packages)
7. [Tutorials](#tutorials)
    1. [Multiple sensors with same I2C address](#multiple-sensors-with-same-i2c-address)
    2. [Pull-up resistors on I2C lines](#pull-up-resistors-on-i2c-lines)
8. [Documentation](#documentation)

## Preface

The goal of this page is to help users navigate the various driver offerings by
Sensirion.

### «Platform independent drivers requiring minimal porting efforts»

Sensirion is offering reference driver implementations that are meant to
support customers in their product designs. These are tested extensively, and
cover most of the common functionality of our sensors. They are also written in
a platform independent way, to enable easy porting to new platforms. Because of
that, they tend to be a bit more complex than a simple platform specific
library, but offer peace of mind for the user to freely move to a different
hardware platform with minimal adjustments. These drivers are described in
the [Reference Drivers and Examples](#reference-drivers-and-examples) section below.

| [Reference Drivers](#reference-drivers-and-examples) |
|---|

### «Platform specific prototyping starters»

We are also offering some platform specific libraries and code snippets to
boost your prototyping activities. We have an extensive set
of [Arduino drivers and examples](#arduino-drivers-and-examples)
and [Python packages](#python-packages), which can be used to communicate with
our sensors via the
[Sensirion SensorBridge](https://sensirion.com/sensorbridge) ([Sensirion Evaluation Kit](https://sensirion.com/sek))
.

We also offer some preconfigured and simplified variations of the reference
drivers for the RaspberryPi platform. See the
section [RaspberryPi Drivers and Examples](#Raspberry-Pi-Drivers)

| [Arduino](#arduino-drivers-and-examples)  | [RaspberryPi](#Raspberry-Pi-Drivers) | [Python](#python-packages)
|---|---|---|

### «Thank you to the open source community»

Lastly, there's a few third party repositories that we wanted to include.
Please note that Sensirion is creating these projects and therefore being
listed there is not an official endorsement, but there's really great work out
there by our community that we wanted to share with you!

| [Community Picks](#third-party-repositories-provided-by-our-developer-community) |
|---|

Finally, feel free to report any issues you have with the drivers on the
respective GitHub repository. If you have questions beyond the drivers we're
sharing here - for example anything that's related to the sensors themselves,
rather than the drivers - the best way to get help is to use
the [contact form](https://www.sensirion.com/en/about-us/contact/) on the
Sensirion website.

For more information, please also check out
or [Developer Website](https://developer.sensirion.com/).

## Reference Drivers and Examples

Generic drivers for all platforms from small-scale embedded-systems to
full-scale Operating Systems.

### Repositories

| Product | Function | Bus |Repository |
|---------|----------|-----|-----------|
| Gas Index Algorithm | Algorithm providing Index output signals from the SGP40/41 raw signals | I2C | [gas-index-algorithm](https://github.com/Sensirion/gas-index-algorithm) |
| SCD | Carbon Dioxide (CO2) | I2C | [embedded-scd](https://github.com/Sensirion/embedded-scd) |
| SCD30 | Carbon Dioxide (CO2) | I2C | [embedded-i2c-scd30](https://github.com/Sensirion/embedded-i2c-scd30) |
| SCD4X | Carbon Dioxide (CO2) | I2C | [embedded-i2c-scd4x](https://github.com/Sensirion/embedded-i2c-scd4x) |
| SDP | Differential Pressure | I2C | [embedded-i2c-sdp](https://github.com/Sensirion/embedded-i2c-sdp) |
| SEN44 | Multi Sensor Environmental Nodes | I2C | [embedded-i2c-sen44](https://github.com/Sensirion/embedded-i2c-sen44) |
| SEN44 | Multi Sensor Environmental Nodes | UART | [embedded-uart-sen44](https://github.com/Sensirion/embedded-uart-sen44) |
| SEN5x | Multi Sensor Environmental Nodes | I2C | [embedded-i2c-sen5x](https://github.com/Sensirion/embedded-i2c-sen5x) |
| SEN66 | Multi Sensor Environmental Nodes | I2C | [embedded-i2c-sen66](https://github.com/Sensirion/embedded-i2c-sen66) |
| SFA3X | Formaldehyde | I2C | [embedded-i2c-sfa3x](https://github.com/Sensirion/embedded-i2c-sfa3x) |
| SFA3X | Formaldehyde | UART | [embedded-sfa3x](https://github.com/Sensirion/embedded-sfa3x) |
| SFM | Gas Flow Meter | I2C | [embedded-sfm](https://github.com/Sensirion/embedded-sfm) |
| SFM3003 | Gas Flow Meter | I2C | [embedded-i2c-sfm-sf06](https://github.com/Sensirion/embedded-i2c-sfm-sf06) |
| SFM3012 | Gas Flow Meter | I2C | [embedded-i2c-sfm-sf06](https://github.com/Sensirion/embedded-i2c-sfm-sf06) |
| SFM3019 | Gas Flow Meter | I2C | [embedded-i2c-sfm-sf06](https://github.com/Sensirion/embedded-i2c-sfm-sf06) |
| SFM3119 | Gas Flow Meter | I2C | [embedded-i2c-sfm-sf06](https://github.com/Sensirion/embedded-i2c-sfm-sf06) |
| SFM4300 | Gas Flow Meter | I2C | [embedded-i2c-sfm-sf06](https://github.com/Sensirion/embedded-i2c-sfm-sf06) |
| SGP | Metal-Oxide (MOX) Gas | I2C | [embedded-sgp](https://github.com/Sensirion/embedded-sgp) |
| SGP40 | Metal-Oxide (MOX) Gas | I2C | [embedded-i2c-sgp40](https://github.com/Sensirion/embedded-i2c-sgp40) |
| SGP41 | Metal-Oxide (MOX) Gas | I2C | [embedded-i2c-sgp41](https://github.com/Sensirion/embedded-i2c-sgp41) |
| SHT | Humidity and Temperature | I2C | [embedded-sht](https://github.com/Sensirion/embedded-sht) |
| SHT3x | Humidity and Temperature | I2C | [embedded-i2c-sht3x](https://github.com/Sensirion/embedded-i2c-sht3x) |
| SHT4x | Humidity and Temperature | I2C | [embedded-i2c-sht4x](https://github.com/Sensirion/embedded-i2c-sht4x) |
| SPS | Particulate Matter | I2C | [embedded-sps](https://github.com/Sensirion/embedded-sps) |
| SPS | Particulate Matter | UART | [embedded-uart-sps](https://github.com/Sensirion/embedded-uart-sps) |
| STC3x | Carbon Dioxide (CO2) | I2C | [embedded-i2c-stc3x](https://github.com/Sensirion/embedded-i2c-stc3x) |
| STS | Temperature | I2C | [embedded-sts](https://github.com/Sensirion/embedded-sts) |
| STS3x | Temperature | I2C | [embedded-i2c-sts3x](https://github.com/Sensirion/embedded-i2c-sts3x) |
| STS4x | Temperature | I2C | [embedded-i2c-sts4x](https://github.com/Sensirion/embedded-i2c-sts4x) |
| SVM4x | Metal-Oxide (MOX) Gas | I2C | [embedded-i2c-svm4x](https://github.com/Sensirion/embedded-i2c-svm4x) |
| SVM4x | Metal-Oxide (MOX) Gas | UART | [embedded-uart-svm4x](https://github.com/Sensirion/embedded-uart-svm4x) |
| SLF3x | Liquid Flow | I2C | [embedded-i2c-sf06-lf](https://github.com/Sensirion/embedded-i2c-sf06-lf) |
| LD20 | Liquid Flow | I2C | [embedded-i2c-sf06-lf](https://github.com/Sensirion/embedded-i2c-sf06-lf) |

Shared code can be found here <https://github.com/Sensirion/embedded-common>

### Concept

Our reference drivers are our suggested starting point to implement stable
products. They are tested intensively, and we provide support to our customers
in case they face unexpected behaviour of the code.

It is implemented in a platform independent way, by means of a small "Hardware
Abstraction Layer" (HAL) which abstracts the interface level commands (I2C,
delay functions etc.) from the sensor readout protocols and timing. Because of
that, the drivers can be ported to new platforms rather easily.

We currently support a range of sample implementation. At the time of writing
this document, the following platforms are supported:

- Linux (with the I2C userspace interface, see below for Linux Kernel drivers)
- MBED OS
- Arduino Wire library (plus alternative I2C library)
- Microchip SAMD2
- Nordic nRF51
- STM32F1
- Zephyr (User Space)

The complete list of implementations is availble in the `embedded-common`
repository.

- For devices with an I2C controller ("hardware-I2C")
  <https://github.com/Sensirion/embedded-common/tree/master/i2c/sample-implementations>
- For devices without an I2C controller, whereby I2C is modulated with the help
  of General-Purpose Input/Output Pins (GPIOs) ("software-I2C")
  <https://github.com/Sensirion/embedded-common/tree/master/i2c/sample-implementations/GPIO_bit_banging/sample-implementations>

### Example use

To build a driver, there's three steps that need to be completed:

1. Download the release zip file from GitHub
2. Configure your platform, or build your own platform support file
3. Compile example / integrate into your application

As an example, for the SHTC1 humidity sensor for Linux user space:

1. Download the latest release zip file from
   <https://github.com/Sensirion/embedded-sht/releases> and unzip
2. Copy
   `embedded-common/i2c/sample-implementations/linux_user_space/sensirion_i2c_hal.c`
   to `embedded-common/i2c/`, thereby overwriting the empty sample
   implementation provided as starting point for new platform support.
3. type `make shtc1_example_usage`

After that, you should have an executable called `shtc1_example_usage` that
will read out the SHTC1 sensor. Run it with `./shtc1_example_usage`. Depending
on the permissions on the I2C device file (which is defined as
`#define I2C_DEVICE_PATH "/dev/i2c-1"` in the provided sample implementation)
you might have to add your user to the respective group or run as root with
`sudo ./shtc1_example_usage`.

## Arduino Drivers and Examples

To simplify developing on the Arduino platform, we offer a range of dedicated
libraries. Those are available directly though the Library Manager in the
Arduino IDE or here on GitHub, so installation is just a few mouse clicks away.

The code can be found in the following repositories:

| Product | Function | Bus |Repository |
|---------|----------|-----|-----------|
| Gas Index Algorithm | Algorithm providing Index output signals from the SGP40/41 raw signals | I2C | [arduino-gas-index-algorithm](https://github.com/Sensirion/arduino-gas-index-algorithm) |
| SCD30 | Carbon Dioxide (CO2) | I2C | [arduino-i2c-scd30](https://github.com/Sensirion/arduino-i2c-scd30) |
| SCD4X | Carbon Dioxide (CO2) | I2C | [arduino-i2c-scd4x](https://github.com/Sensirion/arduino-i2c-scd4x) |
| SDP | Differential Pressure | I2C | [arduino-i2c-sdp](https://github.com/Sensirion/arduino-i2c-sdp) |
| SDP | Differential Pressure | I2C | [arduino-sdp](https://github.com/Sensirion/arduino-sdp) |
| SEN44 | Multi Sensor Environmental Nodes | I2C | [arduino-i2c-sen44](https://github.com/Sensirion/arduino-i2c-sen44) |
| SEN44 | Multi Sensor Environmental Nodes | UART | [arduino-uart-sen44](https://github.com/Sensirion/arduino-uart-sen44) |
| SEN5x | Multi Sensor Environmental Nodes | I2C | [arduino-i2c-sen5x](https://github.com/Sensirion/arduino-i2c-sen5x) |
| SEN66 | Multi Sensor Environmental Nodes | I2C | [arduino-i2c-sen66](https://github.com/Sensirion/arduino-i2c-sen66) |
| SFA3X | Formaldehyde | I2C | [arduino-i2c-sfa3x](https://github.com/Sensirion/arduino-i2c-sfa3x) |
| SFA3X | Formaldehyde | UART | [arduino-uart-sfa3x](https://github.com/Sensirion/arduino-uart-sfa3x) |
| SFM3000 | Gas Flow Meter | I2C | [arduino-i2c-sfm3000](https://github.com/Sensirion/arduino-i2c-sfm3000) |
| SFM3003 | Gas Flow Meter | I2C | [arduino-i2c-sfm-sf06](https://github.com/Sensirion/arduino-i2c-sfm-sf06) |
| SFM3012 | Gas Flow Meter | I2C | [arduino-i2c-sfm-sf06](https://github.com/Sensirion/arduino-i2c-sfm-sf06) |
| SFM3019 | Gas Flow Meter | I2C | [arduino-i2c-sfm-sf06](https://github.com/Sensirion/arduino-i2c-sfm-sf06) |
| SFM3119 | Gas Flow Meter | I2C | [arduino-i2c-sfm-sf06](https://github.com/Sensirion/arduino-i2c-sfm-sf06) |
| SFM4300 | Gas Flow Meter | I2C | [arduino-i2c-sfm-sf06](https://github.com/Sensirion/arduino-i2c-sfm-sf06) |
| SFM6000 | Gas Flow Meter | UART | [arduino-uart-sfx6xxx](https://github.com/Sensirion/arduino-uart-sfx6xxx) |
| SFC6000 | Mass Flow Controller | UART | [arduino-uart-sfx6xxx](https://github.com/Sensirion/arduino-uart-sfx6xxx) |
| SGP40 | Metal-Oxide (MOX) Gas | I2C | [arduino-i2c-sgp40](https://github.com/Sensirion/arduino-i2c-sgp40) |
| SGP41 | Metal-Oxide (MOX) Gas | I2C | [arduino-i2c-sgp41](https://github.com/Sensirion/arduino-i2c-sgp41) |
| SHT | Humidity and Temperature | I2C | [arduino-sht](https://github.com/Sensirion/arduino-sht) |
| SHT3x | Humidity and Temperature | I2C | [arduino-i2c-sht3x](https://github.com/Sensirion/arduino-i2c-sht3x) |
| SHT4x | Humidity and Temperature | I2C | [arduino-i2c-sht4x](https://github.com/Sensirion/arduino-i2c-sht4x) |
| STS3x | Temperature | I2C | [arduino-i2c-sts3x](https://github.com/Sensirion/arduino-i2c-sts3x) |
| STS4x | Temperature | I2C | [arduino-i2c-sts4x](https://github.com/Sensirion/arduino-i2c-sts4x) |
| SLF3x | Liquid Flow Meter | I2C | [arduino-liquid-flow](https://github.com/Sensirion/arduino-liquid-flow) |
| SPS | Particulate Matter | I2C | [arduino-sps](https://github.com/Sensirion/arduino-sps) |
| STC3X | Carbon Dioxide (CO2) | I2C | [arduino-i2c-stc3x](https://github.com/Sensirion/arduino-i2c-stc3x) |
| SVM4x | Metal-Oxide (MOX) Gas | I2C | [arduino-i2c-svm4x](https://github.com/Sensirion/arduino-i2c-svm4x) |
| SVM4x | Metal-Oxide (MOX) Gas | UART | [arduino-uart-svm4x](https://github.com/Sensirion/arduino-uart-svm4x) |
| SLF3x | Liquid Flow | I2C | [arduino-i2c-sf06-lf](https://github.com/Sensirion/arduino-i2c-sf06-lf) |
| LD20 | Liquid Flow | I2C | [arduino-i2c-sf06-lf](https://github.com/Sensirion/arduino-i2c-sf06-lf) |


Shared code can be found
here: [Arduino Core](https://github.com/Sensirion/arduino-core)

Finally, we offer some snippets to bootstrap our flow sensor based prototypes
(SLG, SLI, SLS, SLQ-QTxxx, LG16-xxxxD, LS32, LPG10, LD20 and SLF3x):
[Arduino Liquid Flow Snippets](https://github.com/Sensirion/arduino-liquid-flow-snippets)

Want to understand every single step of your Arduino driver in one file? Check
the
[Arduino Snippets](https://github.com/Sensirion/arduino-snippets) and learn it
from scratch.

## Python Packages

The python packages work with our I2C and UART (SHDLC) sensors when attached to
a compatible system. Compatible means, that the system provides an I2C
Interface (e.g. a Raspberry Pi on Linux) for I2C sensors, or a
COM-Port/Character device for UART (SHDLC) sensors. The Python drivers also
work for I2C sensors attached with
a [SensorBridge](https://sensirion.com/sensorbridge)

| Product | Function | Bus |Repository |
|---------|----------|-----|-----------|
| SensorBridge | USB to I2C Gateway | USB |  [python-shdlc-sensorbridge](https://github.com/Sensirion/python-shdlc-sensorbridge) |
| Gas Index Algorithm | Algorithm providing Index output signals from the SGP40/41 raw signals | I2C | [gas-index-algorithm](https://github.com/Sensirion/gas-index-algorithm) |
| SCD30 | Carbon Dioxide (CO2) | I2C | [python-i2c-scd30](https://github.com/Sensirion/python-i2c-scd30) |
| SCD4x | Carbon Dioxide (CO2) | I2C | [python-i2c-scd](https://github.com/Sensirion/python-i2c-scd) |
| SDP | Differential Pressure | I2C | [python-i2c-sdp](https://github.com/Sensirion/python-i2c-sdp) |
| SFA3X | Formaldehyde | I2C | [python-i2c-sfa3x](https://github.com/Sensirion/python-i2c-sfa3x) |
| SFA3X | Formaldehyde | UART | [python-shdlc-sfa3x](https://github.com/Sensirion/python-shdlc-sfa3x) |
| SFC5XXX | Mass Flow Controller for Gasses | UART | [python-shdlc-sfc5xxx](https://github.com/Sensirion/python-shdlc-sfc5xxx) |
| SFC6000 | Mass Flow Controller | UART | [python-uart-sfx6xxx](https://github.com/Sensirion/python-uart-sfx6xxx) |
| SFM3003 | Gas Flow Meter | I2C | [python-i2c-sfm-sf06](https://github.com/Sensirion/python-i2c-sfm-sf06) |
| SFM3012 | Gas Flow Meter | I2C | [python-i2c-sfm-sf06](https://github.com/Sensirion/python-i2c-sfm-sf06) |
| SFM3019 | Gas Flow Meter | I2C | [python-i2c-sfm-sf06](https://github.com/Sensirion/python-i2c-sfm-sf06) |
| SFM3119 | Gas Flow Meter | I2C | [python-i2c-sfm-sf06](https://github.com/Sensirion/python-i2c-sfm-sf06) |
| SFM4300 | Gas Flow Meter | I2C | [python-i2c-sfm-sf06](https://github.com/Sensirion/python-i2c-sfm-sf06) |
| SFM6000 | Gas Flow Meter | UART | [python-uart-sfx6xxx](https://github.com/Sensirion/python-uart-sfx6xxx) |
| SGP4X | Metal-Oxide (MOX) Gas | I2C | [python-i2c-sgp4x](https://github.com/Sensirion/python-i2c-sgp4x) |
| SHT3x | Humidity and Temperature | I2C | [python-i2c-sht3x](https://github.com/Sensirion/python-i2c-sht3x) |
| SHT4x | Humidity and Temperature | I2C | [python-i2c-sht4x](https://github.com/Sensirion/python-i2c-sht4x) |
| STC | Carbon Dioxide (CO2) | I2C | [python-i2c-stc](https://github.com/Sensirion/python-i2c-stc) |
| SVM4x | Metal-Oxide (MOX) Gas | I2C | [python-i2c-svm4x](https://github.com/Sensirion/python-i2c-svm4x) |
| SVM4x | Metal-Oxide (MOX) Gas | UART | [python-shdlc-svm4x](https://github.com/Sensirion/python-shdlc-svm4x) |
| SLF3x | Liquid Flow | I2C | [python-i2c-sf06-lf](https://github.com/Sensirion/python-i2c-sf06-lf) |
| LD20 | Liquid Flow | I2C | [python-i2c-sf06-lf](https://github.com/Sensirion/python-i2c-sf06-lf) |
| SEN5x | Multi Sensor Environmental Nodes | I2C | [python-i2c-sen5x](https://github.com/Sensirion/python-i2c-sen5x) |
| SEN66 | Multi Sensor Environmental Nodes | I2C | [python-i2c-sen66](https://github.com/Sensirion/python-i2c-sen66) |


## Raspberry Pi Drivers and Examples

The Raspberry Pi drivers are [Reference Drivers](#reference-drivers-and-examples), which we
configured for Raspberry Pi and should work out of the box. See the
corresponding README.md files for detailed setup and installation instructions.

Learn how to port any [Reference Drivers](#reference-drivers-and-examples) to Raspberry Pi
by reading [this section](#example-use).

| Product | Function | Bus |Repository |
|---------|----------|-----|-----------|
| Gas Index Algorithm | Algorithm providing Index output signals from the SGP40/41 raw signals | I2C | [gas-index-algorithm](https://github.com/Sensirion/gas-index-algorithm) |
| SCD30 | Carbon Dioxide (CO2) | I2C | [raspberry-pi-i2c-scd30](https://github.com/Sensirion/raspberry-pi-i2c-scd30) |
| SCD4X | Carbon Dioxide (CO2) | I2C | [raspberry-pi-i2c-scd4x](https://github.com/Sensirion/raspberry-pi-i2c-scd4x) |
| SDP | Differential Pressure | I2C | [raspberry-pi-i2c-sdp](https://github.com/Sensirion/raspberry-pi-i2c-sdp) |
| SEN44 | Multi Sensor Environmental Nodes | I2C | [raspberry-pi-i2c-sen44](https://github.com/Sensirion/raspberry-pi-i2c-sen44) |
| SEN44 | Multi Sensor Environmental Nodes | UART | [raspberry-pi-uart-sen44](https://github.com/Sensirion/raspberry-pi-uart-sen44) |
| SEN5x | Multi Sensor Environmental Nodes | I2C | [raspberry-pi-i2c-sen5x](https://github.com/Sensirion/raspberry-pi-i2c-sen5x) |
| SEN66 | Multi Sensor Environmental Nodes | I2C | [raspberry-pi-i2c-sen66](https://github.com/Sensirion/raspberry-pi-i2c-sen66) |
| SFA3X | Formaldehyde | I2C | [raspberry-pi-i2c-sfa3x](https://github.com/Sensirion/raspberry-pi-i2c-sfa3x) |
| SFA3X | Formaldehyde | UART | [raspberry-pi-uart-sfa3x](https://github.com/Sensirion/raspberry-pi-uart-sfa3x) |
| SGP40 | Metal-Oxide (MOX) Gas | I2C | [raspberry-pi-i2c-sgp40](https://github.com/Sensirion/raspberry-pi-i2c-sgp40) |
| SGP41 | Metal-Oxide (MOX) Gas | I2C | [raspberry-pi-i2c-sgp41](https://github.com/Sensirion/raspberry-pi-i2c-sgp41) |
| SHT3x | Humidity and Temperature | I2C | [raspberry-pi-i2c-sht3x](https://github.com/Sensirion/raspberry-pi-i2c-sht3x) |
| SHT4x | Humidity and Temperature | I2C | [raspberry-pi-i2c-sht4x](https://github.com/Sensirion/raspberry-pi-i2c-sht4x) |
| STS3x | Temperature | I2C | [raspberry-pi-i2c-sts3x](https://github.com/Sensirion/raspberry-pi-i2c-sts3x) |
| STS4x | Temperature | I2C | [raspberry-pi-i2c-sts4x](https://github.com/Sensirion/raspberry-pi-i2c-sts4x) |
| STC3X | Carbon Dioxide (CO2) | I2C | [raspberry-pi-i2c-stc3x](https://github.com/Sensirion/raspberry-pi-i2c-stc3x) |
| SVM4x | Metal-Oxide (MOX) Gas | I2C | [raspberry-pi-i2c-svm4x](https://github.com/Sensirion/raspberry-pi-i2c-svm4x) |
| SVM4x | Metal-Oxide (MOX) Gas | UART | [raspberry-pi-uart-svm4x](https://github.com/Sensirion/raspberry-pi-uart-svm4x) |
| SLF3x | Liquid Flow | I2C | [raspberry-pi-i2c-sf06-lf](https://github.com/Sensirion/raspberry-pi-i2c-sf06-lf) |
| LD20 | Liquid Flow | I2C | [raspberry-pi-i2c-sf06-lf](https://github.com/Sensirion/raspberry-pi-i2c-sf06-lf) |
| SFM3003 | Gas Flow Meter | I2C | [raspberry-pi-i2c-sfm-sf06](https://github.com/Sensirion/raspberry-pi-i2c-sfm-sf06) |
| SFM3012 | Gas Flow Meter | I2C | [raspberry-pi-i2c-sfm-sf06](https://github.com/Sensirion/raspberry-pi-i2c-sfm-sf06) |
| SFM3019 | Gas Flow Meter | I2C | [raspberry-pi-i2c-sfm-sf06](https://github.com/Sensirion/raspberry-pi-i2c-sfm-sf06) |
| SFM3119 | Gas Flow Meter | I2C | [raspberry-pi-i2c-sfm-sf06](https://github.com/Sensirion/raspberry-pi-i2c-sfm-sf06) |
| SFM4300 | Gas Flow Meter | I2C | [raspberry-pi-i2c-sfm-sf06](https://github.com/Sensirion/raspberry-pi-i2c-sfm-sf06) |
| SFM6000 | Gas Flow Meter | UART | [raspberry-pi-uart-sfx6xxx](https://github.com/Sensirion/raspberry-pi-uart-sfx6xxx) |
| SFC6000 | Mass Flow Controller | UART | [raspberry-pi-uart-sfx6xxx](https://github.com/Sensirion/raspberry-pi-uart-sfx6xxx) |


## Third party repositories provided by our developer community

> :warning: Please note that libraries listed in this section are not maintained
> by Sensirion, and are not supported by Sensirion.

> Note that this list does not claim to be complete. If you would like to have
> your repository listed here, please submit a pull request or file an issue
> containing the github URL. Thanks!

### Linux Kernel drivers

While our reference drivers above support [Linux](https://www.kernel.org)'
userspace I2C interface, there's also the option to build them into the kernel.
Some of those drivers were authored by Sensirion (and are now maintained as part
of the Linux kernel). The following drivers are available:

#### Via HWMON interface
- SHT1x (legacy): <https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht15.c>
- SHT2x: `CONFIG_SENSORS_SHT21` <https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht21.c>
- SHT3x: `CONFIG_SENSORS_SHT3x` <https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht3x.c>
- SHTC1/SHTC3, SHTW1/SHTW2: `CONFIG_SENSORS_SHTC1` <https://github.com/torvalds/linux/blob/master/drivers/hwmon/shtc1.c>
- SHT4x: 'CONFIG_SENSOR_SHT4x' <https://github.com/torvalds/linux/blob/master/drivers/hwmon/sht4x.c>

#### Via IIO interface
- SGP30, SGPC3: `CONFIG_SENSIRION_SGP30` <https://github.com/torvalds/linux/blob/master/drivers/iio/chemical/sgp30.c>
- SGP30, SGPC3: Out-of-tree module with more functionality and for older
  kernels: <https://github.com/Sensirion/linux-sgp30/>
- SPS30: `CONFIG_SPS30` <https://github.com/torvalds/linux/blob/master/drivers/iio/chemical/sps30.c>
- SPS30: Out-of-tree module for older kernels: <https://github.com/Sensirion/linux-sgp30/>


### From Paul van Haastrecht
- SPS30 on Arduino : <https://github.com/paulvha/sps30>
- SPS30 on Raspberry: <https://github.com/paulvha/sps30_on_raspberry>


### Sparkfun
- SGP30 Arduino Library: <https://github.com/sparkfun/SparkFun_SGP30_Arduino_Library>
- SHTC3 Arduino Library: <https://github.com/sparkfun/SparkFun_SHTC3_Arduino_Library>
- SCD30 Arduino Library: <https://github.com/sparkfun/SparkFun_SCD30_Arduino_Library>


### Adafruit
- SHT31 Arduino Library: <https://github.com/adafruit/Adafruit_SHT31>
- SHT31D CircuitPython Library: <https://github.com/adafruit/Adafruit_CircuitPython_SHT31D>
- SHTC3 Arduino Library: <https://github.com/adafruit/Adafruit_SHTC3>
- SHTC3 CircuitPython Library: <https://github.com/adafruit/Adafruit_CircuitPython_SHTC3>
- SGP30 Arduino Library: <https://github.com/adafruit/Adafruit_SGP30>
- SGP30 CircuitPython Library: <https://github.com/adafruit/Adafruit_CircuitPython_SGP30>


### Seeedstudio
- SGP30 Arduino Library: <https://github.com/Seeed-Studio/SGP30_Gas_Sensor>
- SGP30 Python Driver: <https://github.com/Seeed-Studio/Seeed_Python_SGP30>
- SHT31 Arduino Library: <https://github.com/Seeed-Studio/Grove_SHT31_Temp_Humi_Sensor>
- SHT35 Arduino Library: <https://github.com/Seeed-Studio/Seeed_SHT35>
- SCD30 Arduino Library: <https://github.com/Seeed-Studio/Seeed_SCD30>

### Rust packages

#### Sensirion HDLC
- Crate: <https://crates.io/crates/sensirion-hdlc>
- Source code: <https://github.com/iohe/sensirion-hdlc>

#### SPS30 UART
- Crate: <https://crates.io/crates/sps30>
- Source code: <https://github.com/iohe/sps30>

#### SPS30 I2C
- Crate: <https://crates.io/crates/sps30-i2c>
- Source code: <https://github.com/david-gherghita/sps30-i2c-rs>

#### SHTCX Driver
- Crate: <https://crates.io/crates/shtcx>
- Source code: <https://github.com/dbrgn/shtcx-rs>

#### SHT3x Driver
- Crate: <https://crates.io/crates/sht3x>
- Source code: <https://github.com/miek/sht3x-rs>

#### SGP30 Driver
- Crate: <https://crates.io/crates/sgp30>
- Source code: <https://github.com/dbrgn/sgp30-rs>

#### SFC6XXX UART
- Crate: <https://crates.io/crates/sfc6xxx-rs>
- Source code: <https://github.com/EggShark/sfc-rs>

### Node packages

#### Sensirion HDLC

Node package which uses Node SerialPort and RXJS to implement Sensirion HDLC.

- NPM package: <https://www.npmjs.com/package/@cytera/sensirion-hdlc>
- Source code: <https://github.com/cytera/sensirion-hdlc-node>

## Tutorials

### Multiple sensors with same I2C address
If you need to connect multiple sensors with the same I2C address to your board, you have different options.

1. Change the I2C address of the sensor. This is possible for some of our sensors, for example for the SF06 Liqui Flow Sensors.
   - Tutorial article using an ESP32 DevKit board to connect two SLF3x sensors on [hackster.io](https://www.hackster.io/sensirion-software/use-several-slf3x-sensors-on-the-same-i2c-bus-f4aaed)
   - Example for Arduino in [arduino-i2c-sf06-lf](https://github.com/Sensirion/arduino-i2c-sf06-lf/tree/master/examples/exampleI2cAddressChange) driver repository
   - Example for Raspberry-Pi in the [raspberry-pi-i2c-sf06-lf](https://github.com/Sensirion/raspberry-pi-i2c-sf06-lf/tree/master/example-i2c-address-change) driver repository
   
2. Use a multiplexer
   - Tutorial article using an Arduino Uno and multiplexer board to connect two SCD41 sensors [hackster.io](https://www.hackster.io/sensirion-software/using-a-multiplexer-to-connect-multiple-sensors-1363d0)
   - Example code [arduino-i2c-multiplexer-usage](https://github.com/Sensirion/arduino-i2c-multiplexer-usage)

3. Use different I2C buses
   - Tutorial article using an ESP32 DevKit board to connect two SCD41 sensors on different I2C buses [hackster.io](https://www.hackster.io/sensirion-software/two-separate-i2c-buses-on-esp32-67a65c)
   - Example code and documentation for a few boards on Arduino IDE platform [arduino-i2c-different-buses-example](https://github.com/Sensirion/arduino-i2c-different-buses-example)

### Pull-up resistors on I2C lines
For a robust communication over I2C it is important to understand the role of pull-up resistors. You find a documentation
in the GitHub repository [arduino-i2c-different-buses-example](https://github.com/Sensirion/arduino-i2c-different-buses-example/blob/main/i2c-pull-up-resistors-intro.md).

## Documentation
### Sensirion BLE Specifications
Do you want to integrate a Sensirion Bluetooth gadget into your own project ?  
To learn more about the BLE specifications used by Sensirion Bluetooth devices please check out the [dedicated page](https://sensirion.github.io/ble-services/).
