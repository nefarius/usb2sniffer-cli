# usb2sniffer-cli

lcsniff-cli software for [USB2Sniffer hardware](https://github.com/lambdaconcept/usbsniffer) ([buy](http://shop.lambdaconcept.com/home/35-usb2-sniffer.html)). It currently spits out pcap but also usb files that you can load in [usb2sniffer-qt](https://github.com/lambdaconcept/usb2sniffer-qt).

On Linux it requires [a kernel driver](https://github.com/lambdaconcept/ft60x_driver).

## Build

### Linux

No external libs required on Linux.

```bash
make
```

### Windows

Open the solution in Visual Studio and build. Put the resulting executable and `FTD3XX.dll` into a common directory.

## HowTo

### Linux usage

```bash
./lcsniff-cli fs /dev/ft60x0 test.pcap
./lcsniff-cli fs /dev/ft60x0 test.usb
```

### Windows usage

```PowerShell
.\lcsniff-cli fs 0 test.pcap
.\lcsniff-cli fs 0 test.usb
```

Then `CTRL+C` to stop capture.
