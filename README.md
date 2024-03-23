# How-To-GitHub-Basically

## Description

How-To-GitHub-Basically

(Assumes Using Windows 11

and

Visual Studio Code)

## Content

Powershell

Windows Subsystem for Linux

IDE (Integrated Development Environment) (Visual Studio Code)

git bash

GitHub

Goes through simple setup for version control system

Goes through some simple git commands

Refers to some commands which can delete so to be used with caution

towards the end of this document.

Use at your own risk.

## Purpose

Provide dedicated beginner with a somewhat beginner friendly reference to some 

common commands and a few issues / workarounds / fixes possibly encountered along the way.

Not suitable for any production or important work just for learning purposes.

Warning: some commands (especially towards the end of document) may not be suitable for all projects, so be very careful!

Intended for very informal reference purposes only and to possibly avoid having to dig through 

the much more extensive, offical git-scm.com documentation, for example.

This is very much not an official reference in any sense.

Errors and omissions accepted.

## Steps

1. [Go to Windows website to get Powershell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4#install-powershell-using-winget-recommended)

2. Download Powershell using commands given: `winget search Microsoft.PowerShell`

3. Add folder with Powershell.exe to Windows System Environment Variables > Path by clicking `New`

4. [Click here to go to Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install)

5. Copy command `wsl --install`

6. Open Powershell

7. Paste Command `wsl --install` into Powershell

8. [Download git bash](https://git-scm.com/downloads)

9. Install git bash

10. Add git bash install folder for git bash to System Environment Variables on Windows

11. [Download an IDE like Visual Studio Code](https://code.visualstudio.com/)

12. Install IDE (e.g. VSCode)

13. Add VSCode folder to System Environment Variables

14. [Go to GitHub](https://github.com/)

15. Sign up for GitHub Account

16. Create new Repository

17. Click Dropdown arrow beside Clone Button

18. Copy Repository url from Clone dropdown

19. Open IDE (e.g. VSCode)

20. Open integrated terminal

21. If (base) shows (due to Anaconda installed) type `deactivate`

22. Click cog wheel in bottom left corner for settings

23. Sync Visual Studio Code with GitHub

24. (May need to Install some Recommended Extensions) (go to left vertical column and click on symbol of blocks about 5th from the top)

25. In Integrated Terminal: type: `git clone` and then space and Paste url content Copied from GitHub Clone Button into integrated terminal in Visual Studio Code

26. Press Enter (this will clone repo)

27. Click File > Add New File > name it README.md (if not already in repository)

28. In terminal: Type the following 3 git commands pressing enter after each

29. `git add .`

30. `git commit -m "Add README md file"`

31. `git push`

32. `git status`

33. `git pull`

Optional commands (for later reference) for cloning another repository into local and then pushing to own repository:

34. To clone another repository: 

35. Clone the repo from [other repository to be cloned] to your local machine as follows:

36. Click dropdown arrow beside green clone button on repository to be cloned, and copy <url ending in .git>

37. Create a new repo at github.

38. To **Setup own remote repository:** Go to GitHub.com > Login > Click New Repository > (in this case: do not make any edits on opening screen (apart from name and setting public or private) to get to screen with "If you've done this kind of thing before, then copy url .git)

39. VSCode > File > New Window

40. Set up local folder

41. **In VSCode:** Go to left vertical column, click third image from top to go to git commands GUI (Graphic User Interface) (can either use this or the equivalent terminal commands [git clone <paste repo url with .git ending from Clone buitton drropdown menu on GitHub>](https://git-scm.com/docs/git-clone) interchangeably)

42. if using GUI Click Clone, paste url copied from GitHub Repository to be cloned into the window that appears, click Enter to clone into currently selected local folder.

### Disconnect from cloned repo remote repository:

43. `git remote rm origin` [StackOverflow | How to remove origin from git repository](https://stackoverflow.com/questions/9224754/how-to-remove-origin-from-git-repository)

### Connect to own new repository remote repository on GitHub:

44. `$ git remote set-url origin http://github.com/YOU/YOUR_REPO` [StackOverflow](https://stackoverflow.com/questions/18200248/cloning-a-repo-from-someone-elses-github-and-pushing-it-to-a-repo-on-my-github)

45. `git remote -v` to check if there is one line ending in (fetch) and one ending in (push) (2 lines total). If there are 4 lines, then can remove the lines not beginning with origin.

46. If get error this site contains instructions to fix and is also a reference for commands mentioned here. [How to fix ‘fatal: remote origin already exists’ Git error](https://komodor.com/learn/how-to-fix-fatal-remote-origin-already-exists-error/)

### Miscellaneous commands possibly needed:

47. Reference for following commands: [Git push existing repo to a new and different remote repo server?](https://stackoverflow.com/questions/5181845/git-push-existing-repo-to-a-new-and-different-remote-repo-server)

48. `git remote rename origin upstream`

49. `git remote add origin URL_TO_GITHUB_REPO`

50. `git push origin master`

### Further miscellaneous commands:

51. `git checkout <commit>` full command: with optional flags: [git checkout [-q] [-f] [-m] [--detach] <commit>](https://git-scm.com/docs/git-checkout)

52. Partial command: `git merge` Reference: [git merge | git-scm.com](https://git-scm.com/docs/git-merge)

Side note:

from git merge reference above:

Can use the following commands with CAUTION if read up a bit on them first here and possibly elsewhere in certain situations:

```bash
--ff
--no-ff
--ff-only
```

```text
Specifies how a merge is handled when the merged-in history is already a descendant of the current history. --ff is the default unless merging an annotated (and possibly signed) tag that is not stored in its natural place in the refs/tags/ hierarchy, in which case --no-ff is assumed.

With --ff, when possible resolve the merge as a fast-forward (only update the branch pointer to match the merged branch; do not create a merge commit). When not possible (when the merged-in history is not a descendant of the current history), create a merge commit.

With --no-ff, create a merge commit in all cases, even when the merge could instead be resolved as a fast-forward.

With --ff-only, resolve the merge as a fast-forward when possible. When not possible, refuse to merge and exit with a non-zero status.
```

53. Partial command: `git branch` Reference: [git branch | git-scm.com](https://git-scm.com/docs/git-branch)

54.  `git reset --soft HEAD` or `git reset --soft <commit to revert to>` (Note: soft means not permanent, and can undo if wrong, however, next command uses hard, which cannot be undone, so proceed with Caution!)

55. **WARNING!!**, be very careful with this one, as it **DELETES!!** things: `git reset --hard` to undo last commit, OR: **To go back multiple commits!**: `git reset --hard <commit-hash>` [Be aware that the git reset –hard HEAD or git reset –hard HEAD@{n} command would remove your uncommitted changes, even if you staged them. If you don’t want your unstaged changes to be removed, you can use the --soft flag instead of the --hard flag. | Git Reset Hard – How to Reset to Head in Git | freeCodeCamp](https://www.freecodecamp.org/news/git-reset-hard-how-to-reset-to-head-in-git/)

____

Update 18-01-2024:

The following may be needed to make WSL, VSCode, git and GitHub work together effectively:

[Install the GitHub Pull Requests and Issues extension](https://code.visualstudio.com/docs/sourcecontrol/github) in VSCode

In addition to point 4. above, 

(namely [PowerShell `wsl --install`](https://learn.microsoft.com/en-us/windows/wsl/install))

Also, if this error happens:

[WSL broken with "Class not registered" code 4294967295 (0xffffffff) #8268](https://github.com/microsoft/WSL/issues/8268)

```text
To fix "Class not registered" error, I only repair WSL on "Settings > Applications > Instaled Applications > Windows Subsystem for Linux > Advanced Options > Repair". After do that, my WSL command returned to work.
```

```text

To fix "Class not registered" error, I only repair WSL on "Settings > Applications > Instaled Applications > Windows Subsystem for Linux > Advanced Options > Repair". After do that, my WSL command returned to work.

I ended up having to uninstall Windows Subsystem for Linux from here, disable the windows feature (start menu > Turn windows features on or off), reboot, then re-enable it

```

Summary:

In addition to toggling on and off wsl in turn Windows Features on or off in Control Panel: 

- Windows PowerShell 2.0

- open PowerShell (may need to run as Admin)

- wsl --install

- reboot

Other references for this:

Search: [PS C:\WINDOWS\system32> wsl --install Class not registered Error code: Wsl/CallMsi/REGDB_E_CLASSNOTREG](https://www.google.com/search?q=PS+C%3A%5CWINDOWS%5Csystem32%3E+wsl+--install+Class+not+registered+Error+code%3A+Wsl%2FCallMsi%2FREGDB_E_CLASSNOTREG&oq=PS+C%3A%5CWINDOWS%5Csystem32%3E+wsl+--install+Class+not+registered+Error+code%3A+Wsl%2FCallMsi%2FREGDB_E_CLASSNOTREG&gs_lcrp=EgZjaHJvbWUyBggAEEUYOdIBBzQzMWowajeoAgCwAgA&sourceid=chrome&ie=UTF-8)

[WSL broken with "Class not registered" code 4294967295 (0xffffffff) #8268](https://github.com/microsoft/WSL/issues/8268)

[How to deal with the problem: “Error code: Wsl/CallMsi/REGDB_E_CLASSNOTREG”](https://learn.microsoft.com/en-us/answers/questions/1462932/how-to-deal-with-the-problem-error-code-wsl-callms)

[Error code: Wsl/CallMsi/REGDB_E_CLASSNOTREG #10882](https://github.com/microsoft/WSL/issues/10882)

[How can I fix WSL.exe sudden corruption in unknown DLL giving error 0x80040154 on Win11](https://superuser.com/questions/1776891/how-can-i-fix-wsl-exe-sudden-corruption-in-unknown-dll-giving-error-0x80040154-o)

____

Update: 23-03-2024

```bash
git remote set-url origin <git url here>
```

gives:

```bash
error: No such remote 'origin'
```

Reason:

here:

[](https://stackoverflow.com/questions/25503017/why-does-git-tell-me-no-such-remote-origin-when-i-try-to-push-to-origin)

basically:

1 - You never told Git to start tracking any file

For that you need to stage the files of interest, using:

```bash
git add .
```

```bash
git commit -m "some descriptive message"
```

2 - You haven't set up the remote repository

see StackOverflow:

[Why does Git tell me "No such remote 'origin'" when I try to push to origin?](https://stackoverflow.com/questions/25503017/why-does-git-tell-me-no-such-remote-origin-when-i-try-to-push-to-origin)

____

## References

[freeCodeCamp](https://www.freecodecamp.org/)

[git-scm.com](https://git-scm.com/)

[stackoverflow](https://stackoverflow.com/)

[learn.microsoft.com](https://learn.microsoft.com/en-us/)

[Visual Studio Code](https://code.visualstudio.com/)
