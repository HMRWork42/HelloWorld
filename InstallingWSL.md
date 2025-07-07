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

Hyper-V - VM Monitor Mode Extensions	Yes
Hyper-V - Second Level Address Translation Extensions	Yes
Hyper-V - Virtualisation Enabled in Firmware	No
Hyper-V - Data Execution Protection	Yes
