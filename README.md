# Installation guide (Gstreamer)
prerequisites:
To run the GStreamer software, the [GStreamer](https://gstreamer.freedesktop.org/documentation/installing/index.html) libs must be installed.

To compile the transmitter use:

`` gcc -pthread -o transmitter threadMainTest.c cpipetest.c `pkg-config --cflags --libs gstreamer-1.0` ``

Optionally, the file configured for USB webcam streaming can be compiled as
`` gcc -pthread -o transmitterCam threadMainTestCam.c cpipetest.c `pkg-config --cflags --libs gstreamer-1.0` ``
But it might not work optimally with all cameras.
The resulting file can be run as `./transmitter <width> <height> <VCL> <address> <port>`

The receiver is a simple shell script and can be run as `./receiver.sh`
**Note that the receiver uses port 5004 as default**

The API is written in python and requires the transmitter to be running in order to function.
run with `python serverside.py`
Likewise the demo client `python client.py` with an optional string argument `<cmd>` which specifies a message sent to the server
# Installation guide (Standalone)
