---
title: Software I find helpful in my daily life
---

This website was written in `markdown` using `neovim` on Arch Linux and converted to HTML with `pandoc`. I'll cover these tools, and others, on this page. The page is organized in order of most to least broad recommendation (I strongly recommend each of these tools, but not all will apply to every user).

## Terminal Applications

I prefer to use terminal applications when possible. While it might sound surprising, this is a practical decision for a few reasons:

1. In scientific contexts, a lot of software is developed without GUI front ends. Therefore, using the terminal is unavoidable. Embracing this fact increases comfort when using these programs, and comfort/familiarity makes the inevitable debugging easier.
2. Humans primarily communicate technical ideas and instructions via text. The terminal is a mostly text-based interface. It does not make sense to use it for inherently graphical tasks like photo-editing, but it is simple and elegant for anything text-oriented.
3. Using text-based commands to deal with tasks enables immediate automation or recall of those tasks if they are performed more than once.
4. A good terminal emulator has imperceptible input and output lag.
5. Terminal applications can be run remotely without perceptible delay through `ssh`. You can efficiently and instantly utilize the full power of a personal or cloud machine remotely.
6. The most powerful input device on your computer is still the keyboard. Terminal applications allow you to take full advantage of this and minimize the time you spend switching device and context between keyboard, mouse, touch-screen, or voice command.
7. `tmux-resurrect` minimizes the disruption from working remotely or setting whole workspaces after rebooting. You never need to leave your spot in an entire set of open files.

### Neovim

`Vim` is a decades-old text editor program with a brilliant built-in language for manipulating text. Neovim (`nvim`) is a refactored and modernized version that adds new features. Vim/neovim has many powerful extensions, letting you do everything from compiling LaTeX documents live as they are edited to automatically formatting Python code. The program is language-agnostic, so you don't get caught up in the particularities of word processes, IDEs, and GUI text editors. If it involves manipulating words on a screen, there's no better tool invented. I use it for coding, writing papers, taking notes, creating this website, etc. You can see my configuration/plug-ins [here.](https://raw.githubusercontent.com/liamtimms/configs/master/.config/nvim/init.vim)

If you aren't sold on it, this famous Stack Overflow answer expresses it well: https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118

### Pandoc

Is CLI application is an _absurdly_ powerful utility for converting between document types. I use it often as it allows one to write quickly in the simple language of Markdown and then generate pdfs (via LaTeX), slide shows, or HTML for websites (like this whole site!).

**Example:** `pandoc [inputfilename.md] -o [outputfilename.pdf]`

## General Terminal Utilities

### fzf

If you only add one program to your workflow from looking at this site, make it this one.

### neovim

### ranger

File-manager in the terminal is a must-have IMO for visually orienting oneself in filesystem organizations in text shell interfaces. I recently switched to [joshotu]() but haven't used it long enough to give a solid recommendation to this alternative.

### ssh

By setting up port-forwarding on your router, you can break down the physical barriers to working on a more powerful desktop machine from anywhere. For example, I use `ssh` to connect directly to the shell on my more powerful desktop, to tunnel into a VNC connection to provide a remote GUI display, and to mount files remotely through `sshfs`.

### tmux

I use tmux constantly to organize my development and writing environments. It allows one to collect tasks into sessions which I use for broad tasks with tabs for specific foci and panes to run individual programs. In combination with `ssh`, one can maintain the same working setup on a machine indefinitely and connect to it from anywhere. With the addition

## Linux Distributions

### Linux Mint

An excellent distribution (distro) for new Linux users, Mint is based on Ubuntu's Long Term Support release but has additional tools to help guide new users in setting up backups, etc. Ubuntu has the largest Linux desktop community, which leads to lots of online help and official support, which is nearly always equally applicable to Mint. Valuing stability over new feature updates, it works well for someone who simply wants their machine to work and doesn't care if they don't have the latest features of every program. They also work to develop their own desktop environment (DE) called Cinnamon.

recommended DE/edition: Cinnamon

[Install guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/)

### Arch Linux

Almost the opposite philosophy from Mint, this distro is all about setting up a bleeding-edge system from individual components tailored to an individual's preferences. Rather than maintaining a long-supported stable system of increasingly old programs, it is constantly updating, keeping pace with most new software releases directly from the developers. Arch Linux makes sharing software easy by allowing anyone to contribute packaging scripts to the Arch User Repository (AUR). I have found this particularly useful for neuroimaging programs which are almost all under active development by other researchers and academics. Using Arch as my platform for my analysis and development allows me to keep up with improved features from neuroimaging software in an integrated and automated way. I maintain multiple AUR packages to help the neuroimaging community on Arch.

My favorite DE: GNOME 40+ (on Wayland)

[Install guide](https://wiki.archlinux.org/title/installation_guide)

### Debian

Rock-solid. Free software. "The universal operating system." It's Debian. I'm running this website on a Debian server and recommend it for many general server applications. However, the slow update cycle makes it frustrating for everyday desktop use in my experience. Missing out on too many of the recent features in desktop programs can be noticeably painful.

DE: I don't have one on my install and `ssh` into the server directly.

## Python Libraries

### The Nipy Neuroimaging Python Suite

### Pandas

### Seaborn

### Scikit Image

## Research Tools

### Zotero

I used to recommend Mendeley as THE way to manage one's library of scientific literature. Unfortunately, recent releases have become buggy for large libraries (I have lost multiple papers without even knowing until later), and the company behind the program is increasingly hostile to users. It has started trying to lock down one's library with encryption. Encryption is beneficial in the hands of users, but here it is in the hands of the company and used to limit user freedom to switch platforms. I currently believe Zotero is a better long-term option.

Recommend using the ZotFile extension to place literature pdf into a folder synced between your machines.

### Jupyter-lab

I consider jupyter-notebooks suboptimal for any in-depth work, but they are perfect for initially iterating on figures, exploring data, and prototyping analysis. Jupyter-lab is a handy tool for exploring scientific data for this reason.
