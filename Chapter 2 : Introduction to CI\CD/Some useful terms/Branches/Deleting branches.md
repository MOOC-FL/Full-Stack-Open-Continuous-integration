#### Deleting branches
- Once you’ve finished working on a branch and have merged it into the main code base, you’re free to delete the branch without losing any history:
```git
1git branch -d crazy-experiment
```
However, if the branch hasn’t been merged, the above command will output an error message:
```git
1error: The branch 'crazy-experiment' is not fully merged. If you are sure you want to delete it, run 'git branch -D crazy-experiment'.
```
This protects you from losing access to that entire line of development. If you really want to delete the branch (e.g., it’s a failed experiment), you can use the capital `-D` flag:
```git
1git branch -D crazy-experiment
```
- [ ] This deletes the branch regardless of its status and without warnings, so use it judiciously.
- [ ] The previous commands will delete a local copy of a branch. The branch may still exist in remote repos. To delete a remote branch execute the following.
```git
1git push origin --delete crazy-experiment
```
or
```git
1git push origin :crazy-experiment
```
- This will push a delete signal to the remote origin repository that triggers a delete of the remote `crazy-experiment` branch.

