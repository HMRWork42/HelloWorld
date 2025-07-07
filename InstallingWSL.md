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
