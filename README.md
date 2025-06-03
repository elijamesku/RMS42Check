# RMS42Check

This README includes a PowerShell script that checks whether `RMSLauncher.exe` is installed on a Windows system.

This detection script verifies the existence of `RMSLauncher.exe` in the default installation directory:

C:\Program Files\RMS3\RMSLauncher.exe

It returns:
- Exit code `0` if the file is found
- Exit code `1` if the file is not found

Console messages are printed to indicate the result.

## Detection Script

Save this as `Check-RMSLauncher.ps1`:

```powershell
$filePath = "C:\Program Files\RMS3\RMSLauncher.exe"
if (Test-Path $filePath) {
    Write-Host "RMSLauncher.exe found."
    exit 0
} else {
    Write-Host "RMSLauncher.exe not found."
    exit 1

```

<br>
<br>

![RMS 3 Launcher Screenshot](Screenshot%202025-06-03%20094844.png)
<br><br>
