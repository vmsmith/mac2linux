<< [README](https://github.com/vmsmith/mac2linux/blob/master/README.md) < [Previous](https://github.com/vmsmith/mac2linux/blob/master/Machine_Preparations.md) || [Next](https://github.com/vmsmith/mac2linux/blob/master/Installing_Applications.md) > [Appendices]() >> 


* Downloaded `ubuntu-16.04.1-desktop-amd64.iso` from [Ubuntu site](https://www.ubuntu.com/download/desktop).

* Downloaded `UNetbootin` from the [UNetbootin site](http://unetbootin.github.io/).

* Moved both files on to USB.

* Put .iso image on desktop.

* Changed screen capture location to Kingston drive:
  * `defaults write com.apple.screencapture location /Volumes/KINGSTON/screenshots/`
  * `killall SystemUIServer`

* Ran `unetbootin-mac-625-dmg`. The first thing that appeared was the following:

![unetbootin files](/images/Screen Shot 2016-11-21 at 11.36.41 AM.png)

* Double-clicked on the .app and got this:

![warning message](/images/Screen Shot 2016-11-21 at 11.37.03 AM.png)

* Clicked on "Open" and got this:

![unexpected quit message](/images/Screen Shot 2016-11-21 at 11.32.14 AM.png)

* Did some Googling and found this on an Apple help page: [If an application quits unexpectedly](https://help.apple.com/machelp/mac/10.7/help/index.html?lang=en#mchlp2579)
