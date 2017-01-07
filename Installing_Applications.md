Installed R and RStudio from their respective websites  
No problems  

Installed the VLC media player using:  
    `sudo get-apt updates`      
    `sudo get-apt install vlc`    
The first DVD I tried would not play. Googled and found I need to install `libdvdcss`, `libdvdread4`, and `libdvdnav4`.  
    `sudo get-apt install libdvdcss libdvdread4 libdvdnav4`  
Got message:  
    `libdvdcss` is not available.
I checked and the other two are installed.https://ubuntuforums.org/showthread.php?t=2312060 
Googled around a bit, and got to here: http://askubuntu.com/questions/487949/ubuntu-14-04-and-libdvdcss-file. No luck. 
Found this page, too: https://ubuntuforums.org/showthread.php?t=2312060

  
Installed abcde CD ripper using:  
    `sudo get-apt install abcde`        
Received a message to update postfix mail. I chose not to do anything.  
No problems with remaining install  

Next:  
* Need to install `lame` to rip .mp3 files - https://ubuntuforums.org/showthread.php?t=109429
