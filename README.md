# github_test_session

### contents

This repositiory contains a simple python program to print a message. 


### Things required (desired by every repo.) 
- readme (a markdown explanation of what is going on and how to run)
- .gitignore (what files not to track or upload)
- Licence (usually something like MIT or related attribution lisenses are useful (can be none)
- Wiki (separate but useful for the documentation of large complex programs)



## Setting up (first time only)
```
git config --global user.name "Your Name"
git config --global user.email username@mit.edu

#save credentials after first time
git config credential.helper store

# set editor _ ctrl + x followed by an y or n to save changes
git config --global core.editor nano

#add some colour
git config --global color.branch auto
git config --global color.diff auto
git config --global color.interactive auto
git config --global color.status auto
git config --global color.grep auto
```




## Aims 

#### Basic
1. clone this repository and `cd` into it
2. create a new branch `git checkout -b <yourbranchnamehere>`
3. make some changes to different files in the sandbox folder (change `.` to your faviourite number)
4. commit your changes
5. push your changes 
6. create a pull request to update master (--force?)

#### Mistake
8. pull latest version
9. view changes using github.com
10. Make a big-bad change 
11. `git stash` the results, `stash list` and `stash drop`

#### Bigger Mistake
12. Make a big-bad change and commit this. 
13. Maybe even push this?
14. undo the last commit with `git reset --hard HEAD^` or the last two with `git reset --hard HEAD~2`
15. recommit and push 

----------------------------------------

#### Forking
1. Demo on repo creation
2. fork the reop into a personal account, clone the personal one and change directory into it. 
3. Make some improvements (be creative) - update the readme file

4. We know the main file has updated changes, so we wish to update our personal repo to match. 

```
git remote add upstream [original-repo-git-url]
git fetch upstream
git merge upstream/master
```
To remove remote branch `git remote remove upstream` will work. 


5. Fix the merge conflicts
```Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
```
Navigate to the file with the conflicts. This should have several indicators. 

You will see changes from YOUR head branch `<<<<<<HEAD` until `============`
and from the base branch `>>>>>>>> upstream/master`. Decide which changes you wish to keep, delete the others and remove the conflict markers and re add/commit your files. 


Note - if there are no conflicts the merge is seamless. 

6. commit and push to your own repo
7. push to the original repository using webinterface (create pull request)

### How a does a file change between commits 
Just replace github.com with github.githistory.xyz
https://github.githistory.xyz/scpyork/github_test_session/blob/master/README.md

### Issues and Todolists
See tab. 

### other problems 
- Try `git status`, it tends to tell you how to undo changes (eg `git merge --abort`  and then start again)
- the web interface
- google is your friend







