
## Guide on how to install and basically set up WSL 2, Windows Terminal, Ubuntu, Visual Studio Code on Windows 10
**WSL** stands for Windows Subsystem for Linux.
WSL version **1** uses *translation layer* to communicate with Windows.
WSL version **2** uses *virtualization technology* to communicate with Windows.

1. Open Windows features in Control Panel.

2. Check two checkboxes with labels:
- *Virtual Machine Platform*,
- *Windows Subsystem for Linux*
and click OK.

3. Download the Linux kernel update package from [here](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) and install it.

4. Set version 2 of WSL as your default version
using the command in Powershell:
`wsl --set-default-version 2`

5. Install *Ubuntu* from Micorosft Store.

6. Install *Windows Terminal* from Micorosft Store.

7. Install *Visual Studio Code* from [official website](https://code.visualstudio.com/).

8. Launch Ubuntu app.

9. Type new username and new password.

10. Create .hushlogin file using the command:
`touch ~/.hushlogin`

11. Update system using the command:
`sudo apt-get update -y && sudo apt-get upgrade -y && sudo apt-get dist-upgrade -y`

12. Change default profile in Windows Terminal settings to Ubuntu.

13. Install ZSH (Z shell) - Unix shell using the command:
`sudo apt-get install zsh`

14. Type `zsh` and then `2` to set up ZSH's configuration.

15. Set ZSH as the default shell using the command:
`chsh -s $(which zsh)`

16. Install slimzsh - configuration for ZSH using the command:
`git clone --recursive https://github.com/changs/slimzsh.git ~/.slimzsh`

17. Set slimzsh as your default configuration:
`nano ~/.zshrc`
*#Add new line:*
`source "$HOME/.slimzsh/slim.zsh"`
*#Add new line:*
`alias update="sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade"`

18. Install Fasd tool using the command:
`sudo apt-get install fasd`

19. Open Visual Studio Code.

20. Open the Command Palette using the shortcut: "Ctrl+Shift+P".
Search for *Open Settings (JSON)* and choose it to open your `settings.json` file.

21. Add 3 settings:
`{
    "terminal.integrated.defaultProfile.windows": "Ubuntu (WSL)",
    "terminal.integrated.tabs.enabled": true,
    "terminal.integrated.copyOnSelection": true,
}`

22. Install *Remote - WSL* extension.

23. Open Terminal>New Terminal (Ctrl+Shift+`).

**Basic commands**:
- `sudo <command>` "superuser do" - allows a permitted user
to execute a command as the superuser or another user
- `su <username>` "substitute user" - changes the current user to another user
- `man <command>` "manual page" - form of software documentation
- `pwd` "print working directory" - prints name of current/working directory
- `mkdir <...path/directory_name>` "make directory" - makes directory/ies
- `touch <...path/file_name>` *touch of a magic wand* -  creates new file (if it doesn't already exist)
- `cd <...path/directory_name>` "change directory" - switches current/working directory to another
- `clear` - clears the terminal screen
- `nano <...path/file_name>` - small editor for the terminal
- `ls` - lists content of current/working directory
- `cat <...path/file_name>` "concatenate" - concatenates files and prints their contents

**Materials used**:
- https://www.youtube.com/watch?v=g1XbI-CjGcI&ab_channel=helloroman
- https://www.youtube.com/watch?v=_fntjriRe48&ab_channel=DavidBombal
- https://docs.microsoft.com/en-us/windows/wsl/install-win10
- https://fireship.io/lessons/windows-10-for-web-dev/
- https://askubuntu.com/questions/131823/how-to-make-zsh-the-default-shell
- https://askubuntu.com/questions/733434/one-single-command-to-update-everything-in-ubuntu
- https://en.wikipedia.org/wiki/Z_shell
- https://en.wikipedia.org/wiki/Man_page
- https://en.wikipedia.org/wiki/Su_(Unix)
- https://en.wikipedia.org/wiki/Sudo
- https://en.wikipedia.org/wiki/Touch_(command)
- https://en.wikipedia.org/wiki/Pwd
- https://en.wikipedia.org/wiki/Cat_(Unix)
- https://github.com/changs/slimzsh
- https://github.com/clvv/fasd
