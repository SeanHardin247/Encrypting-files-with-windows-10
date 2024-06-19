Connect to your windows 10 virtual machine using remote desktop
Click on the file explorer icon on the taskbar
Select "This PC" on the left side bar and underneath the devices and drives section that pops up right click on Windows (C:)
On the popup click the Turn on BitLocker option with a shield next to it
We will preform a file backup before starting, when you get to the Preparing your drive for BitLocker screen click on the underlined blue text that says "Use file History to preform a backup"
Now a window will be brought up about file history, click on the turn on button to turn on file history, beneth the storage drive icon it should say something along the lines of saving now, and when its done it will say "Files last copied on" and then the current date
You can close this window now and return to the Bitocker window, Select next and wait
Click next again, now you will have an option to select how you want to back up your recovery key, which can save you if you cant get into your PC, in a real life scenario you may want to print it or do all of these, but we will just choose the Save to file option
Another winodw will open, this one is a file explorer window, we cant save this to an encrypted drive, that would be pointless since we need this key incase we cant get back into our encrypted files. 
On the left side bar double click click Temporary Storage (D:) and near the top click New Folder. You can name this folder whatever you want, or not name it at all. Hit enter when finished naming.
Double click your new folder and hit save or enter on your keyboard. This will save your BitLocker recovery key .txt document
The next option in BitLockers setup is how much of our drive we want to encrypt, there is a lot of text explaining it but the short version is for new PCs we want to select encrypt used disk space only, and Ecrypt entire drive for PCs that have been using for awhile.
Make sure Encrypt used disk space only is checked and hit next.
Next is which encryption mode, most likely you will never move this drive to a windows operating system older than 10, so we will choose the new encryption mode and hit next.
Now we begin the encryption process which may take awhile and the computer will restart, click continue and a popup will come out of the right side of the screen, click it and cick restart now. alternatively if you missed the popup right click the windows button, hover over shut down or sign out and press restart.
Obviously now you will kicked out of your Remote desktop session, wait around 30 seconds and try to log back in. 
Once back in click file explorer and This PC then right click Windows (C:) where a new option will be in place of turn on bitlocker, this one will say "Manage Bitlocker" Click it.
If done right you should see an the drive icon this time with the padlock and key in it, the text will say BitLocker is on. 
We are going to make sure it is done though, right click on the windows icon and select "Windows Powershell (Admin)"
In Powershell type "manage-bde -status" then hit enter on the keyboard a bunch of stuff will popup but look for the Percentage Encryption section, if it says 100% then you are good it go and have completed this tutorial properly!
