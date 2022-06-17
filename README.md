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


### Hardware used

|    |    |
|:--:|:--:|
| Raspberry Pi 3 Model B Rev 1.2 | USB RTL2832U R820T |
| <img src="https://user-images.githubusercontent.com/69190238/174204348-ebaf1cb6-6824-4da5-891c-67455d590673.png" height="256"/> | <img src="https://user-images.githubusercontent.com/69190238/174203308-132b86bd-e8dd-4970-8632-9a7aab74d853.png" height="256"/> |
| USB MSI2500 MSI001 | USB HackRF One |
| <img src="https://user-images.githubusercontent.com/69190238/174203616-3af67c7b-b81c-4928-b5fc-7c2f3af30489.png" height="256"/> | <img src="https://user-images.githubusercontent.com/69190238/174203750-e10e6d66-1bbe-45c6-8231-3a9901e7e1ed.png" height="256"/> |
