# ESP-01_INFO_2
How to setup ESP-01 via the Documentation
## Download the Firmware Zip and Extract
    https://bbs.espressif.com/
##### Version I downloaded
Version :- ESP8266_NONOS_SDK_V2.0.0_16_08_10
Zip File Has been added above
## Download the Flash Tool and Extract
The Zip File has been added above
## Setting Up Flash Tool
After extracting the Flash Tool *RUN APPLICATION ESP_DOWNLOAD_TOOL_V2.3*
### Making Appropriate Connections in your ESP-01 *Esp-01 to Arduino Connections*
Vcc => 3.3V // GND => GND // GPIO0 => GND // GPIO2 => 3.3V
CS => 3.3V // TXD => TX // RXD => RX
#### You will see this Screen *Ignore my Settings*
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool1.JPG)

Make Sure you have done the connections correctly

Set the COM PORT *Check in Device Manager* & BAUD RATE *Usually 9600 or 115200*

#### Next Disconnect the Vcc to ESP-01 and click *START*
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool2.JPG)
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool3.JPG)

#### Now connect the ESP-01 to Vcc back again
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool4.JPG)
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool5.JPG)

Check your QUAD: in the *Detected Info* and set *FLASH SIZE* as per the Documentation 
Pg 3-5 of Documentation

For Eg mine is *16 Bit*

![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashSize.JPG)

## Flashing the FIRMWARE
As you can see in the above image there are *Files* and the *Address*they need to be flashed at.

Go inside the extracted folder of FIRMWARE ESP8266_NONOS_SDK_V2.0.0_16_08_10 and add the Path and Address as shown in the documentation in the Flash Tool *Example of which I have shown below*

*Remember the name of the file doesn't exactly needs to be the same In my case the boot.bin was boot_v1.6.bin*
