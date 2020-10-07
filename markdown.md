{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "<div style=\"float:left\">\n",
    "            <h1 style=\"width:450px\">Practical 1: Getting Started</h1>\n",
    "            <h2 style=\"width:450px\">Getting to grips with Jupyter, Git and Markdown</h2>\n",
    "</div>\n",
    "<div style=\"float:right\"><img width=\"100\" src=\"https://github.com/jreades/i2p/raw/master/img/casa_logo.jpg\" /></div>"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Welcome!\n",
    "\n",
    "If you haven't already watched it, then please see the [_Welcome_ video](https://web.microsoftstream.com/video/f80fdbac-cba1-45b5-a170-407b0dca887c) that I recorded for you: it sets out how I approach the teaching of programming and how I think you can ensure that you both learn to code _and_ maximise your chances of getting a good mark in the course. \n",
    "\n",
    "And here's a _short_ introduction to Practical 1.\n",
    "\n",
    "[![Practical 1 Video](https://github.com/jreades/i2p/raw/master/practicals/img/Practical_1_Still.png)](https://web.microsoftstream.com/video/49b76b86-69df-4006-ba3d-c0fb4dbb3839)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Task 1: Git and Version Control\n",
    "\n",
    "Understanding how to use Git and GitHub effectively is a core element of learning to code. So one of the _first_ things that we are going to do is set you up with an account and a new project.\n",
    "\n",
    "So in order to complete this task you need to:\n",
    "1. Create a login with [GitHub](https://github.com). You may wish to set it up with your UCL email and then link a personal email address as well.\n",
    "2. Create a new **private** project directly on GitHub. You might as well call it `i2p` since that's a lot shorter than `intro_to_programming_for_spatial_analysts`.\n",
    "3. Edit the `README.md` file with some information about what's in the project (_e.g._ your notes and practicals for the module).\n",
    "4. Save the changes (this is called a 'commit') and say in a general way what edits you did.\n",
    "5. Work out how to compare the original and edited versions of `README.md` in your browser."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Task 2: Getting Comfortable with Markdown\n",
    "\n",
    "To get some practice with Markdown let's write up some notes direclty in our GitHub repository (aka 'repo'). Here's a screenshot from GitHub of the [Markdown lecture](https://github.com/jreades/i2p/blob/master/lectures/1.3-Writing_Code.md).\n",
    "\n",
    "![Markdown Image](https://github.com/jreades/i2p/raw/master/practicals/img/Markdown.png)\n",
    "\n",
    "In order to complete this task you will need to:\n",
    "\n",
    "1. Select *one* of today's lectures by visiting [jreades/i2p/lectures](https://github.com/jreades/i2p/tree/master/lectures) and selecting one of the files starting `1.`\n",
    "2. You will need to click on `Raw` to see the Markdown. \n",
    "3. Select and copy all of the raw Markdown.\n",
    "4. Go back to **your** repository and select `Add File > Create New File`, then paste in the copied text.\n",
    "5. Once the file has been added successful, edit it by clicking on the 'pencil' icon. \n",
    "\n",
    "Add notes incorporating:\n",
    "  - Plain text\n",
    "  - Header levels: `#`, `##`, `###`, etc.\n",
    "  - Emphasis/Italics: `_italics_`, `**bold**`.\n",
    "  - Lists: `- ` and `1. `.\n",
    "  - Links: `[link text](url)`.\n",
    "  - Images: `![Alt text](url)`.\n",
    "  - Code: \\``...`\\`.\n",
    "  \n",
    "Save your changes (don't forget to add a basic comment outlining what you've done) and then view the difference (aka 'History) to see what you've edited."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Task 3: Installing Command Line Tools\n",
    "\n",
    "We need to install some basic tools that will allow us to interact with Git and other applications from the Terminal/Command Prompt. You only need to do one of these depending on your Operating System:\n",
    "\n",
    "1. **MacOS**: install the Xcode Command Line Tools [directly from the command line](https://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/).\n",
    "2. **Windows**: install Git Bash by following [these instructions](https://www.stanleyulili.com/git/how-to-install-git-bash-on-windows/). You may *also* find it helpful to install the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Task 4: Organising Your Workspace\n",
    "\n",
    "Before we start trying to code, I'd suggest organising your 'workspace' on your computer so that it's easy to find/load data and Python notebooks. The easiest way to do this is work from your `Documents` folder and set up some directories there to hold your code and data. You should generally go with what makes sense to you, but leaving everything in the Downloads folder or in random places all over you computer is likely to be a disaster.\n",
    "\n",
    "Here's _one_ way of organising things, and I'm also taking the opportunity to show you how to do this using the Command Line:\n",
    "\n",
    "```bash\n",
    "cd ~  # This will normally take you to your 'home' directory (on a Mac this is /Users/<your username>)\n",
    "cd Documents # You're now *c*hanging *d*irectory to the Documents folder (e.g. /Users/<your username>/Documents)\n",
    "mkdir CASA # *make* a *dir*ectory called `CASA`\n",
    "mkdir CASA/modules # make a directory called `modules` under `CASA`\n",
    "mkdir CASA/modules/i2p # make an intro to programming directory\n",
    "```\n",
    "If you follow this approach then below, when you download the Vagrantfile, you will need to move it from your `Downloads` folder to `~/Documents/CASA/` (which is the equivalent to `/Users/<your username>/Documents/CASA/`)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Task 5: Getting Set Up with Vagrant or Anaconda Python\n",
    "\n",
    "You may be tempted to leave this for later, but we'd _strongly_ encourage you to try installing the programming environment as soon as possible so that we have as long as possible to help you over any hurdles before we get to week 3 where it will be essential that you are running the environment successfully. In our experience, the students who put off trying to get the environment running end up falling quickly behind as they are unable to complete basic tasks successfully. \n",
    "\n",
    "The _majority_ of you will be able to use the [Vagrant](https://www.vagrantup.com/)/[VirtualBox](https://www.virtualbox.org/) solution, but there will be _some_ Windows 10 users whose computers will refuse to run either VirtualBox or Vagrant, in which case will you need to run [Anaconda Python](https://anaconda.org/) directly.\n",
    "\n",
    "<div style=\"border: dotted 1px rgb(156,121,26); padding: 10px; margin: 5px; background-color: rgb(255,236,184); color: rgb(156,121,26)\"><i>Note</i>: There are any number of ways to organise your CASA work, what's important is that you put the Vagrantfile in the directory <i>above</i> where all of your <i>Introduction to Programming</i> notebooks are stored, and that you are <i>logical</i> about things like names and hierarchy. This will make it much easier to access files and notebooks using Vagrant <i>and</i> using Python.</div>\n",
    "\n",
    "### Installing Vagrant \n",
    "\n",
    "I have [produced an installation video](https://web.microsoftstream.com/video/d94bc09d-02c9-45cf-83ed-3badeab3568b) for users on Apple's MacOS that is available on MS Streams directly as well as from the Moodle Page.\n",
    "\n",
    "[![Installing Vagrant](https://github.com/jreades/i2p/raw/master/practicals/img/Vagrant_Mac.png)](https://web.microsoftstream.com/video/d94bc09d-02c9-45cf-83ed-3badeab3568b?list=studio)\n",
    "\n",
    "The process for Windows users will be similar. We are working on a video for this.\n",
    "\n",
    "You can **follow along** in a [text version of the installation guide on GitHub](https://github.com/jreades/sds_env/tree/master/vagrant).\n",
    "\n",
    "### Installing Anaconda Python\n",
    "\n",
    "If the installation of Vagrant/VirtualBox fails, then you will need to go down this route for installing the programming environment. \n",
    "\n",
    "You can **follow along** in a [text version of the installation guide on GitHub](https://github.com/jreades/sds_env/tree/master/conda).\n",
    "\n",
    "To run Anaconda Python you will want to launch the new `Anaconda Prompt` (which should now appear as a new 'app' in your Windows menu) and type the following:\n",
    "\n",
    "```bash\n",
    "cd ~/Downloads/CASA\n",
    "conda activate sds2020\n",
    "jupyter lab\n",
    "```\n",
    "\n",
    "That's 'it'! You're done. We've had to put a lot of pieces of software in place for the term, but you'll find these useful across multiple modules that are part of your MSc/MRes and you're now set up for the future!"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Other Useful Resources\n",
    "\n",
    "- [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/)\n",
    "- [Common Mark](https://commonmark.org/help/)\n",
    "- [Markdown Guide](https://www.markdownguide.org/basic-syntax/), which helpfully includes do's and don'ts.\n",
    "\n",
    "Finally, these are a bit overkill but the bits about setting up and installing `git`, `bash`/`zsh`, and so on may come in handy later:\n",
    "- [Setting Up a New Mac](https://www.taniarascia.com/setting-up-a-brand-new-mac-for-development/)\n",
    "- [Beginner's Guide to Setting Up Windows 10](https://medium.com/@mfosullivan/a-beginners-guide-to-setting-up-a-modern-web-development-environment-on-windows-10-4d75cd94cde8)\n",
    "- [Setting up Windows without Linux](https://dev.to/jozsefsallai/how-i-ve-set-up-my-windows-machine-as-a-development-environment-without-wsl-2kcl)\n",
    "- [Microsoft Python Setup Guide](https://docs.microsoft.com/en-us/windows/python/beginners)"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.7.8"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 4
}
