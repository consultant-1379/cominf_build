Instructions for creating Wifi Media for Linux
==============================================

This script is only supported on a Redhat linux system.

The genisoimage package needs to be installed.

1/ Create a directory and unpack the tar file wifi.tar into the directory

2/ Copy the latest Wifi software package (WiFiManager_YYY.bin) to a temporary
directory

3/ cd to directory where you unpacked wifi.tar

4/ Create the media using the command:

./create_iso.bsh -s <OSS Shipment> -r <Media revision>

Example:
./create_iso.bsh -s O13_2/13.2.9 -r A

The script will prompt for the full path to the Wifi software package (including the filename). 

5/ The iso and md5 files are created in the iso directory.

Note: The media is created using a place-holder CXP number at the minute. When
a valid CXP number is known, change the following line in the create_iso.sh script:

G_MEDIA_CXP_NUMBER=<CXPNUMBER>

Media Structure
===============

|->linux
	|->ewm (contains OSS install wrapper files)
	|
	|->software (contains WifiManager software)

|->.ewm_linux (media identity file for caching on MWS)

