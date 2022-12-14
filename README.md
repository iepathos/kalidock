kalidock
-----

## Kali Linux docker wrapper environment


Bunch of scripts and docker setups to containerize various kali tooling for a cross-platform pentesting environment.

Some limitations with this approach especially if you need to run some password cracking that takes advantage of GPU acceleration.  I have seen implementations using nvidia-docker which you can try if you're using an nvidia GPU.

Developed by Glen Baker <iepathos@gmail.com> for personal use


# VPN

Copy openvpn profile to vpn.ovpn, it will be mounted into the vpn client container and networked with the interactive kali container.  Good practice to run behind a vpn, can modify the docker-compose.yml to avoid running the vpn container.


# Tools and Usage

Needs to be ran once `./create-volumes.sh`

## Interactive Kali Shell

Enter an interactive kali container with a bunch of default tools installed for general working environment.  Put any files you need to pass into the container into the `in` directory.

`./enter.sh`

## Nmap

`docker-compose run nmap *args*`

## John The Ripper

Move the input for John into the `in` directory.

`docker-compose run john --wordlist=/usr/share/wordlists/john.lst `

## Metasploit

`docker-compose run msf`
