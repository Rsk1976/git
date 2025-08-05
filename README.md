## clean list of filenames
```
dir /b
```
## other basic comments
https://g.co/gemini/share/cc1bbb2baed1


# to show the branch name
```
Install-Module posh-git -Scope CurrentUser -Force
```
type the line below, go to the file path 
```
$profile
```
then open notepad and copy & paste the below code
```bash
notepad $profile
```


```bash
function prompt {
    $branch = ''
    if (Test-Path .git) {
        $branch = & git rev-parse --abbrev-ref HEAD 2>$null
        if ($branch) {
            # Add ANSI escape codes for green color
            $branch = "$([char]27)[32m($branch)$([char]27)[0m"
        }
    }
    "$PWD $branch> "
}
```
finally run this line
```
Get-ExecutionPolicy
```
```
Set-ExecutionPolicy RemoteSigned CurrentUser
```

https://youtu.be/Vdd3b4TwaI4?si=THYUJQaOc5OW7Jb7
