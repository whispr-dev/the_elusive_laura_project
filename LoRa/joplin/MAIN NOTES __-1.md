## MAIN NOTES ##
*mostly from:*
[https://www.youtube.com/watch?v=N3FXej9fqIk]

a quick film about "LoRa 868 ("meshtastic")" comms:@


**LoRa** (**L**ong **R**ange) **WAN** (**W**ide **A**rea **N**etwork)*

long range for EU is colloquially "868" 
(actually 863 to 870 and 873 MHz)

given example transciever as basic std. in youtube is the "heltec lora 862 multiband" - it uses usb C
note: takes an attic 12" to even get near the 20km mark, good coax essential cos most coax sux.

- LoRa will do 0.3-50 kbps data rate long range (2-5km urban, 15+km suburb) on battery power - travels thru walls/glass/concrete
- achieved via short range/duration vs. sub-GHz freq and adaptive data rate scheme trade off.
- star-of-star topology LoRaWAN gateways 'transparent bridge' as part of central network, cloud or endpoint to endpoint.

*(LoRa and LoRaWAN are not synonymous. LoRaWAN is the network on which all LoRa devices operate. The media access control (MAC) layer protocol on top of the physical layer, LoRaWAN defines the communication protocol and system architecture for a device. LoRa, on the other hand, is a radio frequency carrier signal based in the physical (PHY) layer that converts received data into signals. LoRa architecture enables the long-range communication link.)*


3 encryption layers used:
unique network key EUI64
unique app key EUI64
device specific EUI128

3 types of tx/rx
Class A:: uplink (tx) anytime, downlink (rx) window allocated upon transmit
Class B:: network provides beacon sig. decices use to open rrx windows at sched times inbetween which tx's occur
class C:: power hungry continuous recieve unless tx'ing


- With LoRa  range is huge advantage:
tho Wi-Fi is well-known and commonplace, it lacks the range that LoRa got, limiting its useability. 
- Whilst Wi-Fi has the edge where faster, stronger signals are required, LoRa that is  best solution for long-range communication and tracking applications.
- LoRa is extremely reliable for data transfer. Due to its architecture, LoRa has less interference and error when transferring data, meaning that it is also very reliable.


LoRa sends information via radio waves and through chirp spread spectrum modulation or CSS. A chirp spread spectrum is similar to the way that bats and dolphins communicate and has a wave flow that is a linear and sinusoidal wave that can increase or decrease in frequency over time. It is on this chirp spread spectrum that information is encrypted and sent.
LoRa gateways employ nodes and star architecture in order to send and receive communications. Because this method of communication requires less infrastructure, it means that there is the capacity to support more devices and transfer more data per gateway.
Per each 8-channel gateway, hundreds and thousands of messages can be sent across an enormous amount of devices, up to 10,000 to be exact. Plus, the more gateways that are added, the more information can be sent and more devices are supported.


LoRa employs 3 module types:
The first module available is a **transceiver** module, which is designed for low-functioning devices.
The second is a **telemetry** module, which is used to transfer radiological data.
The third and final module type is a **modem** module.

Typically, **nodes** broadcast data to be picked up by **gateways** that forward the information to **operator servers** for processing
*n.b. The term “gateway” often refers to the physical casing that contains the hardware and application software necessary to connect IoT devices to the cloud.*

the range for a LoRa module can go as far as 20km, and depending on the module, they will operate on a frequency as low as 137 Mhz and potentially as high as 1000 Mhz.

basic install overview guide:
- purchase and install a gateway product. 
- set up the LoRa gateway by installing the memory card from the LoRa gateway kit.
- attach the necessary antennas to the LoRa gateway product
- take the installed SD card from your computer and place it into the LoRa gateway.
- turn on the power supply and ensure all the lights turn on at the bottom of the gateway.
- test connectivity. Send a test packet and check the metadata in the received packet to see what gateways you are connected to.
:)

best 8 chan Gateways based around:
SX1308IMLTRT smd ic
8chan 
8x 125khz demod
1x 125/250/500 high speed demod
1x fsk modem
consumption 1.5w
LoRa Corecell gateway reference design
