## FORKS AND BRANCHES

**Forking**

Forking is used more with the intention of cloning a repository to use as a new source. In conclusion, you have no intention of merging it back with the original.

<p align="center">
<img src="https://i.stack.imgur.com/yPKXU.png" alt="isolated" width="400" />
</p>

**Branching**

Branches are most commonly used as codebase build zones, with the intention of merging them back into the source and once merged, deleting that branch.

**Associated costs**

When you merge a branch, github just has to compare the different work you've done on the branch.
Instead, when you want to merge a fork to the origin, github has to compare two entire projects.

**Forking is also operationally more expensive**

Working with forks gives less visibility to the code, since as each developer has their individual repository, it is not possible to work together comfortably.
For this reason branches are used when collaborating, in this way a person will be able to visualize all the changes that have been made in the code.

**TL;DR**

A branch-centric workflow makes sense for most business settings.

**High-level differences**

*Forking*

| Pros | Cons |
| ------------- | ------------- |
| Keeps branches separated by user  | Makes it more difficult to see all of the branches that are active (or inactive, for that matter)  |
| Reduces clutter in the primary repository  | Collaborating on a branch is trickier (the fork owner needs to add the person as a collaborator)  |
| Your team process reflects the external contributor process | Multiple remotes in Git requires additional mental bookkeeping. This will make the workflow more difficult for people who aren't super comfortable with Git |

*Branching*

| Pros | Cons |
| ------------- | ------------- |
| Keeps all of the work being done around a project in one place  | Branches that get abandoned can pile up more easily  |
| All collaborators can push to the same branch to collaborate on it  | Your team contribution process doesn't match the external contributor process  |
| There's only one Git remote to deal with  | You need to add team members as contributors before they can branch  |
