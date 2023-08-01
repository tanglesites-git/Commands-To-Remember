# Commands

## DOTNET CLI

### Create a Soltion
```powershell
dotnet new sln -n <SolutionName>
```

### Create a NEW Webapi Project
```powershell
dotnet new webapi -n <ProjectName>
```

### Create a NEW Webapi Project with no HTTPS and  Usaing Minimal API's
```powershell
dotnet new webapi -n <ProjectName> --no-https -minimal
```

### Create Class Library
```powershell
dotnet new library -n <ProjectName>
```


## POWERSHELL COMMANDS

### Create a file 
```powerhsell
ni <filename>
```


## GIT COMMANDS

### CHECK STATUS (VERBOSE)
```powershell
git status -u
```


### ADD FILE TO STAGING
```powerhsell
git add <filename>
```

### DELETE BRANCH
```powershell
git branch -d <branch_name>
```

### DELETE BRANCH --FORCE
```powerhsell
git branch -D <branchname> or feature/branchname
```