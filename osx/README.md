# SSH
```
ssh-keygen -t rsa -b 4096 -C "mwurzberger@mdwsolutions.net"
pbcopy < ~/.ssh/id_rsa.pub
```
Add key now in clipboard to github

# Command Line
Set resource limits `sudo launchctl limit maxfiles 1000000 1000000`

# Git Setup
```
git config --global core.editor “nano” && 
git config --global user.name "Matthew Wurzberger" && 
git config --global user.email "mwurzberger@mdwsolutions.net"
```	

After Beyond Compare is installed
```
git config --global diff.tool bc3 && 
git config --global merge.tool bc3 && 
git config --global mergetool.bc3 trustExitCode true
```

# NPM Setup
mkdir ~/npm
nano ~/.npmrc
prefix = /Users/mwurzberger/npm

# Install Homebrew (Node.js and wget)
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install node
brew install wget
```

# Finder
View > Show Status Bar
View > Show Path Bar
View > Show View Options > Check 'Show Library Folder'

# Applications
Slack - https://slack.com/ (communication)
DBeaver - http://dbeaver.jkiss.org/ (relational DB)
Robomongo - https://robomongo.org/ (non-relational DB)
BeyondCompare - http://www.scootersoftware.com/download.php
Keka - http://www.kekaosx.com/en/ (archival tool)
TextWrangler - http://www.barebones.com/products/TextWrangler/

# VMWare Tools
Mount VM Tool.iso file to VMware (VM > Reinstall VMWare Tools)
Run the Install VMware Tools link that pops up from the mounted disk



Configurations
Terminal
Download https://github.com/stephenway/monokai.terminal zip file
Double click on the Monokai.terminal script
Terminal > Preferences > Profiles > Monokai > Click ‘Default’ button

Git
Install diffmerge from website (not dmg version)
git config --global merge.tool diffmerge
git config --global mergetool.diffmerge.cmd "diffmerge --merge --result=\$MERGED \$LOCAL \$BASE \$REMOTE"
git config --global mergetool.diffmerge.trustExitCode true
git config --global mergetool.keepBackup false


New Software
Install brew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew link openssl
brew install wget

SizeUp - window resizing manager
Paw - https://paw.cloud/ API tool
Paw - https://paw.cloud/ API tool

Broken in newer version of OSX
     xtrafinder - add tabs and other small things to finder https://www.trankynam.com/xtrafinder/
