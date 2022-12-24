---
title: Software I find helpful in my daily life
---

This website was written in `markdown` using `neovim` on Arch Linux and converted to HTML with `pandoc`. I'll cover these tools, and others, on this page. The page is organized in order of most to least broad recommendation (I strongly recommend each of these tools, but not all will apply to every user).

For help applying markdown to scientific writing, see my work [here.](https://github.com/liamtimms/scientific-markdown)

## Terminal Applications

I prefer to use terminal applications when possible. While it may initially sound odd, it is pragmatic for a few reasons:

### The unavoidable power of text

Humans communicate the majority of technical ideas and instructions via text. The terminal is a primarily text-based interface that fits neatly into this niche. It does not make sense to use it for graphical tasks like photo editing, but it is simple and elegant for anything text-oriented.

Text:

1. can communicate specific information with precision
2. is exactly repeatable
3. travels efficiently over both space (networking) and time (documentation)
4. can be relatively quickly input into a machine
5. is exactly repeatable
6. The most powerful input device on your computer is currently the keyboard. Terminal applications allow you to take full advantage of this and minimize the time you spend switching input devices and mental context between keyboard and mouse.

### Remote and recall

Because text is exactly repeatable and can be easily transmit, terminal based programs which use text input can be easily controlled by simple scripts or remotely without needing to render and navigate on the 2D surfaces of screens.

1. Terminal applications can be run remotely without perceptible delay through `ssh`. You can efficiently and instantly utilize the full power of a personal or cloud machine remotely.
2. Solving the problems with text-based commands in a "shell" enables quick automation of those solutions (via shell scripts) or immediate recall of the solution from history ("crtl+r" with `fzf` keybindings in the shell vastly simplifies this). There is no need to type the same command multiple times.
3. A good terminal emulator has imperceptible input and output delay. Many modern GUI applications cannot boast this, particularly when accessed remotely.
4. Programs like `tmux-resurrect` can reduce the disruption from working remotely or setting up whole workspaces after rebooting. You never need to leave your spot in an entire set of open files. This is not the case for most GUI applications.

### A secret third thing

Many scripts and small software applications are developed without GUI front ends in academic or scientific contexts. Therefore, using the terminal is unavoidable. Embracing this fact increases comfort when using these programs, and familiarity reduces the cognitive load required for the inevitable debugging.

### Neovim

A program I have made incredibly central to my interaction with my computer.

`Vim` is a decades-old text editor program with a brilliant built-in language for manipulating text. Neovim (`nvim`) is a refactored and modernized version that adds new features. Vim/neovim has many powerful extensions, letting you do everything from compiling LaTeX documents live as they are edited to automatically formatting Python code. The program is language-agnostic, so you don't get caught up in the particularities of word processes, IDEs, and GUI text editors. If it involves manipulating words on a screen, there's no better tool invented. I use it for coding, writing papers, taking notes, creating this website, etc. You can see my configuration/plug-ins [here.](https://raw.githubusercontent.com/liamtimms/configs/master/.config/nvim/init.vim)

If you aren't sold on it, this famous Stack Overflow answer expresses it well: https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118

### Pandoc

Is CLI application is an _absurdly_ powerful utility for converting between document types. I use it often as it allows one to write quickly in the simple language of Markdown and then generate pdfs (via LaTeX), slide shows, or HTML for websites (like this whole site!).

**Example:** `pandoc [inputfilename.md] -o [outputfilename.pdf]`

## General Terminal Utilities

### fzf

If you add only one program to your workflow on the command line, make it `fzf`. This fuzzy finder enables fast recall of previous commands, switching active directories, and quickly opening files.

### ranger

File-manager in the terminal is a must-have IMO for visually orienting oneself in filesystem organizations in text shell interfaces. I recently switched to [joshotu](https://github.com/kamiyaa/joshuto) but haven't used it long enough to give a solid recommendation for this alternative.

### ssh

By setting up port-forwarding on your router, you can break down the physical barriers to working on a more powerful desktop machine from anywhere. For example, I use `ssh` to connect directly to the shell on my more powerful desktop, tunnel into a VNC connection to provide a remote GUI display, and mount files remotely through `sshfs`.

### tmux

I use tmux constantly to organize my development and writing environments. It allows one to collect tasks into sessions which I use for broad tasks with tabs for specific foci and panes to run individual programs. In combination with `ssh`, one can maintain the same working setup on a machine indefinitely and connect to it from anywhere. With the addition

## Linux Distributions

### Linux Mint

An excellent distribution (distro) for new Linux users, Mint is based on Ubuntu's Long Term Support release but has additional tools to help guide new users in setting up backups, etc. Ubuntu has the largest Linux desktop community, which leads to lots of online help and official support, which is nearly always equally applicable to Mint. Valuing stability over new feature updates works well for someone who wants their machine to work and doesn't care if they don't have the latest features of every program. They also work to develop their own desktop environment (DE) called Cinnamon.

recommended DE/edition: Cinnamon

[Install guide](https://linuxmint-installation-guide.readthedocs.io/en/latest/)

### Arch Linux

Almost the opposite philosophy from Mint, this distro is all about setting up a bleeding-edge system from individual components tailored to an individual's preferences. Rather than maintaining a long-supported stable system of increasingly old programs, it is constantly updating, keeping pace with most new software releases directly from the developers. Arch Linux makes sharing software easy by allowing anyone to contribute packaging scripts to the Arch User Repository (AUR). I have found this particularly useful for neuroimaging programs which are almost all under active development by other researchers and academics. Using Arch as my platform for my analysis and development allows me to keep up with improved features from neuroimaging software in an integrated and automated way. I maintain multiple AUR packages to help the neuroimaging community on Arch.

My favorite DE: GNOME 40+ (on Wayland)

[Install guide](https://wiki.archlinux.org/title/installation_guide)

### Debian

Rock-solid. Free software. "The universal operating system." It's Debian. I'm running this website on a Debian server and recommend it for many general server applications. However, the slow update cycle makes it frustrating for everyday desktop use, in my experience. Missing out on too many of the recent features in desktop programs can be noticeably painful.

DE: I don't have one on my install, and `ssh` into the server directly.

## Python Libraries

### The Nipy Neuroimaging Python Suite

Nipy is a Python library for analyzing neuroimaging data, such as MRI and PET scans. It offers tools for loading, processing, and visualizing brain images. It has a couple sub-project tools associated with it:

#### Nipype

Nipype is a Python library for creating and running neuroimaging pipelines. It provides a flexible and extensible interface to a range of neuroimaging tools, allowing users to easily build and execute complex processing workflows. Nipype is particularly useful for reproducibility, as it allows users to easily document and share their pipelines with others.

#### Nibabel

Nibabel provides a set of functions for reading and writing various neuroimaging file formats, such as NiFTI and ANALYZE, as well as tools for interacting with and manipulating neuroimaging data in a variety of ways. It is particularly useful for general MRI data analysis pipelines (even when not using it to translate between image formats as the "babel" name implies) because it allows one to load NifTI images into `numpy` arrays.

#### Nilearn

Nilearn is a Python library for analyzing and visualizing neuroimaging data. It provides a range of tools for loading, processing, and analyzing neuroimaging data, including MRI and PET scans, as well as functions for extracting and manipulating brain maps and other features from neuroimaging data. Nilearn is particularly useful for tasks such as statistical analysis, machine learning, and visualization of brain images.

#### Dipy

Diffusion imaging in Python (DiPy) is a Python library for the analysis of diffusion magnetic resonance imaging (dMRI) data. It provides a range of tools for loading, processing, and analyzing dMRI data, including functions for estimating diffusion tensors, performing tractography, and visualizing diffusion data. DiPy is particularly useful for tasks such as studying white matter microstructure, investigating brain connectivity, and analyzing the organization of the brain's fibers. I use it in my work on non-diffusion relaed research because the image correction functions it supplies can be useful for more general quantitative MR image analysis than just diffusion.

### Pandas

Pandas is a Python library that provides high-performance, easy-to-use data structures and data analysis tools. It is designed to work with tabular data, such as spreadsheets or datasets in a SQL database, and allows you to manipulate and analyze these types of data in a fast and efficient manner. Pandas is widely used in data science and machine learning projects but can also be combined with `numpy` and manually created excel sheets for easy use in neuroimaging data analyis.

Also of note: **Polars** which provides Pandas like dataframe structures in `rust`. It can be used in both rust and python data pipelines and delivers higher performance at the cost of less documentation, stackoverflow answers, and tutorials being currently available.

### Seaborn

Seaborn is a Python library for creating graphics and visualizations. It is built on top of Matplotlib and provides a high-level interface for quickly drawing attractive data visualizations. It provides a range of graph types, including scatter plots, line plots, bar plots, and heatmaps, and has a variety of customization options to allow users to create visually appealing and informative graphics.

However, an unfortunate con of seaborn is that it is often extremely difficult to make customizations to some of the default settings for each type of graph it provides and there are multiple levels of abstraction within seaborn itself. Therefore it is extremely easy to create a nice looking graph while knowing or tweaking very little, but "abstractions have a cost" and sometimes getting the _exact_ graph one desires requires learning multiple layers of seaborn _and_ the underlying matplotlib fuctions it is using _and_ understanding how to correctly pass options to both libraries at once.

### Scikit Image

Scikit-image is a Python library for image processing and computer vision. It provides a range of tools for tasks such as image filtering, restoration, and feature detection, as well as functions for building image processing pipelines and working with large datasets. Scikit-image is built on top of NumPy and SciPy and is designed to be easy to use and integrate into scientific workflows.

### Scikit Learn

Scikit-learn is a Python library for machine learning and statistical modeling. It provides a range of tools and algorithms for tasks such as classification, regression, clustering, dimensionality reduction, and model selection, as well as tools for preprocessing and feature extraction.

## Research Tools

### Zotero

I used to recommend Mendeley as THE way to manage one's library of scientific literature. Unfortunately, recent releases have become buggy for large libraries (I have lost multiple papers without even knowing until later), and the company behind the program is increasingly hostile to users. It has started trying to lock down one's library with encryption. Encryption is beneficial in the hands of users, but here it is in the hands of the company and used to limit user freedom to switch platforms. I currently believe Zotero is a better long-term option.

Recommend using the ZotFile extension to place literature pdf into a folder synced between your machines.

### Jupyter-lab

I consider jupyter-notebooks suboptimal for any in-depth work, but they are perfect for initially iterating on figures, exploring data, and prototyping analysis. Jupyter-lab is a handy tool for exploring scientific data for this reason.
