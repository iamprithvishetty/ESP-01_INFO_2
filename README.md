# ESP-01_INFO_2
How to setup ESP-01 via the Documentation
## Download the Firmware Zip and Extract
    https://bbs.espressif.com/
##### Version I downloaded
Version :- ESP8266_AT_Bin_V1.7
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
As you can see in the above image there are *Files* and the *Address* they need to be flashed at.

Go inside the extracted folder of ESP8266_AT_Bin_V1.7 and add the Path and Address as shown in the documentation in the Flash Tool *Example of which I have shown below*

*Remember the name of the file doesn't exactly needs to be the same In my case the boot.bin was boot_v1.6.bin*

![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool6.JPG)

#### Mark the Checkbox

![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool7.JPG)

#### Disconnect the Vcc from ESP-01 again and press START when you see connecting in Terminal Connect Vcc to ESP-01 Back

![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool8.JPG)
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool9.JPG)

#### After finishing the Flashing

![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/FlashTool10.JPG)

## AT Commands
#### Steps
Remove the GPIO pins from the connection and Disconnect and Connect again Vcc to ESP-01

#### Open Arduino IDE Serial Monitor set the Baud Rate and Carriage Return and *TYPE*
    AT
![alt text](https://github.com/iamprithvishetty/ESP-01_INFO_2/blob/main/Flash_Tool_Images/SerialMonitor.JPG)

    AT+UART_DEF=115200,8,1,0,3
    
### *Refrence*
    https://www.allaboutcircuits.com/projects/update-the-firmware-in-your-esp8266-wi-fi-module/#:~:text=Power%20up%20your%20ESP%20programming,flash%20download%20tool%20GUI%20window.
