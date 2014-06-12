#cs1504

## Using the Scanner

This information is documented elsewhere online, but briefly:

### Clear the scanner

This can be done inside the cs1504 code. There is a line at the end of the python file that can be commented if you do not wish the barcodes to be cleared automatically when the script is finished running. Otherwise, to clear the scanner, hold down the small minus button for 5 seconds or so.

### Delete scan

You can delete the last instance of a certain barcode by holding down the minus sign and scanning a barcode. Do not hold the minus sign too long or the entire set of files will be deleted as well.

### Toggle volume

You can mute or unmute the scanner by holding down the plus button for 10 or so seconds

### Other considerations

Be aware that the scanner can only hold about 140 scans. Do not expect it to handle weeks' worth of data.

Other functions can be seen in the python code. The python code is by no means an exhaustive listing of functionality for the scanner, and the scanner can be further programmed and new functions can be assigned to buttons. I just have never researched this.

## Installation

After going through the installation process on several computers now, I'm finally fed up and want to write this down in a centralized location. 

### Windows 7


#### Python

Go to the [Python downloads](http://www.python.org/downloads) website and download python *2*. _The scanner python drivers will not work with Python 3_. Select the latest release of python 2.

You will also need to install pySerial. The easiest method is to go to the [PySerial](https://pypi.python.org/pypi/pyserial) webiste and download pyserial-2.7.win32.exe, however this can also be done via pip.

If you do use pip, don't make the same mistake that I did and try to run it from inside the python shell. You will have to do this from Windows+R and then type in something like 

    c:\python27\scripts\pip install pyserial

#### Serial port driver
To get drivers for the Prolific USB to Serial adaptor, visit their website and download the drivers [here](http://www.prolific.com.tw/US/ShowProduct.aspx?p_id=225&pcid=41)

Once this is all up and running, you will need to right-click on My Computer, and open up manage -> device manager. Check where the COM drivers are installed, and see what number port it is.

Open up the cs1504.py file (or win-cs1504 if you prefer) and edit in the first few lines the port so the computer knows where to find the file.
