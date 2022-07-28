FROM docker.io/kalilinux/kali-rolling:latest
RUN apt update -y && apt install -y john wordlists && apt-get clean
ENTRYPOINT ["/usr/sbin/john"]
