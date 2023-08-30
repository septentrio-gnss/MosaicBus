<p align="center">
  <img width="100%" src="Assets/Banner-Bus.jpg">
</p>

# MosaicBus

## What is the MosaicBus project?
**MosaicBus is a Septentrio Open-Source hardware project powered by the Mosaic GNSS receiver that is compatible with the Mikroe mikroBUS standard.**
The objective of this project was to allow easy prototyping and development with the Mosaic by using the mikroBUS ecosystem.

The board also has the option to be used as a standalone device by using the USB-C connector and MosaicBus has been designed to be use either the Septentrio [**Mosaic-x5**](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5) or the [**Mosaic-H**](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-h).


## What is the Mosaic module?
**[Mosaic modules](https://www.septentrio.com/en/products/gnss-receivers/rover-base-receivers/receivers-modules) are Septentrio's small-size and low-power GNSS receiver modules ideal for providing highly accurate positions.** Mosaic modules integrate the latest generation of GNSS technology, delivering highly accurate positions with minimal power consumption. While compact in size they fully retain the high-reliability and exceptional accuracy performance that Septentrio receivers are known for. True multi-frequency multi-constellation technology gives our module receivers access to every possible signal from all available GNSS satellite constellations including the U.S. GPS, European Galileo, Russian GLONASS, as well BeiDou, QZSS and NavIC. [Septentrio’s advanced field-proven algorithms](https://www.septentrio.com/en/company/septentrio-gnss-technology) exploit this signal diversity to deliver maximum positioning availability and reference network compatibility.


## How to set up MosaicBus?
### Hardware
To start using the MosaicBus some antennas need to be connected to the board.
When using a Mosaic-x5 only a single antenna needs to be connected to the ANT 1 MMCX connector.
However when using the Mosaic-H a single or dual antenna setup can be configured.
To have a single antenna setup the antenna needs to be connected to the ANT 1 MMCX connector.
When using dual antennas the main antenna is connector to the ANT 1 MMCX connector while the auxillary is connected to the ANT 2 MMCX connector.

Afterwards just click the MosaicBus into a mikroBUS compatible carrier board.

The easiest way to configure the Mosaic is through the USB interface.
When connecting the MosaicBus with a computer through a USB-C cable. 
A new USB device should be visible on the system.
If the system is running Linux or MacOS, the drivers for the Mosaic are automatically installed.
When using a Windows system the drivers have to be installed manually.
These are contained on the new drive visible in file manager.
Running the installer is unnecessary when [**RxTools**](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) is already installed.

### Software
#### Web interface
By default the Mosaic suppports Ethernet-over-USB. Therefore its possible to connect to the receiver and access its information and configuration through a browser.
To do so search to the static IP address which is [`192.168.3.1`]().
This will show the Mosaic's web interface where you can configure the Mosaic.

#### Command line
Another way to connect to the Mosaic receiver is using its COM ports.
These ports should be visible as [`ACM0`]() and [`ACM1`]().
Using a serial terminal such as Putty a connection can be established using the following settings.
| port | baud rate | data bits | stop bits | parity | flow control |
|:---:|:---:|:---:|:---:|:---:|:---:|
| ACM0 / ACM1 | 115200 | 8 | 1 | no | none |

Now you can interface using the command line.
For information on the commands, syntax and reponses the Mosaic Reference Guide section 3.1 can be consulted.



*Designed by A. Gheeraert*
