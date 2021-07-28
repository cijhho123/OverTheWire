## What is Bandit?

The Bandit wargame is a CTF aimed at absolute beginners. It will teach the basics needed to be able to play other wargames </br>
Link to the challenge: https://overthewire.org/wargames/bandit/

## Dev's note for new solvers

This game, like most other games, is organised in levels. You start at Level 0 and try to “beat” or “finish” it. Finishing a level results in information on how to start the next level. The pages on this website for “Level <X>” contain information on how to start level X from the previous level. E.g. The page for Level 1 has information on how to gain access from Level 0 to Level 1. All levels in this game have a page on this website, and they are all linked to from the sidemenu on the left of this page.
 
## Introduction
I am using an Ubuntu VM for the puzzle, and will mark my terminal commands via </br>
``` CODE ``` </br>
and will mark passwords with 
>PASSWORD

  
## Stage 0 
#### The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.
```ssh bandit0@bandit.labs.overthewire.org -p 2220``` </br>
are you sure you want to continue connecting (yes/no/[fingerprint])? </br>
```yes```</br>


## Stage 1
#### The password for the next level is stored in a file called - located in the home directory</br>
```bandit0@bandit:~$ ls ``` </br>
readme </br>
```bandit0@bandit:~$ cat readme ``` </br>
>boJ9jbbUNNfktd78OOpsqOltutMc3MY1 </br>


## Stage 2
#### The password for the next level is stored in a file called spaces in this filename located in the home directory </br>
```bandit1@bandit:~$ ls``` </br>
‌‌ - </br>
```bandit1@bandit:~$ cat /-``` </br>
cat: /-: No such file or directory </br>
```bandit1@bandit:~$ cat ./-``` </br>
>CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9 </br>


## Stage 3
#### The password for the next level is stored in a file called spaces in this filename located in the home directory </br>
```bandit2@bandit:~$ ls```\
spaces in this filename\
```bandit2@bandit:~$ cat "spaces in this filename"```
>UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK


## stage 4
#### The password for the next level is stored in a hidden file in the inhere directory.
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden 
>pIwrPrtPN36QITSp3EQaw936yaFoFgAB



```
