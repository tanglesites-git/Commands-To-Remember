<h1 style="font-size: 3rem; text-align: center;">ROUTINES</h1>
<h3 style="font-size: 1.5rem; text-align: center;">Because I Forget</h3>

# TOC
- [Commit and Push Submodule](#commit-and-push-submodule)

# Commit and Push Submodule

> - Do some work in submodule

## Navigate to submodule
```powershell
cd ./path/to/submodule
```

## Check Your Status
```powerhsell
git status -S -u
```

## Add and Commit
```powershell
git add -A;git commit -S -m "A commit Message"
```

## Update Submodule
```powershell
cd /path/to/working_directory
git submodule update --remote --merge
```

## Push to Remote
```powershell
cd /path/to/submodule
git push origin main
```

## Commit Updated Refs to Submodule
```powershell
git add ./path/to/submodule
git commit -S -m "Message"
```

## Push to Remote
```powershell
git push origin main
```

# Merge Pull Request

```powershell
git pull origin main
git checkout main
git merge dev
git push -u origin main
```