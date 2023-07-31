- git config --global user.email <email>
- git config --global user.name <name>
- git config --global core.editor "code --wait" // Set Visual Studio Code as default editor
- git config --global core.autocrlf true
- git config --global commit.template ~/.gitmessage.txt
- git config --global --add safe.directory <Your Directory>
```markdown
Subject line (try to keep under 50 characters)

Multi-line description of commit,
feel free to be detailed.

[Ticket: X]
# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
# modified:   lib/test.rb
#
~
~
".git/COMMIT_EDITMSG" 14L, 297C
```

- git config --global core.pager '' // Git will the entire output of a command

## Finding your Key
```powershell
gpg --list-secret-keys --keyid-format=long
```
```markdown
sec   rsa4096/################ 2023-07-22 [SC]
      C6F9134A1AAADA228A26ECCA################
uid                 [ultimate] John Doe <username@hotmail.com>
ssb   rsa4096/################ 2023-07-22 [E]
```
> We need the part after the **sec rsa4096/** where **sec** stands for *security key*

### GPG Signing Key
- git config --global user.signingkey <gpg-key-id>
- git config --global commit.gpgsign true
- git config --global gpg.program <path to gpg.exe>

### Finding GPG Program
```powershell
where.exe gpg
```

## My .gitignore
```markdown
[user]
	email = username@hotmail.com
	name = John Doe             # Must equal your github Name (not username)
	signingkey = ################
[core]
	editor = code --wait
[commit]
	gpgsign = true
[safe]
	directory = Z:/Filmz
[gpg]
	program = C:\\Program Files (x86)\\GnuPG\\bin\\gpg.exe
```

help.autocorrect

# Powershell

### Set Execution Policy
Without running this script I usually run into trouble executing the following scripts in Powershell.
```powershell
Set-ExecutionPolicy Bypass -Scope LocalMachine
```
### Install Oh My Posh
```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
```

### (Alternative) Install Oh My Posh
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://ohmyposh.dev/install.ps1'))
```

### Initialize Oh My Posh | Default Theme
```powershell
oh-my-posh init pwsh | Invoke-Expression
```

### Set Custom Oh My Posh Theme
```powershell
oh-my-posh init pwsh --config 'C:/Users/Posh/<them-name-here>.omp.json' | Invoke-Expression
```

### Powershell Autocompletion
```powershell
Install-Module -Name PSReadLine
```

### PSReadLine | Change Arrow to Tab
```powershell
Set-PSReadLineKeyHandler -Chord "Tab" -Function ForwardWord
```

### Install IT Automation Tool **Carbon**
```powershell
Install-Module -Name 'Carbon' -AllowClobber
```

### Microsoft SQL Automation Tool
```powershell
Install-Module -Name dbatools
```

# Microsoft.Powershell_profile.ps1
```powershell
oh-my-posh init pwsh --config 'C:\Users\Tanglesites\AppData\Local\Programs\oh-my-posh\themes\spaceship.omp.json' | Invoke-Expression
Import-Module -Name Terminal-Icons

Set-PSReadLineKeyHandler -Chord "Tab" -Function ForwardWord
```


# Applications

### Windows Terminal
```powershell
winget install Microsoft.WindowsTerminal
```

### Git
```powershell
winget install Git.Git
```

### Visual Studio Code
```powershell
winget install Microsoft.VisualStudioCode
```

### Visual Studio Enterprise 2022
```powershell
winget install Microsoft.VisualStudio.2022.Enterprise
```

### Python
```powershell
winget install Python.Python.3.12
```
