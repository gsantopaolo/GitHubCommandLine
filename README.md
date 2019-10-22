Add Existing core to a new repo
===== 


1. Create a new repository on GitHub. To avoid errors, do not initialize the new repository with _README_, license, or _gitignore
1. Open Git Bash
1. Change the current working directory to your local project.
1. Initialize the local directory as a Git repository.
 `$ git init`
1. Add the files in your new local repository. This stages them for the first commit.
`$ git add .`
1. Commit the files that you've staged in your local repository.
`$ git commit -m "First commit"`
1. At the top right of the GitHub repositoryclick on _Clone or Download_ and then click the 

![image.png](/.attachments/image-23cd624e-4629-4188-b422-480b5d9b2661.png) to copy the remote repository URL.
![image.png](/.attachments/image-a0df0f85-ac0c-42f8-b380-561cc6685f49.png)
1. In the Command prompt, add the URL for the remote repository where your local repository will be pushed.
```
$ git remote add origin THE_URL_YOU_COPIED
$ git remote -v
```
9. Push the changes in your local repository to GitHub.
`$ git push origin master`



git pull to overwrite local files
==
`git fetch --all`

Then, you have two options:

`git reset --hard origin/master`

OR If you are on some other branch:
`git reset --hard origin/<branch_name>`