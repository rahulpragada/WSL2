# WSL2
Windows Subsystem for Linux
WSL - Windows Subsystem for Linux
We could easily configure linux distributions and use them in parallel to Windows OS.
Let's see how do we setup WSL2 for Windows

Open Windows Powershell in Administrator mode
Enter the below command to install wsl2 
```wsl.exe --install```

# For older versions
1. Check requirements for running WSL 2
Windows 10 or 11 - Version 1903 or later, with Build 18362.1049 or later

2. Enable the Virtual Machine Platform
```dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart```

3. Enable Virtual Machine Feature
```dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart```

4. Install wsl2
```wsl.exe --install```
To update
```wsl.exe --update```
We could also install wsl2 through microsoft store
Go to Microsoft Store and search for ```Windows Subsystem for Linux```

6. Set wsl2 as the default version
```wsl.exe --set-default-version 2```

7. Choose the linux distribution
```wsl.exe --list --online```
Install Kali Linux
```wsl.exe --install kali-linux```
Set the default distribution to Kali Linux
```wsl.exe -d kali-linux```

It is also available as an application
Go to Microsoft Store and search for "Kali Linux"
Install the application and run it
Create a new Username and a Password
You are ready to go with the Kali Linux WSL2

Update all the packages
```sudo apt update && sudo apt upgrade -y```

For further documentation, visit https://learn.microsoft.com/en-us/windows/wsl/


# For GUI
Win-KeX provides a GUI desktop experience for Kali Linux in Windows Subsystem for Linux (WSL 2) with the following features:

# Window mode
Start a Kali Linux desktop in a dedicated window
# Seamless mode
Share the Windows desktop between Windows and Kali application and menus
# Enhanced session mode
Similar to Hyper-V, uses RDP for a more feature rich experience
  * Sound support
  * Shared clipboard for cut and paste support between Kali Linux and Windows
  * Root & unprivileged session support
  * Multi-session support: root window & non-privileged window & seamless sessions concurrently
  * Fully compatible with WSLg

Installing win-kex
```sudo apt install kali-win-kex -y```

To start Win-Kex in window mode
```kex --win -s```

To start Win-Kex in Seamless mode
```kex --sl -s```

To start Win-Kex in Enhanced Session Mode
```kex --esm --ip -s```

If there is any issue in the usage of Win-Kex 
Remove the package and re-install it
```sudo apt remove kali-win-kex -y```
```sudo apt install kali-win-kex -y```

For further documentation, visit https://www.kali.org/docs/wsl/win-kex/
