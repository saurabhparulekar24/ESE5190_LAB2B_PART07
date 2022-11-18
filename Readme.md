## PIO Sequencer
Using the logic analyser codes which captures the input as well as output on any GPIO pin, we slowed downed the clock so that we can capture the boot button at 500us interverals. The boot buttons state was read using direct register access.

We integrated the original code of the sequencer into the logic analyser code to create the PIO sequencer, as data was already being recorded by the analyser, we created an array which was sent to the Play function of the original Sequencer. The output is sent to the neoPixel as well as to GPIO 23 using PIO.


https://user-images.githubusercontent.com/57740824/202586802-48fe0814-e282-4c1e-8ebe-7fd66a8e1558.mp4

The graph looks inverted as it is, the Boot Button rest state is High/1, the raw array is sent to the python script and inverted data to the LED

# Data Logging
The data captured is also send via the USB, and capture by a python script which converts it into a graph of the boot button state, you can find the .py file in the code folder, you can use the script to acquire data from your QtPy board, just update the COM port

