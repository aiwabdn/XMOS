# XMOS
Setting up XMOS microphone array on Ubuntu

Steps:

1. Copy the [99-xmos.rules](https://github.com/aiwabdn/XMOS/blob/gh-pages/99-xmos.rules) files into __/etc/udev/rules.d/__ .
2. In a terminal run `sudo service udev reload`.
3. Reconnect your XMOS Mic array with the JTAG.
4. Setup the development environment, the IDE and the demonstration app as directed in the [link](https://www.xmos.com/published/getting-started-with-the-xcore-voice-smart-microphone-board), __Sections 1-4__
6. Install libusb-1.0 on system : `sudo apt-get install libusb-1.0-0-dev`
5. To setup command line tools ala __Section 7__, replace the __Makefile.linux__ file with the one given [here](https://github.com/aiwabdn/XMOS/blob/gh-pages/Makefile.linux).
6. Edit the __Makefile.linux__ file to replace the library paths in line __11__ appropriately.
7. Run `sudo make -f Makefile.linux`. It should compile and create __./bin/xvsm_usb__ executable.
8. Follow demo instructions in document to check usb connection and calibrate XMOS.
