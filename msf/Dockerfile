FROM docker.io/kalilinux/kali-rolling:latest
RUN apt update -y && apt install -y metasploit-framework && apt-get clean
RUN service postgresql start && msfdb init
CMD ["msfconsole"]
