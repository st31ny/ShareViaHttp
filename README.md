# ShareViaHttp
Share any files or directory from the command line with other devices in your (W)LAN

Inspired by the [Android App "Share Via HTTP"](https://github.com/marcosdiez/shareviahttp), this shell script lets you share any files or directories from the command line using Python3's "http.server" module. Additionally, a QR code is generated for easy sharing with mobile devices in your WLAN.

## Requirements

* Python3 with http.server module (on Debian included in python3 package and its dependencies)
* python-qrcode (with the qr utility) for the console qr code generation
* some standard utilities: sed, awk

## Usage

* Just call the script and pass any files or directories as parameters.
* The script then generates a temporary directory with symbolic links to all specified files/directories and starts an http server in it.
* The link to this temporary directory is printed as text and qr code.
* In case only one directory or file is to be shared, the links directly points to this file/directory, so the download starts immediately.
* To stop sharing just exit the script by pressing Ctrl+C.
