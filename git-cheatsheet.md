<pre>
Basic git commands
Alias(~/.gitconfig) https://github.com/GitAlias/gitalias
p.s. Head can always be replace with CommitHashId 
Info: status ; branch [-a] ; log [--oneline --graph] ; tag
Stage: add {fname} / . 
Commit: commit ; commit –m “my comment”
CommitAppend: commit --amend -m "my comment"
Checkout: checkout chash/bname (Moves HEAD) 
UnStage: reset {fnames}  /  reset (all)
UnCommit Move HEAD back: 
  Last commit destroy un/stage: reset --hard head~1
  Last commit no destroy stage: reset --soft head~1
  Last commit no destroy unstage: reset head~1
Rollback(Rewrite History) reset --hard {to-keep-hash}
Rollback Merge: 
a. git log to identify the keep-branch-position (kbp)
b. revert commit-hash -m kbp (1 or 2 or 3 ...) link 
Remote Rollback: push -f 
Stash: stash ; stash pop/list/drop/clear
Branch Add: branch {bname}
  Add and Checkout: checkout -b {bname}
Branch switch(move head to bname):checkout {bname}
Br. move(branch to head): checkout -B {bname} head
Branch Merge:
  step1: checkout bnameHM  (HEAD WILL Move)
  step2 : merge bnameD (decide step1 HEAD Dest)
    * fastforward: HM to top bnameD
    * 3-way merge: HM to the new generated commit
  step2 !shared: rebase bnameD (step1 HEAD Dest)
    1. clone new-commits(ncs) of bnameHM
    2. HM to top of ncs
    3. bottom of ncs points to bnameD
Branch Delete Local Step 1: branch –d {bname} 
Branch Delete Remote Step 2: push -d origin {bname}
Diff -stage +work:diff {fname} 
Diff -head +work: diff head {fname}
Diff -head +stage: diff --staged {fname}
Diff: diff {bname1}..{bname2} / {CommitId1}..{CommitId2}
Log range log <since>..<until>: e.g.
  HEAD~4..HEAD // shortcut -n 4
  branchA..branchB
log --since=1.month.ago --until=1.day.ago
reflog: history of branch/head commands
Info: remote -v ; branch -r ; remote show {bname}
Clone: clone {url} // -b {bname} specific branch
Add: remote add {rrepo} {url}
Ignore: create a file .gitignore github.com/github/gitignore
1st Push:: push -u origin {bname} //-u = --set-upstream
Push/Pull: push ; pull // i.e. fetch + merge {lbname}
Fetch: fetch // into lrepo lbname
Remote Branch Delete: git push origin --delete {bname}
Tag: tag -a vx.x.x.x -m "ver. comment" ; push --tags
Alias:config --global alias.s status
Color: config --global color.ui true
Rename: mv {sfname} {dfname}
File Del: rm {fname}
Diff Read: link 
Page Fwd/Bwd/Quit: f/b/q
VIM: ‘i’ ; [ESC] ; :x ; :q

Alias
a = add
b = branch
c = commit
discard = o --
d/dc/ds/dw = diff
f = fetch
g = grep
l/lk = log
m = merge
o = checkout
p = pull
publish = 1st Push
r = remote
s/ss/ssb = status
save/pop/stashes=stash save/pop/list
unstage/add=reset HEAD
w = whatchanged
</pre>
