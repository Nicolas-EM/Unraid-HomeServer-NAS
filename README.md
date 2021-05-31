# Unraid HomeServer / NAS
## Hardware :computer:
Chosen with the help of r/CabaloftheBuildsmiths

Hardware | Part
------------ | -------------
CPU | Intel Core i5-11400 2.6 GHz 6-Core Processor
Motherboard | ASRock B560M-ITX/ac Mini ITX LGA1200 Motherboard
Memory | Corsair Vengeance LPX 16 GB (2 x 8 GB) DDR4-3600 CL19 Memory
Storage (HDD) | Seagate EXOS Enterprise 8 TB 3.5" 7200RPM Internal Hard Drive x 3
Storage (SSD) | Crucial P2 500 GB M.2-2280 NVME Solid State Drive
Case | Cooler Master Elite 130 Mini ITX Tower Case
PSU | be quiet! Pure Power 11 400 W 80+ Gold Certified ATX Power Supply

Storage | Use |
------------ | -------------
8TB HDD x 2 | Storage
8TB HDD | Parity Drive
500GB SSD | Cache

Mini ITX was chosen due to my current living situation, and as I had never built a Mini ITX PC I had some initial trouble dealing with the case size.
After using the server for a couple of days I realized the case-included CoolerMaster fans and stock Intel CPU cooler were insufficent for cooling.
The resulting cooling setup is:
Type | Cooling
------------ | -------------
CPU Cooler | Noctua NH-L9x65 
Front Fan | Noctua NF-F12 PWM (120 mm)
Side Fan | Noctua NF-A8 ULN (80 mm)

## Unraid Setup
### Docker Containers
* Media Server :movie_camera:
 * binhex-delugevpn - Torrent downloader with Private Internet Access
 * binhex-jackett - Indexer manager
 * binhex-nzbhydra2 - NZB indexer
 * binhex-plex - Media streaming platform
 * binhex-radarr - Movie tracker
 * binhex-sonarr - TV Show tracker
 * requestrr - discord bot for media requests
* Books :books:
 * calibre -  E-book manager
 * calibre web - Web app for calibre
 * readarr - Ebook tracker
* Cloud storage :floppy_disk:
 * mariadb - Relational database back-end
 * nextcloud - Front-end
* File backup
 * Syncthing - File synchronization
* Remote access
 * Namecheap-DDNS - Updates namecheap domain dynamic ip
 * swag - Secure Web Application Gateway, Nginx webserver and reverse proxy
* Other
 * pihole template - Pihole DNS for network wide adblocking
 * binhex-minecraftbedrockserver - Minecraft bedrock server
 * mealie - Recipe manager and meal planner

### Applications / Plugins
Only including most significant ones
* Community Applications - Unraid "app store"
* Appdata Cleanup - Unused data deletion
* Dynamix S3 Sleep - S3 Sleep config to reduce energy usage
* Dyanmix Wireguard - Remote tunneled access to Server LAN
* ProFTPd - FTP access manager

### VM's
#### OS's
* Windows 10
* Ubuntu - Dev environment
#### Notes
Due to the current GPU market, I was unable to acquire a GPU, limiting my use of VM's for daily drivers (and media encoding).
See Project Roadmap

### Security Measures :closed_lock_with_key:
* Disabled Telenet
* Secure remote access (ProFTPd, Root password, etc...)
* Restricted share acceess

## Skills Used / Learned
* LAN/WAN Security Practices
* DNS Setup (CNAME, DDNS, etc...)
* Port Forwarding
* Dockerized applications

## Project Roadmap
### Future upgrades
* GPU Installation - Once the GPU market stabilizes, a GPU will be used for VM's and media encoding
* Case upgrade - Hoping to upgrade case to ATX for better cooling, possible storage expansion
* Mail Server - Will possibly implement a mail server for custom domain mail
