FROM docker.io/kalilinux/kali-rolling:latest
RUN apt update -y && apt install -y nmap
ENTRYPOINT ["/bin/nmap"]
