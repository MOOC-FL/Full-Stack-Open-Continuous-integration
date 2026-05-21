#### Creating branches
- It's important to understand that branches are just pointers to commits. When you create a branch, all Git needs to do is create a new pointer, it doesn’t change the repository in any other way. If you start with a repository that looks like this:
<img src="https://github.com/MOOC-FL/Media/blob/main/Full-Stack-Open-Continuous-integration/AT21KER.svg" alt=""></img>
- Then, you create a branch using the following command:
```git
git branch crazy-experiment
```
- The repository history remains unchanged. All you get is a new pointer to the current commit:
<img src="https://github.com/MOOC-FL/Media/blob/main/Full-Stack-Open-Continuous-integration/AT21KES.svg" alt=""></img>
- Note that this only **creates** the new branch. To start adding commits to it, you need to select it with `git checkout`, and then use the standard `git add` and `git commit` commands. 

#### Creating remote branches
- So far these examples have all demonstrated local branch operations. The `git branch` command also works on remote branches. In order to operate on remote branches, a remote repo must first be configured and added to the **local repo config**.
```git
1$ git remote add new-remote-repo https://bitbucket.com/user/repo.git
2# Add remote repo to local repo config
3$ git push <new-remote-repo> crazy-experiment~
4# pushes the crazy-experiment branch to new-remote-repo
```
This command will push a copy of the local branch `crazy-experiment` to the remote repo `＜remote＞`.



