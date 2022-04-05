---
title: Software I find useful in my daily life
---

This website was written in `markdown` using `neovim` on Arch Linux and converted to html with `pandoc`. I'll cover these tools, and others, on this page.

## Linux Distributions

### Linux Mint

A great distribution (distro) for new Linux users, this is based on Ubuntu's Long Term Support release but has additional tools to help guide new users and run smoothly without the need for detailed configurations. Ubuntu has the largest Linux desktop community which leads to lots of online help and official support which is nearly always equally applicable to Mint. Valuing stability over new feature updates, this works well for someone who just wants their machine to work and doesn't care if they don't have the latest features of every program.

DE: Cinnamon

[Install guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/)

### Arch Linux

Almost the opposite philosophy from Mint, this distro is all about setting up a bleeding-edge system from the ground up for an individual's preferences. Rather than maintaining a long supported stable system of increasingly old programs, it is constantly updating, keeping pace with most new software releases directly from the developers. Arch Linux makes sharing software very easy by allowing anyone to contribute packaging scripts to the Arch User Repository. I have found this particularly useful for neuroimaging programs which are almost all under active development by other researchers and academics. Using Arch as my platform for my own analysis development allows me to keep up with important features from the neuroimaging in an integrated and automated way.

My favorite DE: GNOME 3.38

[Install guide](https://wiki.archlinux.org/title/installation_guide)

### Debian

Rock-solid. Free software. "The universal operating system." It's Debian. Great for servers and a good base for reproducible research. I'm running this site on a Debian server. However, the slow update cycle and focus on servers over desktop users makes it frustrating for standard desktop use in my experience. I didn't have to do any manual setup for installing it and let my VPS take care of the initial setup automatically.

DE: I don't have one on my install (headless server)

## Terminal Applications

I prefer to use terminal applications when possible. While it might sound surprising, this is actually a practical decision for a few reasons:

1. In scientific contexts, a lot of software is developed without GUI front ends. This means using the terminal is unavoidable. Embracing this increases comfort when using these programs and comfort/familiarity makes the inevitable debugging easier.
2. The primary way humans communicate technical ideas and instructions is via text. The terminal is a mostly text-based interface. It does not make sense to use it for inherently graphical tasks like photo-editing but for anything text oriented it is simple and elegant.
3. Using text based commands to deal with tasks enables immediate automation or recall of those tasks if they ever have to performed more than once.
4. A good terminal emulator has imperceptible input and output lag.
5. Terminal applications can be run remotely without any perceptible delay through `ssh`. You can easily instantly utilize the full power of a personal or cloud machine remotely.
6. The most powerful input device at your computer is still the keyboard. Terminal applications allow you to take full advantage of this and minimize the amount of time you spend switching device and context between keyboard, mouse, touch-screen or voice-command.
7. `tmux-ressurect` minimizes the disruption from working remotely or setting whole workspaces after rebooting. You never need to leave your spot in whole set of open files.

### Neovim

`Vim` is a decades old text editor program with an absolutely brilliant built in language for manipulating text. Neovim (`nvim`) is a refactored and modernized version which is adding new features. Vim/neovim have many powerful extensions available letting you do everything from compiling LaTeX documents live as they are edited to automatically formatting Python code, the program itself is language agnostic so you don't get caught up in the particularities of word processes, IDEs and GUI text editors. If it involves manipulating words on a screen, there's no better tool invented. I use it for coding, writing papers, taking notes, creating this website, etc. You can see my personal configuration/plug-ins here: https://raw.githubusercontent.com/liamtimms/configs/master/.config/nvim/init.vim

If you aren't sold on it, this famous Stack Overflow answer expresses it well: https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118

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

I used to recommend Mendeley as THE way to manage one's library of scientific literature but recent releases have become extremely buggy for large libraries (I have lost papers without even knowing until later) and the company behind the program is increasingly hostile to users and have started trying to lock down one's library with encryption. Encryption is extremely useful in the hands of users but here it is in the hands of the company and used to limit user freedom to switch platforms. I currently believe Zotero is a better long term option.

Recommend using the ZotFile extension to place literature pdfs into a folder synced between your machines.

### Jupyter-lab

In my opinion, jupyter-notebooks suck for any really in-depth work but they perfect for initially iterating on figures, exploring data and prototyping analysis. Jupyter-lab is a very useful tool for exploring scientific data for this reason.

## General Utilities

### Zathura

Not scientific software specifically but scientific papers are generally available in pdf format and this is a super fast and simple pdf reader which I use daily. I use it because it is perfectly setup with `vim`-style key-bindings out of the box.

### ssh

Breaks down the physical barriers to working on your machine from anywhere.

### ssh + tmux

This is an important combination.

### ranger

File-manager in the terminal.

### fzf

Instant access.
