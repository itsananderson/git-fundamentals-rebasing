title: "Git Fundamentals - Rebasing"
author:
  name: Will Anderson
  twitter: itsananderson
  url: http://willi.am
output: index.html

--

# Git Fundamentals
## Rebasing - keep your commit history clean

--

### Introduction

Rebasing is replaying history

Follow along:

http://willi.am/git-fundamentals-rebasing/

https://github.com/itsananderson/rebase-examples

--

### Why?

Consider a common example  
You are working on a feature branch...

<p style="text-align:center">
![](i-have-a-branch.png)
</p>

--

Now somebody does more work on the master branch

<p style="text-align:center">
![](master-has-changes.png)
</p>

--

You could merge changes from master with  
`git merge master`

<p style="text-align:center">
![](merge-master.png)
</p>

--

But then things get crazy if you do this several times when developing your feature

<p style="text-align:center">
![](merge-insanity.png)
</p>

--

### There is a better way 

<p style="text-align:center">
![](master-has-changes.png)
</p>

--

<p style="text-align:center">
`git rebase master`
</p>
<p style="text-align:center">
![](basic-rebase.png)
</p>

--

### Merge Conflicts

Sometimes a merge fails

<p style="text-align:center">
![](rebase-fail.png)
</p>

--

Check your status: `git status`

<p style="text-align:center">
![](rebase-status.png)
</p>

--

Resolve conflicts and `git rebase --continue`

<p style="text-align:center">
![](rebase-merge-complete.png)
</p>

--

### Modifying History

<p style="text-align:center">
What if we do not want C2, C3 *and* C4?
</p>

<p style="text-align:center">
![](master-has-changes.png)
</p>

--

<p style="text-align:center">
`git rebase -i master`
</p>

<p style="text-align:center">
![](interactive-rebase.png)
</p>
