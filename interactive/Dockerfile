FROM docker.io/kalilinux/kali-rolling:latest
RUN apt update -y && apt install -y nmap john wordlists metasploit-framework nikto iputils-ping dnsutils vim && apt-get clean
RUN service postgresql start && msfdb init

# just keep container running if ran with docker-compose up
ENTRYPOINT ["tail", "-f", "/dev/null"]
