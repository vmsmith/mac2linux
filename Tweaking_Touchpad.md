Once I got the Linux distribution properly installed, the touchpad started acting totally crazy. It seemed as though all I had to do was look at it and things would start happening. It was hypersensitive.

After some Googling, I found that this is not uncommon. It has to do with the touchpad driver.

The original driver is a synaptics driver, and it turned out that what I wanted was an mtrack driver.

Some fellow named Phil Plückthun wrote a pretty comprehensive guide to installing Ubuntu 14.10 on a Macbook, and what he wrote generally worked for me.

I installed the mtrack driver with:

    sudo apt-get install xserver-xorg-input-mtrack

I saved the synaptics configuration file to a backup:

    sudo mv /usr/share/X11/xorg.conf.d/50-synaptics.conf /usr/share/X11/xorg.conf.d/50-synaptics.conf.bak

And then I got rid of the driver:

    sudo apt-get autoremove xserver-xorg-input-synaptics
    
Finally, I edited the mtrack configuration file with:

    sudo vim /usr/share/X11/xorg.conf.d/50-mtrack.conf
    
These are the settings I used:

    Section "InputClass"
         MatchIsTouchpad "on"
         Identifier "Touchpads"
         Driver "mtrack"
         Option "IgnoreThumb" "true"
         Option "ThumbSize" "50"
         Option "IgnorePalm" "true"
         Option "DisableOnPalm" "false"
         Option "BottomEdge" "30"
         Option "TapDragEnable" "true"
         Option "Sensitivity" "0.6"
         Option "FingerHigh" "3"
         Option "FingerLow" "2"
         Option "ButtonEnable" "true"
         Option "ButtonIntegrated" "true"
         Option "ButtonTouchExpire" "750"
         Option "ClickFinger1" "1"
         Option "ClickFinger2" "3"
         Option "TapButton1" "1"
         Option "TapButton2" "3"
         Option "TapButton3" "2"
         Option "TapButton4" "0"
         Option "TapDragWait" "100"
         Option "ScrollLeftButton" "7"
         Option "ScrollRightButton" "6"
         Option "ScrollDistance" "100"
    EndSection

The cursor still moved too fast, and I had to change "Sensitivity" to "0.5".

Fortunately, there is a list of all the configuration options at [xf86-input-mtrack](https://github.com/BlueDragonX/xf86-input-mtrack/) GitHub repository.

There are also a few links that can help:

[Phil Plückthun's Medium Article](https://medium.com/@philpl/ubuntu-14-10-running-on-my-macbook-18991a697ae0)  
[Ubuntu Community Page](https://help.ubuntu.com/community/MacBookPro11-1/utopic)  
[Yarenty's Blog](http://yarenty.blogspot.com/2014/08/how-to-fix-macbook-pro-touchpad-on.html)  


