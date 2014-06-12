cs1504
======

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
