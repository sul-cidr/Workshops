# Intro to Unix and Git for Academics
This is a very gentle introduction for non-programmers to the most basic, text-based 
ways to do things with a computer: the Unix (or Linux) command line.  Sometimes considered 
arcane, off-putting, or just old-fashioned, a bit of command line knowledge is still 
required for much digital humanities and social science work, even on a modern Mac or PC -- 
knowledge that is too often treated as implicit, but too seldom taught.  We will also 
cover the basics of Git, the near-universal version-control system that is one of basic 
toolkits of digital scholarship and especially collaboration. This workshop is a safe 
space for people of all experience levels, with no question too basic to ask!

Prerequisites: None.  Please bring your own computer.  It would be helpful before the 
class to create a free account on http://github.com if you don’t have one.

## Learning goals
* To understand what the command line is, and how it relates to our customary graphical user interfaces
* To understand files, directories, paths, commands, and how they interact 
* To become familiar with 10 Unix commands with their syntax
* To be introduced to 2 Unix programs (for editing text and transferring files)
* To become familiar with version control using Git

## Pre-workshop prep

### Windows: install Git Bash
[https://gitforwindows.org/]
which provides both a Unix-like shell and Git.

### Mac: install Git

## Unix: defining terms
- File
- Directory
- Path
- Command (or program)

### Unix syntax
A language analogy:

* `command` `[-option(s)]` `object1` `object2` 
* Verb  [Adverb]  DirectObject  IndirectObject

### A few essential Unix commands
`pwd`	

`ls`

`cp`

`mv`

`rm`

`cat`

`wc`

`grep`

`cd`

`./`

`../`

`mkdir`

`rmdir`

`|`

`>` `>>`

`man`

TAB completion

↑ command history

`ssh`

`sftp`
(plus commands within)

`vi`
(plus commands within)

## Git

### Why do we care about version control and git?

- Addresses issue of multiple versions and drafts of files
- Provides capacity to easily move between different versions of files (a la Google Sheets, but locally)
- Facilitates collaboration
- Facilitates backup and storage through remote repositories

### Conceptual model of git

- Local directory/working directory
- Staging area
- Git repository
- Remote repository

### Setting up git

- Installing
- Working with your git config
  - Username
  - Email

### Initializing a local git repository (`git init`)

### Telling git what to keep track of (`git add`)

### Telling git when to take a snapshot of your tracked files (`git commit`)

### Practice:

### Collaborating with git (fixing merge conflicts)

### Advanced collaboration (the branching model)
