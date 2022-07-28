FROM docker.io/kalilinux/kali-rolling:latest
RUN apt update -y && apt install -y nmap && apt-get clean
ENTRYPOINT ["/bin/nmap"]
