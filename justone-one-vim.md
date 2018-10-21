# One Vim

Pulling from my [presentation](https://github.com/justone/one_vim_present).

# High level outline

* Rationale
  * efficiency
  * proximity
  * reference
  * refactoring
* Starting off
  * splits
  * tabs
* Deeper dive
  * finding files
  * editing neighbors
  * adding files from other shells
* Buffer management
  * built ins
  * helpful plugins
  * saving your spot
* Bonus plugins
  * taboo

# Draft

## Introduction

Vim is a powerful editor.  But like many powerful things, sometimes it can be used in less-than-powerful ways.  Do you edit files one at a time?  Do you find yourself bouncing between vim and the terminal to find files?

I am a big fan of using a single instance of Vim, typically scoped to the project (or repository) level.

I've used Vim for more than 20 years, and I've also watched many other people use it.  I've seen people quit vim between each edit and cringed at the lost power that so quickly is dispensed with.

Editing multiple files simultaneously has many benefits.

First, it dispenses with the overhead of startup time and finding the right place in the file.  This usually isn't a lot of time, but it can add up as you flip between different files.

The second benefit has to do with the locality and impact of your edits.  When you start a task that involves editing a single file, it's likely that you will need to edit other files as well.  They could be a reference, or a place to copy information from.  When working in software, it's common to move lines of code between files when doing a refactor. Non software tasks benefit from this as well.  For instance, when editing a file in `/etc/cron.d/`, it might be useful to check a neighbor file to see how its cron expression is constructed. The point is that rarely do files truly stand alone.

A third benefit is that once you have the three or four (or twenty) files open, you can leverage Vim's built-in session saving ability to take that entire set up and save it for later.  This is particularly useful when switching between tasks in a software project.  You can save the editing session for one branch while that code is in review, and start an entirely different task with its own constellation of files.  Then, when you need to make changes in response to the review, you can load up the previous session and get right back to where you were.

There are other benefits as you progress further down the road, but those are a good place to start.

## Structure

This post is written so that you can stop at any time and take what you've learned and that will be sufficient.  You do not need to read and implement the entire content in order to receive any benefit.  On the contrary, the best way to incorporate these (or any tutorial/learning tasks) is to take an incremental approach.  Choose a small amount of information or technique that you can integrate into your workflow, and then use it for a while.  Once it has become integrated, move on to the next section and integrate again.

Don't be frustrated when this information feels like it slows you down.  Remember the phrase "Slow is smooth, and smooth is fast".  Adding a second file to your current Vim session will be slower than quitting your existing session, but overall your productivity will increase.  Take your time and do the motions correctly.  As your muscle memory grows, you will be able to add more files so quickly that you will outpace any former technique.

## Preparation

To give you a known playground, I've prepared a git repository, that you can get one of two ways:

1. Clone it: `git clone https://github.com/justone/2018-one-vim-playground.git`.
2. Download it: `curl https://github.com/justone/2018-one-vim-playground/archive/master.tar.gz | tar -xzvf -`

Either way, you should have a directory in which to try out the following.

## From one to two

The first step is opening just one more file.  Open a single file in Vim, and then run one of the following:

```
:sp <file2>
:vsp <file2>
:tabe <file2>
```

Those will open the file in a horizontal split, vertical split, or a new tab, respectively.

# Ideas for interaction

* Have a git repo to clone, with a tree of files to practice on.
