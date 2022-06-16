# RaspberryPi-SDR
Raspberry Pi usage for Software Defined Radio.

**Raspberry Pi base setup**
* Install Raspberry Pi OS Lite on the SD card using Raspberry Pi Imager
  * Set hostname
  * Enable SSH
  * Set username and password
  * Configure WiFi
* Set a static ip
  * edit /etc/dhcpcd.conf
  * add static ip configuration 
    ```
    interface wlan0
    static ip_address=192.168.1.180/24
    static routers=192.168.1.1
    static domain_name_servers=192.168.1.1
    ```

