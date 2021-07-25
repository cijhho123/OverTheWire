![logo](assets/logo.jpg)

My solutions for the OverTheWire community practices:  https://overthewire.org/wargames/

## What is Over The Wire?

OverTheWire offer a collection of wargames that are designed to help you learn and practice security concepts in addition to fostering and exercising a particular way of thinking. Thinking outside of the box is, inarguably, a hacker or coders most powerful ability. There are a million-and-one scripts and other tools out there and all of them are extremely easy to use in comparison to developing this ability. Even if you have the knowledge to write them yourself you will still need the requisite street-smarts to achieve the desired outcome. Developing this mindset will aid you in problem-solving for the rest of your life.

## Baby steps
OverTheWire's first wargame titled 'Bandit' is aimed at absolute beginners. It will teach you the basics you will need to know in order to engage with their other wargames which increase in difficulty as you move up the levels. Bandit will teach you about using a Linux shell, remote connections, and SSH (secure shell). If you are unfamiliar with SSH I will provide a very brief explanation. The first iteration of SSH (SSH-1) was developed by Tatu Ylönen at Helsinki University of Technology. It's creation was prompted by a password-sniffing attack on the university network. SSH is a cryptographic network protocol for operating network services securely over an unsecured network. This is typically things like remote command-line, login, and remote command execution. Any network service can be secured with SSH. It was designed as a replacement for Telnet and other (insecure) remote shell protocols. Prior to SSH those protocols sent information (like passwords) in plain text which rendered them susceptible to interception through packet analysis. Will packet analysis be a future blog post? Who knows.

## The Progress
The games at OverTheWire are organized into levels and it is intended for you to complete the previous level before advancing. Unlike 'red team vs blue team' hacking CTF (capture the flag) matches, the OverTheWire wargame suite is played solo so there is a lot less 'organizational overhead' needed to get things started. Real friends are overrated anyway. Everyone knows from Mr. Robot that the super-leet have imaginary ones. Spoiler alert.

Bandit currently has 34 levels. The suggested order to play the games is to start there at level 0, then once you have worked through it move on to either Leviathan, Natas, or Krypton. After that they suggest Narnia, Behemoth, Utumno, and Maze in that order. There are also Vortex, Semtex, Manpage, and Drifter. 

* Bandit is designed to familiarize the user with the command-line and SSH and set you up with some of the skills necessary for the later games. 
* In Narnia the user is familiarized with basic exploitation. You are provided with the source code of each level in Narnia to make it easier to find the vulnerabilities. 
* Behemoth deals with common coding mistakes such as buffer overflows, race conditions, and privilege escalation. Most of the beginner games do not require previous coding experience, but it will certainly become useful as you advance. 

* Each shell game has its own SSH port and these wargames are a great way to familiarize oneself with the command-line and general concepts of network security.

## Getting started
To get started with 'Bandit' you will need SSH. The host is bandit.labs.overthewire.org on port 2220 with a login and password of bandit0. You can connect through the command-line with:

ssh -l bandit0 -p 2220 bandit.labs.overthewire.org
For Ubuntu users you can install the SSH server with:
sudo apt update
sudo apt upgrade
sudo apt install openssh-server
For Windows (non-WSL) users you will need to download PuTTY here:
https://www.putty.org

OverTheWire also uses a scoreboard invoked by the wechall command in the SSH shell. It is provided by WeChall at https://www.wechall.net. To use the scoreboard go to the WeChall website and register for an account. Go to Account then WarBoxes to get your token. Edit your ~/.bashrc adding:

export WECHALLUSER="YourUserName"
export WECHALLTOKEN="YOUR-WECHALL-TOKEN-HERE"
Next, edit your ~/.ssh/config and add:

Host *.labs.overthewire.org
SendEnv WECHALLTOKEN
SendEnv WECHALLUSER
Additional information:
https://overthewire.org/wargames/


## My Solutions
[1. Bandit](/Bandit)<br/>
Natas <br/>
Leviathan <br/>
Krypton <br/>
Narnia <br/>
Behemoth <br/>
Utumno <br/>
Maze <br/>


