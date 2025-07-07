For some reason, it needs a 2nd run in powershell:

```
PS C:\Users\...> wsl --install --no-distribution
The requested operation requires elevation.
Installing: Virtual Machine Platform
Error: 0xc004000d
PS C:\Users\...> wsl --install --no-distribution
The requested operation requires elevation.
Installing: Virtual Machine Platform
Virtual Machine Platform has been installed.
Installing: Windows Subsystem for Linux
Windows Subsystem for Linux has been installed.
Installing: Windows Subsystem for Linux
Windows Subsystem for Linux has been installed.
The requested operation is successful. Changes will not be effective until the system is rebooted.
PS C:\Users\...>
```

```
PS C:\Users\...> wsl --list --verbose
This application requires the Windows Subsystem for Linux Optional Component.
Install it by running: wsl.exe --install --no-distribution
The system may need to be restarted so the changes can take effect.
Error code: Wsl/WSL_E_WSL_OPTIONAL_COMPONENT_REQUIRED
PS C:\Users\...>
```

`msinfo32` -> `System Information` -> `System Summary`

```
Hyper-V - VM Monitor Mode Extensions	Yes
Hyper-V - Second Level Address Translation Extensions	Yes
Hyper-V - Virtualisation Enabled in Firmware	No
Hyper-V - Data Execution Protection	Yes
```

Multiple reboots, to get this:

`ESC` BIOS settings, Advanced, switch on `VT-x` and `VT-d`.

```
PS C:\Users\...> wsl --list --online
The following is a list of valid distributions that can be installed.
Install using 'wsl.exe --install <Distro>'.

NAME                            FRIENDLY NAME
AlmaLinux-8                     AlmaLinux OS 8
AlmaLinux-9                     AlmaLinux OS 9
AlmaLinux-Kitten-10             AlmaLinux OS Kitten 10
AlmaLinux-10                    AlmaLinux OS 10
Debian                          Debian GNU/Linux
FedoraLinux-42                  Fedora Linux 42
SUSE-Linux-Enterprise-15-SP6    SUSE Linux Enterprise 15 SP6
SUSE-Linux-Enterprise-15-SP7    SUSE Linux Enterprise 15 SP7
Ubuntu                          Ubuntu
Ubuntu-24.04                    Ubuntu 24.04 LTS
archlinux                       Arch Linux
kali-linux                      Kali Linux Rolling
openSUSE-Tumbleweed             openSUSE Tumbleweed
openSUSE-Leap-15.6              openSUSE Leap 15.6
Ubuntu-18.04                    Ubuntu 18.04 LTS
Ubuntu-20.04                    Ubuntu 20.04 LTS
Ubuntu-22.04                    Ubuntu 22.04 LTS
OracleLinux_7_9                 Oracle Linux 7.9
OracleLinux_8_7                 Oracle Linux 8.7
OracleLinux_9_1                 Oracle Linux 9.1
PS C:\Users\...> wsl --install FedoraLinux-42
Downloading: Fedora Linux 42
Installing: Fedora Linux 42
Distribution successfully installed. It can be launched via 'wsl.exe -d FedoraLinux-42'
Launching FedoraLinux-42...
Please create a default user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: HMRWork42
Your user has been created, is included in the wheel group, and can use sudo without a password.
To set a password for your user, run 'sudo passwd HMRWork42'
```

```
PS C:\Users\...> wsl --version
WSL version: 2.5.9.0
Kernel version: 6.6.87.2-1
WSLg version: 1.0.66
MSRDC version: 1.2.6074
Direct3D version: 1.611.1-81528511
DXCore version: 10.0.26100.1-240331-1435.ge-release
Windows version: 10.0.19045.6036
PS C:\Users\...>
```
