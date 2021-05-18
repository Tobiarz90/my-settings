1. Open Windows Powershell as Administrator.

2. Run the command:
`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`

3. Type `Y` to reboot your PC.

4. Install Ubuntu from Micorosft Store.

5. Install Windows Terminal from Micorosft Store.

6. Install Visual Studio Code from [official website](https://code.visualstudio.com/).

7. Launch Ubuntu app.

8. Type new username and new password.

9. Create .hushlogin file using the command:
`touch ~/.hushlogin`

10. Update system using the command:
`sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade`

11. Change default profile in Windows Terminal settings to Ubuntu.

12. Install ZSH (Z shell) - Unix shell using the command:
`sudo apt-get install zsh`

13. Type `zsh` and then `2` to set up ZSH's configuration.

14. Set ZSH as the default shell using the command:
`chsh -s $(which zsh)`

15. Install slimzsh - configuration for ZSH using the command:
`git clone --recursive https://github.com/changs/slimzsh.git ~/.slimzsh`

16. Set slimzsh as your default configuration:
`nano ~/.zshrc`
*#Add new line:*
`source "$HOME/.slimzsh/slim.zsh"`
*#Add new line:*
`alias update="sudo apt-get update && sudo apt-get upgrade && sudo apt-get dist-upgrade"`

17. Install Fasd tool using the command:
`sudo apt-get install fasd`

18. Open Visual Studio Code.

19. Open the Command Palette using the shortcut: "Ctrl+Shift+P",
type: "open settings json" and click ENTER to open your `settings.json` file.

20. Add 3 settings:
`{
    "terminal.integrated.defaultProfile.windows": "Ubuntu (WSL)",
    "terminal.integrated.tabs.enabled": true,
    "terminal.integrated.copyOnSelection": true,
}`

21. Open Terminal>New Terminal (Ctrl+Shift+`)


MATERIALS USED:
- https://www.youtube.com/watch?v=g1XbI-CjGcI&ab_channel=helloroman
- https://fireship.io/lessons/windows-10-for-web-dev/
- https://askubuntu.com/questions/131823/how-to-make-zsh-the-default-shell
- https://askubuntu.com/questions/733434/one-single-command-to-update-everything-in-ubuntu
- https://en.wikipedia.org/wiki/Z_shell
- https://github.com/changs/slimzsh
- https://github.com/clvv/fasd
