---
published: true
title: Installing Evernote in Linux Using Wine (May 2017)
---
I use Evernote a lot. It keeps all my thoughts, log journals, experiments, tests, code pieces (bash aliases, etc), personal simulation philisophy, thought pieces, articles, and more. 

I also love to use Linux (Currently switching between Fedora & Ubuntu Budgie, although using the Gnome desktop enviroment).

Sadly, evernote does not have a native linux application (doesn't everyone just use nodejs and electron.js for desktop applications now?). In the past this has *eventually* led me to go back to Windows. But I have figured out a way, thanks to WineHQ, to get the latest Evernote version 6.4.2 to work on linux. It has some grapical issues, but mainly just text aliasing. 

## Here's how to do it: with wine and winetricks (for GUI haters:

Install winetricks with your package manager if it's not already installed.
Run the following commands in a terminal: 
1. export WINEARCH=win64
2. winetricks -q ie8
3. wine "*evernote_installer_path*"
4. Follow the installer's instructions
5. The evernote executable is now located at "*wineprefix_path*/drive_c/Program  Files/Evernote/Evernote/Evernote.exe"


## Here is how to make Evernote work with q4wine, a gui for wine.

Make sure you have winetricks and q4wine installed (look for them in your package manager).
Make sure that your terminal is properly configured in q4wine:
  1. Opens the options menu: File > Options
  2. Select "General" and opens the "Utils" tab
  3. Enter the path of your terminal, for instance "/usr/bin/gnome-terminal" if you use gnome.
  4. Enter "-e" as an argument (without the quotes, as always), so that q4wine can execute command just after opening a terminal.
  5. Download evernote for windows, from the evernote website.

**Installation steps:**

1. In the terminal window, type "winetricks -q ie8" (without the quotes) and press Enter. Wait    for the ie8 installation to finish.
2. Run the Evernote installer.

You now have Evernote working (nearly perfectly). 

WebClipper also works which was a massive surprise. Applicator and all.
