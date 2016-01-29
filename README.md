# OpenNI-RaspberryPi2
Project for Interim Project on Poznań Univercity of Technology

STEPS:

1. VMPlayer configuration for SD Card reader - http://www.htpcguides.com/how-to-use-sd-card-reader-in-vmplayer-and-vmworkstation/

2. Ubuntu MATE installation on SD Card

3. Particion resizing -  https://ubuntu-mate.org/raspberry-pi/

4. OpenNI2 library download from GitHub - GitHub https://github.com/OpenNI/OpenNI2

5. You have to download and install (on MATE):
- GCC 4.x
- Python 2.6+/3.x
- LibUSB 1.0.x
- LibUDEV
- JDK 6.0
- FreeGLUT3
- Doxygen
- GraphViz

6. Compilation on RaspberryPi2 - deleting -mfloat-abi-softfb flag from Platform.arm
Helpful link: https://github.com/OpenNI/OpenNI/issues/81

7. To add all examples you have to edit Makefile:
- add at the end of the file:
	core_samples: $(CORE_SAMPLES)
	Tools: $(ALL_TOOLS)
- Write in console make - library will be compiled
- Additional tools - write in console: 
	GLUT_SUPPORTED =1 make tools
Link: http://jetsonhacks.com/2014/08/28/building-openni2-structure-sensor/
