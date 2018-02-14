# Integrate SourceTree for Windows and GitHub

## Commands

These scripts provide new custom actions that add various context-menus to SourceTree for Windows
in order to provide better integration with GitHub. They are:

* View commit on GitHub
* View file commit on GitHub
* View file on GitHub
* View repo on GitHub

## Installation

Check out the scripts to somewhere convenient, e.g. `c:\scripts`

### Option 1
Go into *Tools > Options* in SourceTree for Windows then add new custom actions:

Menu caption | Parameters
-------------|-------------
View commit on GitHub | -noprofile -file c:\scripts\view-commit-on-github.ps1 $REPO $SHA
View file on GitHub | -noprofile -file c:\scripts\view-file-on-github.ps1 $FILE
View file commit on GitHub | -noprofile -file c:\scripts\view-file-commit-on-github.ps1 $REPO $SHA $FILE
View repo on GitHub | -noprofile -file c:\scripts\view-repo-on-github.ps1 $REPO


Each one should also specify:
* Open in a separate window: unchecked
* Show Full Output: unchecked
* Script to run: powershell.exe

### Option 2
* Copy the sample [customactions.xml](https://github.com/damieng/DamienGKit/blob/master/Powershell/SourceTree/customactions.xml) to `%LOCALAPPDATA%\Atlassian\SourceTree`
* Update the path to the scripts as necessary

## Notes
* You may need to restart SourceTree for the custom actions to show in the menus.
* Does not currently work predictably with multiple remote repositories.
