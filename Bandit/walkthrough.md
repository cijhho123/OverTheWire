## What is Bandit?

The Bandit wargame is a CTF aimed at absolute beginners. It will teach the basics needed to be able to play other wargames </br>
Link to the challenge: https://overthewire.org/wargames/bandit/

## Dev's note for new solvers

This game, like most other games, is organised in levels. You start at Level 0 and try to “beat” or “finish” it. Finishing a level results in information on how to start the next level. The pages on this website for “Level <X>” contain information on how to start level X from the previous level. E.g. The page for Level 1 has information on how to gain access from Level 0 to Level 1. All levels in this game have a page on this website, and they are all linked to from the sidemenu on the left of this page.
 
## Introduction
I am using an Ubuntu VM for the puzzle, and will save my terminal commands via </br>
``` history > history_for_print.txt ```

  
## Stage 0 
  The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1.
</br>
```ssh bandit0@bandit.labs.overthewire.org -p 2220``` </br>
are you sure you want to continue connecting (yes/no/[fingerprint])? </br>
```yes```</br>
</br>
## Stage 1


```
