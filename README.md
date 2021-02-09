# CarPwner

CarPwner is a python script to "jam", capture, and replay rolling code signals using two yard stick one devices and rfcat.

This is done by jamming the receiver, capturing two or more remote presses, then stopping the jammer and replaying the first remote press saving the next capture in the rolling code series to replay later. The python code for rfcat-rolljam combines two projects that are already publicly available on Github that allow you to perform a rolljam like attack, it was just fairly clunky to do so requiring multiple scripts, this script simply combines everything into a single script that automates the process. It is up to you to follow all of the laws in your area. Jamming a signal is not legal in many areas. The author(s) of this code take no responsibility for your use or misuse of the script. If you choose to actually use the code you should do so in a controlled environment and only on equipment that you own. Please follow all local, state, federal, and international, and religious laws.

The below commands have been tested by an anonymous user to perform a rolljam attack on a remote power outlet
Capture and replay first code automatically: python CarPwner.py -f 315060000 -r 1818 -m -40 -o -2500000 -O capture.io
Capture and wait for keypress to replay first code: python CarPwner.py -f 315060000 -r 1818 -m -40 -o -2500000 -O capture.io -k
Load previous captures to replay: python CarPwner.py -I capture.io

Scan and replay of the code is borrowed from Andrew Macpherson's RfCatHelpers.

About
rfcat-rolljam is a python script to easily "jam", capture, and replay rolling code signals using two yard stick one devices and rfcat.
