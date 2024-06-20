<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 pro</b> (21H2)

  <h2>Steps </h2>

- Connect to your Windows 10 virtual machine using remote desktop.

- Click on the file explorer icon on the taskbar.

- Select "This PC" on the left side bar, and underneath the devices and drives section that pops up, right-click on Windows (C:).

- On the popup, click the Turn on BitLocker option with a shield next to it.
  
- We will perform a file backup before starting. When you get to the Preparing your drive for BitLocker screen, click on the underlined blue text that says "Use file history to perform a backup."

- Now a window will be brought up about file history. Click on the turn on button to turn on file history. Under the storage drive icon, it should say something along the lines of saving now, and when it's done, it will say "Files last copied on" and then the current date.
You can close this window now and return to the Bitocker window. Select Next and wait.

- Click next again. Now you will have an option to select how you want to back up your recovery key, which can save you if you can't get into your PC. In a real life scenario, you may want to print it or do all of these, but we will just choose the Save to File option.
Another window will open; this one is a file explorer window. We can't save this to an encrypted drive; that would be pointless since we need this key in case we can't get back into our encrypted files.

- On the left side bar, double-click Temporary Storage (D:), and near the top, click New Folder. You can name this folder whatever you want, or not name it at all. Hit enter when finished naming.
  
- Double-click your new folder and hit save or enter on your keyboard. This will save your BitLocker recovery key.txt document.
  
- The next option in BitLockers setup is how much of our drive we want to encrypt. There is a lot of text explaining it, but the short version is that for new PCs, we want to select encrypt used disk space only and encrypt the entire drive for PCs that have been using it for awhile.
  
- Make sure Encrypt used disk space only is checked and hit Next.
  
- Next is which encryption mode. Most likely, you will never move this drive to a Windows operating system older than 10, so we will choose the new encryption mode and hit next.
  
- Now we begin the encryption process, which may take awhile, and the computer will restart. Click continue, and a popup will come out of the right side of the screen. Click it and click restart now. alternatively, if you missed the popup, right-click the windows button, hover over shut down or sign out, and press restart.
  
Obviously, now you will be kicked out of your remote desktop session. Wait around 30 seconds and try to log back in.
  
- Once back in, click File Explorer and this PC, then right-click Windows (C:), where a new option will be in place of turning on bitlocker; this one will say "Manage Bitlocker." Click it.
  
- If done right, you should see the drive icon this time with the padlock and key in it; the text will say BitLocker is on.
  
- We are going to make sure it is done, though. Right-click on the Windows icon and select "Windows Powershell (Admin)."
  
- In Powershell, type "manage-bde -status" and hit enter on the keyboard. A bunch of stuff will pop up, but look for the Percentage Encryption section. If it says 100%, then you are good to go and have completed this tutorial properly!
