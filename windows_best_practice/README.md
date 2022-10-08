# Windows Best Practice

## Debloat Windows

This is a stepwise description of how to "clean up" or more accurately "debloat" Windows. This will work all the way from Windows 7 to Windows 10.

### Without Tools

All the tools are built into windows and it is thus not necessary to install any tools from the internet. The build in tools are as follows:

- The <strong>Run</strong> menu which can be opened using the shortcut Windows+R keys. It is also possible to just search for it in the search-bar in windows.
- <strong>Task Manager</strong>
- <strong>Task Scheduler</strong>
- Cleanup of startup programs using the <strong>Task Manager</strong>. This can be popened using the shortcut Ctrl+Shift+Escape. Under <em>“Startup”</em> disable the applications you are not using.

### Run menu:

Searching <em>shell:startup</em> (this is the user startup) and/or <em>shell:common</em> startup (this is the startup for all users on the system) in the <strong>Run</strong>-menu the programs opened when the pc is booted are located here. Removing a tool in the folder will not delete it, but prevent it from starting up. If there are tools that are unnecessary to run on startup or that you are unfamiliar with, just remove it/them from the folder.

Searching <em>regedit</em> opens the Registry Editor. In there the <em>HKEY_CURRENT_USER</em> is our current user and <em>HKEY_LOCAL_MACHINE</em> is the current machine thus all the users located on the machine. Located in <em>Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Run</em> the run commands for our current user are located (note: change the <em>HKEY_CURRENT_USER</em> with <em>HKEY_LOCAL_MACHINE</em> and the run commands for the local machine can be located). If it is bloated with unnecessary commands, clean them up.

### Task Scheduler:

In the <strong>Task Scheduler</strong> under <strong>Task Scheduler Library</strong> processes/tasks running in the background are located. Disable the ones that are not necessary to be running such as automatic updates, edge and crash reports.

- <strong>NOTE: do not Delete but Disable the tasks. If we Delete the tasks we risk that when a program using the tasks is run, the tasks will be recreated and be Run.</strong>

### Cleanup of actual machine:

In the <strong>Run</strong> menu search <em>appwiz.cpl</em> which opens the old version of the uninstall menu (the newer ones can also be used). Uninstall unnecessary or unused programs.

Windows debloater script:
https://www.christitus.com/debloat-windows-10-2020
