# bitmonero.conf Guide

see video for walkthrough: 


## 1. Install GUI or CLI.

https://www.getmonero.org/downloads/



  
## 2. install tor 

sudo apt install tor

 
## 3. edit /etc/tor/torrc file so it shows:


HiddenServiceDir /var/lib/tor/monero-rpc/

HiddenServicePort 18089 127.0.0.1:18089

HiddenServiceDir /var/lib/tor/monero-p2p/

HiddenServicePort 18084 127.0.0.1:18084



## 4. make sure tor is enabled and active

sudo systemctl tor restart


## 5. get onion links for p2p and rpc

sudo cat /var/lib/tor/monero-p2p/hostname

sudo cat /var/lib/tor/monero-rpc/hostname



## 6. Download Monero ban_list and place in Monero folder with monerod:

https://github.com/Boog900/monero-ban-list/blob/main/ban_list.txt


## 7. Place bitmonero.conf inside ~/.bitmonero

Download bitmonero.conf txt file from github and find hidden directory. On linux, this is in the home folder. 


## 8. Add p2p onion link in anonymous inbound

Insert p2p onion link after anonymous-inbound=

