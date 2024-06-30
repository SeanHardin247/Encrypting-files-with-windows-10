![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/10e72b0d-de1e-45fe-9328-4bdf08494feb)
# File encryption with Windows 10 virtual machines
This is a walkthrough on how to enable file encryption with Microsoft's built-in file encryption service "BitLocker". 
I will be using a Virtual Machine with a Microsoft cloud computing service called Azure. This walkthrough will also give you a quick tutorial on setting up a virtual machine with it. The reason behind this is that my device is old, and uses Windows 10 home, so i dont have the option to encrypt my files this way.
File encryption is very important for keeping files safe and out of the hands of people who could use them to harm a business if it is a work computer, or to harm you if it is a personal computer that gets stolen.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10 pro</b> (21H2)

**It is very important you select Windows 10 Pro and not Windows 10 Home when creating the VM**

<h2>Other applications used</h2>
 
  - PowerShell

<h2>Pre Setup steps</h2>


The first thing you need to do is go to and click on start free. Sign up with your Microsoft account and after getting through all of it you should receive $200 of free credit to use with Azure for a month.
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/c7dd62aa-a92a-423e-9f01-b88f7db743e0)

Once in Azure, click on the search bar and type "Virtual Machines" and click on the Virtual Machines option0
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/7b24e8f9-cc4d-4937-a6d6-efd76240d862)

Click create and choose the Azure Virtual Machine option. Down in the options name the Machine "VM1" and in the Image section make sure you select Windows 10 Pro
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/33ac5795-2850-437a-b992-db3c7f901c53)

Scroll down to size, you can pick whatever size you want to. If you dont care just pick "Standard_D2as_v4" you might need to click the see all sizes button to find it.
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/a64017f0-3e4c-458a-85d6-596e66011406)

Scroll further to username and password, make the username anything you like, ill make it Labuser for this demonstration. Make the password whatever you want, just remember it.
At the bottom check the box that you have a Windows 10 license
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/a947d5ac-3edb-43d1-91cd-9d6f09128a41)

Click review and create, and then create again. It will take a bit to deploy. Once its deployed click the go to resource option
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/7926882b-50f8-4c87-9c3b-367451b533a6)

Hover over the public IP address and click on the clip board option that appears.
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/6caedc2a-062e-471f-b4b0-47c89afa5f11)

Press the windows key on your device and type "Remote Deskstop" then press enter. Click show options on the tab that popped up and insert "labuser" or your Virtual Machines username and click on the field for the computer then hold Ctrl on your keyboard and press V.
![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/c5d60486-8435-4e85-a79b-796dfb57388a)

Now you will be prompted for the Virtual Machines password. Type it in and click ok. You will get a warning, click yes.

So you can connect to your Virtual Machine now, time for the main steps of how to encrypt files.

  <h2>Steps </h2>

- Connect to your Windows 10 virtual machine using remote desktop.

- Click on the file explorer icon on the taskbar.

- Select "This PC" on the left sidebar, and underneath the devices and drives section that pops up, right-click on Windows (C:).

- On the popup, click the Turn on BitLocker option with a shield next to it. If you do not see the BitLocker option, it is most likely because you are not using a Windows 10 Pro Virtual Machine

![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/baf170f1-902a-42c7-9208-06c338f2f973)

  
- We will perform a file backup before starting. When you get to the Preparing your drive for BitLocker screen, click on the underlined blue text that says "Use file history to perform a backup."

- Now a window will be brought up about file history. Click on the turn on button to turn on file history. Under the storage drive icon, it should say something along the lines of saving now, and when it's done, it will say "Files last copied on" and then the current date.

![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/8ff4bcc1-86d5-4291-83ea-759b5bd4da0d)

  
You can close this window now and return to the BitLocker window. Select Next and wait.

- Click next again. Now you will have an option to select how you want to back up your recovery key, which can save you if you can't get into your PC. In a real life scenario, you may want to print it or do all of these, but we will just choose the Save to File option.
Another window will open; this one is a file explorer window. We can't save this to an encrypted drive; that would be pointless since we need this key in case we can't get back into our encrypted files.

- On the left sidebar, Click This PC, double-click Temporary Storage (D:) *you may need to scroll down to find it*, and near the top, click New Folder. You can name this folder whatever you want, or not name it at all. Hit enter when finished naming.

![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/09aa2aee-dda0-491a-9eee-18efab7202e4)
  
- Double-click your new folder and hit save or enter on your keyboard. This will save your BitLocker recovery key.txt document.
  
- The next option in BitLockers setup is how much of our drive we want to encrypt. There is a lot of text explaining it, but the short version is that for new PCs, we want to select encrypt used disk space only and encrypt the entire drive for PCs that have been using it for awhile.
  
- Make sure Encrypt used disk space only is checked and hit Next.
  
- Next is which encryption mode. Most likely, you will never move this drive to a Windows operating system older than 10, so we will choose the new encryption mode and hit next.

- Check the option to run a Bitlocker system check, this will prompt you to restart once the encryption process begins. Start the encryption process and restart the computer when given the prompt to do so.

![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/a770bdbf-fbfe-4ac6-8b1c-a54e44482aff)


After restarting, you will be kicked out of your remote desktop session. try to log back in.

# Confirming that the files are encrypted

- Once back in, click File Explorer and this PC, then right-click Windows (C:), where a new option will be in place of turning on Bitlocker; this one will say "Manage Bitlocker." Click it.
  
- If done right, you should see the drive icon this time with the padlock and key in it; the text will say BitLocker is on or encrypting.

  ![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/f2b59cdc-d6bb-44fa-983b-cc00f9b39f32)

- We are going to make sure it is done. Right-click on the Windows icon and select "Windows Powershell (Admin)."
  
- In Powershell, type "manage-bde -status" and hit enter on the keyboard. A bunch of stuff will pop up, but look for the Percentage Encryption section. If it says 100%, then you are good to go and have completed this tutorial properly!

  ![image](https://github.com/SeanHardin247/Encrypting-files-with-windows-10/assets/172443627/e93f2d39-e297-46f9-9edd-5630283f0e69)

   

