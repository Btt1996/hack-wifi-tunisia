# hack-wifi-tunisia
ooredooand orange tunisia  routers are vulnerable to weak cipher attacks. It is possible to generate the default WEP/WPA key of Huawei HG520 routers. The purpose of this document is to explain the process of developing a key generator for these devices.     Huawei router models HG520b and HG520c contain a key generator command (mac2wepkey) in their TELNET interface. They also contain a command to change the MAC address (fakemac).   

It is possible to change our MAC to generate the default WEP key of a MAC of our choosing.   
This is the list for the first position of the MAC address (Ex. 52:00:00:00:00:00) the value is 5 so we will use the values in position 6 of the list:

SSID-A [0, 14, 10, 4, 8, 6, 2, 12, 0, 14, 10, 4, 8, 6, 2, 12]

SSID-B [0, 8, 0, 8, 3, 11, 3, 11, 6, 14, 6, 14, 5, 13, 5, 13]

SSID-C [0, 0, 3, 3, 2, 2, 1, 1, 4, 4, 7, 7, 6, 6, 5, 5]

SSID-D [0, 11, 12, 7, 15, 4, 3, 8, 14, 5, 2, 9, 1, 10, 13, 6]

WEP-A [0, 13, 10, 7, 5, 8, 15, 2, 10, 7, 0, 13, 15, 2, 5, 8]

WEP-B [0, 5, 1, 4, 6, 3, 7, 2, 12, 9, 13, 8, 10, 15, 11, 14]

WEP-C [0, 1, 3, 2, 7, 6, 4, 5, 15, 14, 12, 13, 8, 9, 11, 10]

WEP-D [0, 14, 4, 10, 11, 5, 15, 1, 6, 8, 2, 12, 13, 3, 9, 7]

WEP-E [0, 9, 0, 9, 5, 12, 5, 12, 10, 3, 10, 3, 15, 6, 15, 6]
This is the list for the first position of the MAC address (Ex. 52:00:00:00:00:00) the value is 5 so we will use the values in position 6 of the list:

SSID-A [0, 14, 10, 4, 8, 6, 2, 12, 0, 14, 10, 4, 8, 6, 2, 12]

SSID-B [0, 8, 0, 8, 3, 11, 3, 11, 6, 14, 6, 14, 5, 13, 5, 13]

SSID-C [0, 0, 3, 3, 2, 2, 1, 1, 4, 4, 7, 7, 6, 6, 5, 5]

SSID-D [0, 11, 12, 7, 15, 4, 3, 8, 14, 5, 2, 9, 1, 10, 13, 6]

WEP-A [0, 13, 10, 7, 5, 8, 15, 2, 10, 7, 0, 13, 15, 2, 5, 8]

WEP-B [0, 5, 1, 4, 6, 3, 7, 2, 12, 9, 13, 8, 10, 15, 11, 14]

WEP-C [0, 1, 3, 2, 7, 6, 4, 5, 15, 14, 12, 13, 8, 9, 11, 10]

WEP-D [0, 14, 4, 10, 11, 5, 15, 1, 6, 8, 2, 12, 13, 3, 9, 7]

WEP-E [0, 9, 0, 9, 5, 12, 5, 12, 10, 3, 10, 3, 15, 6, 15, 6]

 

The following list is for the second position of the MAC address (Ex. 52:00:00:00:00:00) the value is 2 so we will use the values of position 3 in the list:

SSID-A [0, 5, 11, 14, 7, 2, 12, 9, 15, 10, 4, 1, 8, 13, 3, 6]

SSID-B [0, 5, 11, 14, 2, 7, 9, 12, 12, 9, 7, 2, 14, 11, 5, 0]

SSID-C [0, 0, 0, 0, 4, 4, 4, 4, 0, 0, 0, 0, 4, 4, 4, 4]

SSID-D [0, 8, 1, 9, 3, 11, 2, 10, 5, 13, 4, 12, 6, 14, 7, 15]

WEP-A [0, 14, 13, 3, 9, 7, 4, 10, 6, 8, 11, 5, 15, 1, 2, 12]

WEP-B [0, 13, 10, 7, 4, 9, 14, 3, 10, 7, 0, 13, 14, 3, 4, 9]

WEP-C [0, 4, 8, 12, 0, 4, 8, 12, 0, 4, 8, 12, 0, 4, 8, 12]

WEP-D [0, 1, 3, 2, 6, 7, 5, 4, 15, 14, 12, 13, 9, 8, 10, 11]

WEP-E[0, 1, 3, 2, 4, 5, 7, 6, 12, 13, 15, 14, 8, 9, 11, 10]

 

All other positions have the value 0. This value corresponds to 0 in every other list, so the final equation for the first byte of the SSID is the following:

6^11^0^0^0^0^0^0^0^0^0^0^(5 base)= 8            
[SSID=8A9F]

 

From the 108 lists we generated, there are 16 lists that are repeated that we will note with the letter A (A1, A2, A3...) and 33 lists that are never repeated that we will note with the letter N (N1, N2...). This totals 49 unique lists.

 


