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
For Java implementation [install](http://processing.org) processing and open/compile

For C implementation compile each file with `gcc -o <output> file.c -lm`
**encode** expects a file called "input.txt" in the same directory as the code to contain a 200 x 200 space separated values from 0-255(One has been provided for your compression needs)
**decode** expects a file called "c_out.txt" in the same directory, meeting the same requirements as the encoding
**huffencode**  expects a file called "c_out_decode.txt" in the same directory, meeting the same requirements as the encoding
