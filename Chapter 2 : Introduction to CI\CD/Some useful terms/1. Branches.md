#### Branches 
- `Git` allows multiple copies, `streams`, or `versions` of the code to co-exist without overwriting each other. When you first create a repository, you will be looking at the main branch (usually in `Git`, we call this `main` or `master`, but that does vary in older projects). This is fine if there's only one developer for a project and that developer only works on one feature at a time.
> Branches are useful when this environment becomes more complex. 
- [ ] Each branch is effectively a copy of the main branch with some changes that make it diverge from it.
- [ ] Once the feature or change in the branch is ready it can be merged back into the main branch, effectively making that feature or change part of the main software.
- [ ] In this way, each developer can work on their own set of changes and not affect any other developer until the changes are ready.
> But once one developer has merged their changes into the main branch, what happens to the other developers' branches? They are now diverging from an older copy of the main branch.
#####  How will the developer on the later branch know if their changes are compatible with the current state of the main branch? That is one of the fundamental questions we will be trying to answer in this part.
### Git Branch
- This document is an in-depth review of the `git branch` command and a discussion of the overall Git branching model. Branching is a feature available in most modern version control systems.
- Branching in other VCS's can be an expensive operation in both time and disk space. In Git, branches are a part of your everyday development process.
> **Git branches are effectively a pointer to a snapshot of your changes**
- When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes.
-  This makes it harder for unstable code to get merged into the main code base, and it gives you the chance to clean up your future's history before merging it into the main branch.
<img src="https://github.com/MOOC-FL/Media/blob/main/Full-Stack-Open-Continuous-integration/AT21KEQ.svg" alt=""></img>
- The diagram above visualizes a repository with two isolated lines of development,
- [ ]  one for a little feature,
- [ ] and one for a longer-running feature.
-  By developing them in branches, it’s not only possible to work on both of them in parallel, but it also keeps the main branch free from questionable code.
-  The implementation behind Git branches is much more lightweight than other version control system models.
1.  Instead of copying files from directory to directory,
2.   `Git` stores a branch as a `reference` to a commit.
3.   In this sense, a `branch` represents the **tip of a series of commits—it's** not a container for commits.
>  The history for a branch is extrapolated through the **commit relationships**.
- As you read, remember that Git branches aren't like SVN branches.Whereas SVN branches are only used to capture the occasional large-scale development effort
- Git branches are an integral part of your everyday workflow. The following content will expand on the internal Git branching architecture.
