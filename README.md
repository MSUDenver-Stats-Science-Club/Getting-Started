---
title: "How To Use Git"
author: "Jason Carey"
date: "10/12/2021"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Getting Started

In this document I'll explain what git is, I'm going to show you how to use git, and I'll discuss the benefits of using git when working in a team.

So what is git? Git is an open source, modern version control system that was developed in 2005 by Linus Torvalds (the same creator of the Linux OS). Git is used to track changes within development projects typically created by a team of developers. This system is extremely useful for tracking a project's development as it moves from a development environment to production (live for end-users).

### Installation

How can we get git? Luckily, git is very easy to install on any system. Simply navigate to [the git website](https://www.atlassian.com/git) to get started with downloading the software. You may be prompted based on the OS you have installed to download git from an external website that is linked to the main git website. On windows, for example you will be brought to [git for windows](https://gitforwindows.org/) to complete your download. Selecting the default options when installing git is recommended.

You will also need to create an account on GitHub in order to create your own repositories. Not to worry though, creating a GitHub account is really easy to do. Simply go to [GitHub](https://github.com) to get started with making an account. Once you have an account created we can get started with creating a repository. This repository will be our testing ground for pushing our code.

### Running Git Bash

At this point you may be asking yourself, how can I use git for a project that I'm working on, or a project I want to work on? You can do this a couple of different ways that I'll outline in the next sections, but first we need to make sure you're set up with the proper IDs that let git identify who is making the changes to the code. You can set these configs by using the following commands within the terminal:

1. `git config --global user.name "first last"`
2. `git config --global user.email "first.last@email.com"`

After these commands have been entered, git will now know that you are the person to be listed as making the changes to the code when pushing to a repository. This isn't the only way to identify yourself, however. You may also need a token or a key to authenticate yourself when making requests. For this walkthrough we'll keep it simple so you won't require a key or token.

## Git in the terminal

To use git from the terminal that comes with the software, simply search for 'git bash' in the start menu of your OS. Opening this program should result in a new window appearing with a line that shows your username for your machine, and the ID of your machine. From this point you can specify a directory to navigate to by typing in the command 'cd' (change directory).

Let's say that in this example I have a directory already created that contains a python script I wrote. I want to begin a new project using git so that I can make edits to this program from a location other than my computer where this work is saved locally or other individuals can make edits to my program so that it achieves what we want it to achieve. I can do that with git using the terminal to push my code into a public or private repository so that its stored in a centralized location.

You can do that by typing the following commands in this order:

1. `git init`
2. `git add <filename>` or `git add *`
3. `git commit -m 'Initial Commit'`
4. `git branch -M main`
4. `git remote add origin '<url>'`
5. `git push -u origin <branch>` or `git push origin main`

Now that you've executed these commands, refreshing your GitHub repository page should yield the changes you made to your program for the world to see.

## Git in R

Alternatively, you can also use R and the premier IDE for R, R Studio, to push your code into various repositories on GitHub. R Studio provides two options to push and pull your code. You can continue to use the terminal option, which is sometimes required to push an existing project into a repository, or you can use R Studio's GUI to perform the same actions without having to use the terminal. The GUI option provided by the IDE is more simplistic and its ideal for when you're creating markdown documents for business cases, EDAs, or homework. I'll walkthrough how you can use both.
