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
* Update / Upgrade
  * sudo apt update
  * sudo apt upgrade


**RTL-SDR server**
* Install
  * `sudo apt-get install rtl-sdr`
* Test
  * `rtl_test -t`
* Run server
  * `rtl_tcp -a 192.168.1.180`

**SpyServer**
* Install
  * `sudo apt-get install librtlsdr-dev
  * `wget -O spyserver-arm32.tgz http://airspy.com/?ddownload=4247`
    *  link may change : [airspy.com/download](https://airspy.com/download/) : SPY Server – SDR Server for Linux ARMHF
  * tar xvzf spyserver-arm32.tgz
* Configuration
  * edit spyserver.config, change device_type to RTL-SDR
* Run server
  * `./spyserver`


