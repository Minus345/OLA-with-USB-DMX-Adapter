
# OLA-with-USB-DMX-Adapter

Adapter:  
https://www.amazon.de/-/en/RS485-Adapter-Lighting-Control-Cable-black/dp/B07WV6P5W6/ref=cm_cr_arp_d_product_top?ie=UTF8

Comment:  
https://www.amazon.de/-/en/RS485-Adapter-Lighting-Control-Cable-black/product-reviews/B07WV6P5W6/ref=cm_cr_dp_d_show_all_btm?ie=UTF8&reviewerType=all_reviews


## Documentation

Install Ola on Raspberry Pi:  

`sudo apt install ola`  

Udev Rul:  

`/etc/udev/rules.d/dmx.rules`  

`SUBSYSTEM=="usb|usb_device", ACTION=="add", ATTRS{idVendor}=="0403", ATTRS{idProduct}=="6001", GROUP="plugdev"`

Configure:

In `/etc/ola/ola-ftdidmx.conf` - `enabled = true`  

In `/etc/ola/ola-opendmx.conf` - `enabled = false`  

In `/etc/ola/ola-usbserial.conf` - `enabled = false`  

Restart Ola:

`systemctl stop olad.servic`  

`systemctl start olad.servic` 

Connect to Website:

`http:// [ipRaspberry]:9090`

-> Create Universe

