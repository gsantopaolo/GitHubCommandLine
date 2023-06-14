Add Existing code to a new repo
===== 


1. Create a new repository on GitHub. To avoid errors, do not initialize the new repository with _README_, license, or _gitignore
1. remember to add the appropriate .gitignore file
1. Open Git Bash
1. Change the current working directory to your local project.
1. Initialize the local directory as a Git repository.
 `$ git init`
1. Add the files in your new local repository. This stages them for the first commit.
`$ git add .`
1. Commit the files that you've staged in your local repository.
`$ git commit -m "First commit"`
1. At the top right of the GitHub repositoryclick on _Clone or Download_ and then click the 

to copy the remote repository URL.

1. In the Command prompt, add the URL for the remote repository where your local repository will be pushed.
```
$ git remote add origin THE_URL_YOU_COPIED
$ git remote -v
```
9. Push the changes in your local repository to GitHub.
`$ git push origin master`

Check out a remote Git branch
===== 


```
$ git fetch
```

The coomand below will fetch all the remote branches. 
```
$ git branch -v -a

remotes/origin/test
```

Branches stating with remotes/* are branches on the server. 
With the switch command below it is possible to checkout the romote branch

```
$ git switch test
```

In case of multiple remotes see article below https://stackoverflow.com/questions/1783405/how-do-i-check-out-a-remote-git-branch

Overwrite local files and get everithing from server
==
`git fetch --all`

Then, you have two options:

`git reset --hard origin/master`

OR If you are on some other branch:

`git reset --hard origin/<branch_name>`

Untrack files already added to git repository based on .gitignore
==

Step 1: Commit all your changes
-
Before proceeding, make sure all your changes are committed, including your .gitignore file.

Step 2: Remove everything from the repository
-
To clear your repo, use:
`git rm -r --cached .`

rm is the remove command
-r will allow recursive removal
–cached will only remove files from the index. Your files will still be there.
The . indicates that all files will be untracked. You can untrack a specific file with git rm --cached foo.txt (thanks @amadeann).
The rm command can be unforgiving. If you wish to try what it does beforehand, add the -n or --dry-run flag to test things out.

Step 3: Re add everything
- 
`git add .`

Step 4: Commit
-

`git commit -m ".gitignore fix"`

Step 5: Remove local untracked files from the current Git branch
-

```
git clean -f
git clean -fd
git clean -fX
git push origin master
```


you now have a clean repo!
 
Launch Jupyter Notebook from Windows command line
===== 
```python -m notebook```

Pufhing the local work to the remote banch
===== 
```git add .
git commit -m "YOUR COMMENT"
git push origin master
```


Creates a conda env with all the base needed
===== 
```

Pufhing the local work to the remote banch
===== 
```
conda create --name YOUR_ENV_NAME python=3.11.3
```


