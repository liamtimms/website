---
title: Software I find useful in my daily life
---

This website was written in `markdown` using `neovim` on Arch Linux and converted to html with `pandoc`. I'll cover these tools, and others, on this page.

## Linux Distributions

### Linux Mint

A great distro for new linux users, this is based on Ubuntu's Long Term Support release but has additional tools to help guide new users and run smoothly without the need for detailed configurations. Ubuntu has the largest linux desktop community which leads to lots of online help and official support which is nearly always equally applicable to Mint. Valuing stability over new feature updates, this works well for someone who just wants their machine to work and doesn't care if they don't have the latest features of every program.

DE: Cinnamon

### Arch Linux

Almost the opposite philosophy from Mint, this distro is all about setting up a bleeding-edge system from the ground up for an individual's preferences. Rather than maintaining a long supported stable system of increasingly old programs, it is constantly updating, keeping pace with most new software releases directly from the developers. Arch Linux makes sharing software very easy by allowing anyone to contribute packaging scripts to the Arch User Repository. I have found this particularly useful for neuroimaging programs which are almost all under active development by other researchers and academics. Using Arch as my platform for my own analysis development allows me to keep up with important features from the neuroimaging in an integrated and automated way.

My favorite DE: GNOME 3.38

### Debian

Rock-solid. Free software. "The universal operating system." It's Debian. Great for servers and a good base for reproducible research. I'm running this site on a Debian server. However, the slow update cycle and focus on servers over desktop users makes it frustrating for standard desktop use in my experience.

DE: I don't have one on my install

## Terminal Applications

### Neovim

Vim is a decades old text editor program with an absolutely brilliant built in language for manipulating text. Neovim is a refactored and modernized version which is adding new features. Vim/neovim have many powerful extensions available letting you do everything from compiling LaTeX documents live as they are edited to automatically formatting Python code, the program itself is language agnostic so you don't get caught up in the particularities of word processes, IDEs and GUI text editors. If it involves manipulating words on a screen, there's no better tool invented. You can see my personal configuration/plugins here: https://raw.githubusercontent.com/liamtimms/configs/master/.config/nvim/init.vim

If you aren't sold on it, this famous stackoverflow answer gives a basic overview: https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118

### Pandoc

An _absurdly_ powerful little program for converting between document types. I use it often as it allows one to write quickly in the simple language of Markdown and then generate pdfs (via LaTeX), slide shows, or html for websites (like this whole site!).

**Example:** `pandoc [inputfilename.md] -o [outputfilename.pdf]`

## Python Libraries

### The Nipy Neuroimaging Python Suite

### Pandas

### Seaborn

### Scikit Image

## Research Tools

### Zotero

I used to recommend Mendeley as a way to manage one's library of scientific literature but recent releases have become extremely buggy for large libraries and the company behind the program is increasingly hostile to users and have started trying to lock down one's library with encryption. Encryption is often useful to users but here is is ued only to limit user freedom to switch platforms. I currently believe Zotero is a much better long term option.

Make sure you install and set-up the ZotFile extension.

### Jupyter-lab

## General Utilities

### Zathura

Not scientific software specifically but scientific papers are generally available in pdf format and this is a super fast and simple pdf reader which I use daily. `ctrl+r` inverts colors.

### fzf

### ssh

Let's you interact with a machine remotely.

### ssh + tmux

### ranger
