# Installation guide (Gstreamer)
Prerequisets :
To run the GStreamer software, the [GStreamer](https://gstreamer.freedesktop.org/documentation/installing/index.html) libs must be installed.

To compile the transmitter use:

``gcc -pthread -o transmitter threadMainTest.c cpipetest.c `pkg-config --cflags --libs gstreamer-1.0` ```

The resulting file can be run as `./transmitter <width> <height> <VCL> <address> <port>`

The receiver is a simple shell script and can be run as `./receiver.sh`

The API is written in python and requires the transmitter to be running in order to function.
run with `python serverside.py`
Likewise the demo client `python client.py` with an optional string argument <cmd> which specifies a message sent to the server 
#
