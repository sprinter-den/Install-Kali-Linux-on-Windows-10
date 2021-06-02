# Установка Kali Linux на Windows 10

#  🔦🔦🔦COMMANDS:🔦🔦🔦

1. Установка WSL 2

В POWERSHELL от имени  administrator

⚙️ Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

RESTART

⚙️ dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

⚙️ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

RESTART

Download Linux Kernel: https://aka.ms/wsl2kernel

⚙️ wsl --set-default-version 2

CHECK VERSION 
⚙️ wsl --list --verbose

2. Установка GUI

⚙️ sudo apt update && sudo apt upgrade -y

⚙️ sudo apt install kali-desktop-xfce -y

XRDP

⚙️ sudo apt install xrdp -y

⚙️ sudo service xrdp start