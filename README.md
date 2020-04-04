# Install-a-new-Mac
Short description on how to install all necessary tools on a macOS computer and which setting to change to make this computer really yours.

Go to *System Preferences, Keyboard*
Change *Key Repeat* to *Fast*
Change *Delay Until Repeat* to *Short*

Go to *System Preferences, Date & Time preferences*
Set your preferred way of the clock






**Install homebrew**

Homebrew is an packagage installer that will help you installing a lot of programs right from the command line. So type in *terminal* in your spotlight (⌘+space) and hit the following code.

    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

*source: [brew.sh](https://brew.sh/)*

Now you can install many needed programs straight from the terminal.
Here are some defaults for most people.

    brew update
    brew install gnupg gnupg2 (needed for rvm)    
    
Special for me
    brew install ssh-copy-id
    brew install imagemagick --build-from-source --with-quantum-depth-8
    


install manually
* Chrome https://www.google.nl/intl/nl/chrome
* Dropbox https://www.dropbox.com/install
* Atom https://atom.io
  * Atom packackes
  * auto-indent
* Discord https://discordapp.com/download
* Visual studio code https://code.visualstudio.com/Download

Install from the AppStore
* Slack
* Window Tidy
* inet network scanner


I don't like the Dock in screen

    defaults write com.apple.dashboard mcx-disabled -boolean YES
    killall Dock

Doesn't seen to work on **macOS Catalina**
    This makes the tiles really small, but still there
    
    defaults write com.apple.dock tilesize -integer 1; killall Dock               # This makes the tiles really small, but still there
    defaults write com.apple.dock static-only -bool true; killall Dock            # Only active apps, to make it smaller
    defaults write com.apple.dock autohide-time-modifier -float 0; killall Dock   # Can't make it disappear, so make it fast
    defaults delete com.apple.dock;  killall Dock                                 # Set back to defaults


# Install RVM

    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E37D2BAF1CF37B13E2069D6956105BD0E739499BDB
    
  curl -sSL https://get.rvm.io | bash -s stable
  
   source /Users/paulverschoor/.rvm/scripts/rvm
  
 # configure git
 *bash*
 
     git config --global --edit
     
     git config --global core.excludesfile ~/.gitignore_global
     echo .DS_Store > ~/.gitignore_global
     

*source: [rvm.io](http://rvm.io)* 
