# raspberry-pi-w

The Ubuntu 20.4 didn't recognize Raspberry Pi Pico W 2022 at first. It is related to the "type" of micro-USB cable function. Here more info: https://support.thepihut.com/hc/en-us/articles/360017234598-My-computer-won-t-detect-my-Raspberry-Pi-Pico.

For first steps, check page 5: https://datasheets.raspberrypi.com/picow/connecting-to-the-internet-with-pico-w.pdf
SDK Installation: 
$ git clone https://github.com/raspberrypi/pico-sdk
$ cd pico-sdk
$ git submodule update --init
$ cd ..
$ git clone https://github.com/raspberrypi/pico-examples

$ cd  $PICO_SDK_PATH/lib/tinyusb/examples/device/cdc_dual_ports
$ mkdir build && cd build
$ cmake .. && make -j4
