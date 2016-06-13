#### A Collection of Terminal Tweaks for Mac OS X Hosted by [MacTweaks](https://www.mactweaks.net)

#### Notes

* Most of these 'tweaks' edit .plist files in ~/Library/Preferences. To use them simply paste a command into a Terminal window. 
* You can revert changes by deleting the appropriate .plist file or by replacing TRUE/FALSE. 
* I recommend testing these tweaks in a temporary account and turning on 'fast user switching'.
* You can edit .plist files directly by opening them in xcode.
* Use 'sudo' at the beginning of a command to edit locked files.
* Drag and drop files and folders into a terminal window to add its path.
* cd means change directory
* files with a space in their name require a backslash (DVD\ Player.app) or quotation marks ("DVD Player.app")

#### Change System Fonts
* These are the default fonts and sizes
* To use these commands per application replace -g with -app followed by the name of the application (-app Bean NSTitleBarFont).
* To use these commands on applications located within a folder first cd into that directory.
* 'NSBoldSystemFont' safari tab bar
* 'NSPaletteFont' utility window title bar
* 'NSTitleBarFont' title bar 




***




**Plain Text In Mail**

     defaults write com.apple.mail PreferPlainText -bool TRUE

**Disable And Hide Spotlight**

     sudo chmod 600 /System/Library/CoreServices/Search.bundle/Contents/MacOS/Search; killall SystemUIServer

**Disable And Hide Notifications**

     sudo defaults write /System/Library/LaunchAgents/com.apple.notificationcenterui KeepAlive -bool FALSE

**Expand Print Panel By Default**

     defaults write -g PMPrintingExpandedStateForPrint -bool TRUE

**Expand Save Panel By Default**

     defaults write -g NSNavPanelExpandedStateForSaveMode -bool TRUE

**Disable Mission Control Animation**

     defaults write com.apple.dock expose-animation-duration -int 0; killall Dock

**Show All Hidden Files**

     defaults write com.apple.finder AppleShowAllFiles TRUE

**Disable Tooltips**

     defaults write -g NSInitialToolTipDelay -int 999999; killall Finder

**Enable Text Selection In Quicklook**

     defaults write com.apple.finder QLEnableTextSelection -bool TRUE; killall Finder

**Disable Quick Look Window Animation**

     defaults write -g QLPanelAnimationDuration -float 0; killall Finder

**Disable New Window Animation**

     defaults write NSGlobalDomain NSAutomaticWindowAnimationsEnabled -bool FALSE; killall SystemUIServer

**Disable Dialog Box Animation**

     defaults write NSGlobalDomain NSWindowResizeTime 0.001

**Hide Applications**

     sudo chflags hidden /path/to/file

**Disable Autosave/Versions And Enable ’Save-As’**

     defaults write -g ApplePersistence -bool no

**Disable Rubber Band Scrolling**

     defaults write -g NSScrollViewRubberbanding -int 0; killall Finder

**Disable Rubber Band Scrolling In Itunes**

     defaults write com.apple.iTunes disable-elastic-scroll -bool TRUE

**Set Path Bar To Home Directory**

     defaults write com.apple.finder PathBarRootAtHome -bool TRUE; killall Finder

**Show Full Path In Finder Title Bar**

     defaults write com.apple.finder _FXShowPosixPathInTitle -bool TRUE

**Hide 'Automatically Add To Itunes' Folder**

     chflags hidden ~/Music/"Automatically Add to iTunes.localized"

**Change Default Screenshot Location**

     defaults write com.apple.screencapture location /path/to/destination; killall SystemUIServer

**Single App Mode**

     defaults write com.apple.dock single-app -bool TRUE; killall Dock

**Disable Dashboard**

     defaults write com.apple.dock single-app -bool TRUE; killall Dock

**Trash Folder On Desktop**

ln -s ~/.Trash ~/Desktop/Trash

**Change System Fonts**

     defaults write -g NSBoldSystemFont LucidaGrande-Bold 
     defaults write -g NSBoldSystemFontSize -int 13 
     defaults write -g NSFixedPitchFont Menlo-Regular 
     defaults write -g NSFixedPitchFontSize -int 11 
     defaults write -g NSFont Helvetica 
     defaults write -g NSFontSize -int 12 
     defaults write -g NSLabelFont LucidaGrande 
     defaults write -g NSLabelFontSize -int 10 
     defaults write -g NSMessageFont LucidaGrande 
     defaults write -g NSMessageFontSize -int 13 
     defaults write -g NSPaletteFont LucidaGrande 
     defaults write -g NSPaletteFontSize -int 10 
     defaults write -g NSSystemFont LucidaGrande 
     defaults write -g NSSystemFontSize -int 13
     defaults write -g NSTitleBarFont LucidaGrande 
     defaults write -g NSTitleBarFontSize -int 13 
     defaults write -g NSToolTipsFont LucidaGrande 
     defaults write -g NSToolTipsFontSize -int 11

**Lock Dock**

     defaults write com.apple.Dock contents-immutable -bool TRUE; killall Dock

**2D Dock**

     defaults write com.apple.dock no-glass -boolean TRUE; killall Dock

**Disable Dock**

     defaults write com.apple.dock autohide-time-modifier -int 999999 && defaults write com.apple.Dock autohide-delay -float 999999; killall Dock

**Resize Dock**

     defaults write com.apple.dock tilesize -int 34

**Show Dock Animation Speed**

     defaults write com.apple.dock autohide-time-modifier -int 1

**Hide Dock Animation Speed**

     defaults write com.apple.Dock autohide-delay -float 1

**Disable Dock Animation**

     defaults write com.apple.dock autohide-time-modifier -int 0.1 && defaults write com.apple.Dock autohide-delay -float 0.1; killall Dock

**Transparent Icon For Hidden Applications**

     defaults write com.apple.dock showhidden -bool TRUE; killall Dock

**Disable Bouncing Applications In Dock**

     defaults write com.apple.dock no-bouncing -bool TRUE; killall Dock





