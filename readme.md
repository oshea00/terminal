# Windows Terminal Stuff

profiles.json - terminal settings

save to ```C:\Users\<username>\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState```

# Build from source

- Clone the repo
➜  git clone https://github.com/microsoft/terminal.git
- Init submodules as per the README
➜  git submodule update --init --recursive
- Kick off the build in PowerShell
➜  git submodule update --init --recursive
```
Submodule 'dep/gsl' (https://github.com/microsoft/gsl) registered for path 'dep/gsl'
Submodule 'dep/wil' (https://github.com/microsoft/wil) registered for path 'dep/wil'
Cloning into '/mnt/c/Users/Gamer/repos/terminal/dep/gsl'...
Cloning into '/mnt/c/Users/Gamer/repos/terminal/dep/wil'...
Submodule path 'dep/gsl': checked out 'b74b286d5e333561b0f1ef1abd18de2606624455'
Submodule path 'dep/wil': checked out 'fbcd1d2abb558da4564ce343b688f7a658f51318'
```
- Import-Module .\tools\OpenConsole.psm1
- Set-MsBuildDevEnvironment
- Invoke-OpenConsoleBuild
