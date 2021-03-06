# LoRa-Gateway-with-ESP32/NiceRF-Lora1276(915Mhz)
 Library required to build a gateway with esp32
 
Original Library
=====================================================

https://github.com/kersing/ESP-1ch-Gateway-v5.0

Testing
=====================================================

ESP32 based nodes with NiceRF-Lora1276 transceivers.

Connections
=====================================================

Esp32Pin----------------------NiceRF-Lora1276(915Mhz)

3.3V----------------------------------3.3V

Gnd-----------------------------------Gnd

GPIO18--------------------------------SCK

GPIO19--------------------------------MISO

GPIO23--------------------------------MOSI

GPIO5----------------------------------CS

GPIO22---------------------------------RST

GPIO17---------------------------------dio0

GPIO16---------------------------------dio1

GPIO4----------------------------------dio2

libraries required (Arduino IDE)
=====================================================

1-SPIFFS

2-U8G2
 
Configurations
===================================================== 

                                  In the file: ESP-sc-gway.ino

Lines 142 to 147-->  Network Parameters TTN
                                
                                 float lat=0;					
                               
                                 float lon=0;                                         
                                 
                                 int   alt=0;                                          
                                 
                                 char platform[24]	= "Esp32"; 				
                                 
                                 char email[40]		= "";    				
                                 
                                 char description[64]= "";				


                                  In the file: ESP-sc-gway.h

Line 51--> #define _SPREADING SF7,  Define spreading factor

Line 90--> #define _PIN_OUT 3 , 3 is the configurations for the esp32 pins

Line 181-->#define _TTNSERVER "router name", configure ttn router name "router name"

Lines 197 to 202: Network Parameters TTN

                  define _DESCRIPTION "description"
                  
                  define _EMAIL "email"
                  
                  define _PLATFORM "ESP32"
                  
                  define _LAT 
                  
                  define _LON 
                  
                  define _ALT 8
                  
            
Line257: { "YOUR WIFI SSID", "YOUR WIFI SSID PASSWORD" } , Insert wifi ssid and wifi password

                                     In the file: loraModem.h

Line 31 to 46--> Select the frequency

                  uint32_t  freq = freqs[9];
                  uint8_t	 ifreq = 9;
    

References
===================================================== 

https://www.thethingsnetwork.org/forum/t/big-esp32-sx127x-topic-part-1/10247/128

http://www.nicerf.com/product_180_241.html

