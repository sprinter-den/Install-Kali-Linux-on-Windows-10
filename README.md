# Установка Kali Linux на Windows 10

# 🔦🔦COMMANDS🔦🔦

# Включение Hyper-V с помощью PowerShell

      Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All 
  
## Включение Hyper-V с помощью CMD и DISM

     DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V

## Установка WSL 2

#В POWERSHELL от имени  administrator 

     Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

   RESTART

     dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

     dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

   RESTART

#Download Linux Kernel: 

      Invoke-WebRequest -Uri https://aka.ms/wsl-kali-linux-new -OutFile Kali.appx -UseBasicParsing
Скачавшийся фаил appx установить и продолжьть
  [Linux Kernel](https://github.com/sprinter-den/Install-Kali-Linux-on-Windows-10/raw/main/wsl_update_x64.msi "Download Linux Kernel")
      

      wsl --set-default-version 2

#CHECK VERSION 

      wsl --list --verbose

#Установка GUI

      sudo apt update && sudo apt upgrade -y

      sudo apt install kali-desktop-xfce -y

#XRDP

      sudo apt install xrdp -y

      sudo service xrdp start
      
#Displey

            sudo apt update && sudo apt install -y kali-win-kex
            
#start displey

            kex
[Cicada3301](https://github.com/Cicadadenis/)
