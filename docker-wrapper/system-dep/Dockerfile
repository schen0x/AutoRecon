# The system dependencies layer
# sudo docker build -t autorecon/dep .

# FROM kalilinux/kali-bleeding-edge:latest AS builder
FROM kalilinux/kali AS builder
RUN apt-get update
RUN apt-get -y install sudo git
RUN sudo apt-get -y install python3 python3-pip
RUN sudo apt-get -y install seclists curl enum4linux nbtscan nikto nmap onesixtyone oscanner smbclient smbmap snmp sslscan sipvicious tnscmd10g whatweb wkhtmltopdf
RUN sudo apt-get -y install feroxbuster impacket-scripts redis-tools
RUN apt-get -y autoremove && apt-get -y autoclean