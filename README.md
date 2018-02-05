
# Github site by Katherine Duchesneau

## Questions from Jeff

### 1. When should you use Git for a project?

Git is a great method to keep track of previous copies of a project. Everything that is commite will be kept using version control and it will always be possible to go back to previous versions. It helps keep track of what has been done. This can be particularly useful when working in a group since many people will be modifying the same files. Version control allows you to keep copies of previous files, assign changes to particular collaborators, and keeps tract of program versions and results at each step. If the work is left for a long time and the exact details are forgotten, records of of the previous work are easily accessible accessible. Additionally, conflicting changes made by two collaborators can be intergrate together! All of this makes git great for any project between collaborators who want to keep track of their code for stats, programming, or even copies of their writing kept in .txt format.

### 2. What kind of files/info should be saved in a Git repository? What types of files/info should not be included in a Git repo?

Git public repositories can contain text files with code, and information that is not sensitive. They should not contain large files and sensitive or personal information, unless you get a private repository. Note, however, that private repositories are still stored on external servers. 


### 3. What are the commands to undo a commit?

```
$ git commit -m "a bad commit"              
$ git reset HEAD~1     
```
THEN
```
$ git add .                                              
$ git commit -c ORIG_HEAD                                   
```
This way will keep the changes that were bad (the commited file will still be staged), but will no longer be the master while you change your file. 
If you want to entierly delete the commited file (although theres still ways to get it back after), instead of `$ git reset HEAD~1` you can use `$ git reset --hard HEAD~1`. This will return the file to its state before the state seen in your bad commit.

[Citation](https://stackoverflow.com/questions/927358/how-to-undo-the-most-recent-commits-in-git)


### 4. One of your repositories is in a “detached HEAD” state. How do you fix this?

You have a few choices depending on what you want to do. 
If you want to return to the branch you came from `git checkout -`(the dash is a shortcut for the last commited branch)  or more specifically `git checkout [branch name]` will do the trick . However, if you made some changes to the file you are now looking at (which is not necessarily the most recent file on your branch, aka the master) which you want to keep, you need to specify that you want to commit this and make a new branch out of it using `git checkout -b [name of your new branch]`.

[Citation](https://howtogit.net/recipes/getting-out-of-detached-head-state.html)

### 5. Your boss has no idea what Git is or why you are using it. Explain the pros / cons of using Git for your research project. Explain the pros / cons of hosting your project in a public (or private) repository on Github/Bitbucket/Gitlab/etc.

Git is a good way to keep previous versions, and all the qualities mentionned in question 1. However, it takes a long time to learn and can be counter intuitive (as seen in question 3 and 4).

Github allows you to share information with collaborators and store information online. If your computer is compromised your data is still safe. However, its important to remember that the repositories can be accessed by strangers if the repository is not private and github doesnt store very large files. It also isnt great at storing large files. Other repository hosts can give you access to private repositories for free, but there may be limits on collaborators (ex. Gitlab). 


