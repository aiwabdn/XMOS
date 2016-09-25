# XMOS
Setting up XMOS microphone array on Ubuntu

Steps:

1. Copy the __99-xmos.rules__ files into __/etc/udev/rules.d/__ .
2. In a terminal run __sudo service udev reload__.
3. Reconnect your XMOS Mic array with the JTAG.
4. Setup the development environment, the IDE and the demonstration app as directed in the [link](https://www.xmos.com/published/getting-started-with-the-xcore-voice-smart-microphone-board), __Sections 1-4__
5. To setup command line tools ala __Section 7__, replace the __Makefile.linux__ file with the one given here.
6. Edit the __Makefile.linux__ file to replace the library path appropriately.
7. Run __sudo make -f Makefile.linux__. It should compile and create __./bin/xvsm_usb__ executable.
8. Follow demo instructions in document to check usb connection and calibrate XMOS.
