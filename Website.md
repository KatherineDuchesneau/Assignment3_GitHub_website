# Github site by Katherine Duchesneau

## Questions from Jeff

### When should you use Git for a project?

Git is a great method to keep track of previous copies of a project. Everything that is commite will be kept using version control and it will always be possible to go back to previous versions. It helps keep track of what has been done. This can be particularly useful when working in a group since many people will be modifying the same files. Version control allows you to keep copies of previous files, assign changes to particular collaborators, and keeps tract of program versions and results at each step. If the work is left for a long time and the exact details are forgotten, records of of the previous work are easily accessible accessible. Additionally, conflicting changes made by two collaborators can be intergrate together! All of this makes git great for any project between collaborators who want to keep track of their code for stats, programming, or even copies of their writing kept in .txt format.

### What kind of files/info should be saved in a Git repository? What types of files/info should not be included in a Git repo?



### What are the commands to undo a commit?

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


### One of your repositories is in a “detached HEAD” state. How do you fix this?


### Your boss has no idea what Git is or why you are using it. Explain the pros / cons of using Git for your research project. Explain the pros / cons of hosting your project in a public (or private) repository on Github/Bitbucket/Gitlab/etc.

