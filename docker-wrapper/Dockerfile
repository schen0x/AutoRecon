#sudo docker build -t tib3rius/autorecon .
#mkdir /home/kali/autorecon
#Usage: sudo docker run -it -v /home/kali/autorecon:/results --rm --name autorecon-container tib3rius/autorecon 127.0.0.1 127.0.0.2
#Peek: find /home/kali/autorecon -name _full_tcp_nmap.txt | xargs cat

FROM autorecon/dep
RUN python3 -m pip install --user pipx
RUN python3 -m pipx ensurepath
RUN python3 -m pip install git+https://github.com/schen0x/AutoRecon.git
RUN echo "Defaults	secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/kali/.local/bin"" >> /etc/sudoers
ENTRYPOINT ["autorecon"]