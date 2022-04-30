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
```ssh -p 2220 bandit0@bandit.labs.overthewire.org``` </br>
are you sure you want to continue connecting (yes/no/[fingerprint])? </br>
```yes```</br>
bandit0@bandit.labs.overthewire.org's password: 
>bandit0




## Stage 1
#### The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

```bandit0@bandit:~$ cat readme ```
>boJ9jbbUNNfktd78OOpsqOltutMc3MY1


## Stage 2
#### The password for the next level is stored in a file called - located in the home directory
```ssh -p 2220 bandit1@bandit.labs.overthewire.org``` </br>

```bandit1@bandit:~$ ls``` </br>
‌‌ - </br>
```bandit1@bandit:~$ cat ./-``` </br>
>CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9 </br>


## Stage 3
#### The password for the next level is stored in a file called spaces in this filename located in the home directory </br>
```ssh -p 2220 bandit2@bandit.labs.overthewire.org``` </br>

```bandit2@bandit:~$ ls```</br>
spaces in this filename </br>
```bandit2@bandit:~$ cat "spaces in this filename"``` </br>
>UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK


## Stage 4
#### The password for the next level is stored in a hidden file in the inhere directory.
```ssh -p 2220 bandit3@bandit.labs.overthewire.org```</br>

```bandit3@bandit:~$ dir```</br>
inhere  
```bandit3@bandit:~$ cd inhere/``` </br>

```bandit3@bandit:~/inhere$ ls -a``` </br>
.  ..  .hidden

```bandit3@bandit:~/inhere$ cat .hidden ``` </br>
>pIwrPrtPN36QITSp3EQaw936yaFoFgAB


## Stage 5
#### The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.
```ssh -p 2220 bandit4@bandit.labs.overthewire.org```</br>

```bandit4@bandit:~$ ls -a``` </br>
.  ..  .bash_logout  .bashrc  inhere  .profile </br>
```bandit4@bandit:~$ cd inhere/``` </br>
```bandit4@bandit:~/inhere$ grep -iRl ^[a-zA-Z0-9_.-]*$ ./``` </br>
./-file07 </br>
```bandit4@bandit:~/inhere$ cat ./-file07``` </br>
>koReBOKuIDDepwhWk7jZC0RTdopnAYKh


## Stage 6
#### The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:</br> human-readable </br>1033 bytes in size </br>not executable

```ssh -p 2220 bandit5@bandit.labs.overthewire.org```</br>

```bandit5@bandit:~$ ls```</br>
inhere      </br>
```bandit5@bandit:~$ cd inhere/```  </br>
```bandit5@bandit:~/inhere$ ls -a```    </br>
.            maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
..           maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
</br>
```bandit5@bandit:~/inhere$ find -readable -size 1033c -type f ! -executable``` </br>
./maybehere07/.file2 </br>
```bandit5@bandit:~/inhere$ cat ./maybehere07/.file2``` </br>
>DXjZPULLxYr17uwoI01bNLQbtFemEgo7

## Stage 7
#### The password for the next level is stored somewhere on the server and has all of the following properties:</br>owned by user bandit7 </br>owned by group bandit6 </br>33 bytes in size

```ssh -p 2220 bandit6@bandit.labs.overthewire.org```</br>

```bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null```</br>
/var/lib/dpkg/info/bandit7.password  </br>

```bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password``` </br>
>HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs


## Stage 8
#### The password for the next level is stored in the file data.txt next to the word millionth
```ssh -p 2220 bandit7@bandit.labs.overthewire.org```</br>

```bandit7@bandit:~$ ls -a```</br>
.  ..  .bash_logout  .bashrc  data.txt  .profile</br>
```bandit7@bandit:~$ grep "millionth" data.txt ```</br>
millionth	cvX2JJa4CFALtqS87jk27qwqGhBM9plV</br>
>cvX2JJa4CFALtqS87jk27qwqGhBM9plV

## Stage 9
#### The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

```ssh -p 2220 bandit8@bandit.labs.overthewire.org```

```bandit8@bandit:~$ ls -a```   </br>
.  ..  .bash_logout  .bashrc  data.txt  .profile

```bandit8@bandit:~$ cat data.txt | sort | uniq -c | sort -r | head -1```   </br>
      1 UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
>UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
