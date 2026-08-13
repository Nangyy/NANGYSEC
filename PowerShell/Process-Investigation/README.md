# PowerShell Process Investigation

## 🎯 Objective

The goal of this lab was to learn how to investigate
running processes on a Windows system using PowerShell.

## 💻 Environment

- Windows
- PowerShell
- Oracle VirtualBox

## 🛠️ Commands Practiced

- `Get-Process`
- `Sort-Object`
- `Select-Object`
- `Where-Object`
- Process IDs (PIDs)

## 🔎 What I Did

I used PowerShell to:

1. List running processes.
2. Sort processes based on CPU usage.
3. Identify individual processes using their PIDs.
4. Filter processes based on CPU usage.

## 💻 Commands Used

```powershell
Get-Process

Get-Process | Sort-Object CPU -Descending

Get-Process -Id <PID>

Get-Process | Where-Object {$_.CPU -gt 5}
📸 Evidence
Screenshots of the lab will be added here to document the commands and results.
🧠 What I Learned
I learned how to use PowerShell to inspect processes running on a Windows system and how Process IDs (PIDs) can be used to investigate individual processes.
🚀 Future Improvements
Investigate suspicious processes.
Examine process paths.
Learn more about Windows event logs.
Build a PowerShell investigation script.
