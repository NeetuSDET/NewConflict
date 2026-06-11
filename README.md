# NewConflict

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git init
Initialized empty Git repository in /Users/rajnishkhatri/Desktop/NewConflict/.git/
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git add .
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git commit -m "commit1"
[main (root-commit) f5f4ea5] commit1
 1 file changed, 1 insertion(+)
 create mode 100644 a.txt
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git checkout -b Reena
Switched to a new branch 'Reena'
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git branch
* Reena
  main
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git add .
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git commit -m "commit2"
[Reena 7481e1d] commit2
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git checkout -b master
Switched to a new branch 'master'
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git checked main
git: 'checked' is not a git command. See 'git --help'.

The most similar command is
        checkout
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git checkout main
Switched to branch 'main'
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git checkout -b john
Switched to a new branch 'john'
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git add .
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git commit -m "commit3"
[john e4ebb5d] commit3
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git checkout main
Switched to branch 'main'
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git merge Reena
Updating f5f4ea5..7481e1d
Fast-forward
 a.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git merge john
Auto-merging a.txt
CONFLICT (content): Merge conflict in a.txt
Automatic merge failed; fix conflicts and then commit the result.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git add .
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git commit -m "commit4"
[main 13df8e2] commit4
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git remote add origin git@github.com:NeetuSDET/NewConflict.git
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git push -u origin master
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (6/6), 452 bytes | 452.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/NeetuSDET/NewConflict/pull/new/master
remote: 
To github.com:NeetuSDET/NewConflict.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git push -u origin main
To github.com:NeetuSDET/NewConflict.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:NeetuSDET/NewConflict.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git status
On branch main
nothing to commit, working tree clean
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git branch
  Reena
  john
* main
  master
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git remote add origin git@github.com:NeetuSDET/NewConflict.git
error: remote origin already exists.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git push -u origin main
To github.com:NeetuSDET/NewConflict.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:NeetuSDET/NewConflict.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main

(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull origin main
From github.com:NeetuSDET/NewConflict
 * branch            main       -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull --no-rebase origin main
From github.com:NeetuSDET/NewConflict
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull origin main
From github.com:NeetuSDET/NewConflict
 * branch            main       -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull origin main --allow-unrelated-histories
From github.com:NeetuSDET/NewConflict
 * branch            main       -> FETCH_HEAD
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git config pull.rebase false
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull origin main --allow--allow-unrelated-histories
error: unknown option `allow--allow-unrelated-histories'
usage: git pull [<options>] [<repository> [<refspec>...]]

    -v, --[no-]verbose    be more verbose
    -q, --[no-]quiet      be more quiet
    --[no-]progress       force progress reporting
    --[no-]recurse-submodules[=<on-demand>]
                          control for recursive fetching of submodules

Options related to merging
    -r, --[no-]rebase[=(false|true|merges|interactive)]
                          incorporate changes by rebasing rather than merging
    -n                    do not show a diffstat at the end of the merge
    --[no-]stat           show a diffstat at the end of the merge
    --[no-]log[=<n>]      add (at most <n>) entries from shortlog to merge commit message
    --[no-]signoff[=...]  add a Signed-off-by trailer
    --[no-]squash         create a single commit instead of doing a merge
    --[no-]commit         perform a commit if the merge succeeds (default)
    --[no-]edit           edit message before committing
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    --[no-]ff             allow fast-forward
    --ff-only             abort if fast-forward is not possible
    --[no-]verify         control use of pre-merge-commit and commit-msg hooks
    --[no-]verify-signatures
                          verify that the named commit has a valid GPG signature
    --[no-]autostash      automatically stash/stash pop before and after
    -s, --[no-]strategy <strategy>
                          merge strategy to use
    -X, --[no-]strategy-option <option=value>
                          option for selected merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit
    --[no-]allow-unrelated-histories
                          allow merging unrelated histories

Options related to fetching
    --[no-]all            fetch from all remotes
    -a, --[no-]append     append to .git/FETCH_HEAD instead of overwriting
    --[no-]upload-pack <path>
                          path to upload pack on remote end
    -f, --[no-]force      force overwrite of local branch
    -t, --[no-]tags       fetch all tags and associated objects
    -p, --[no-]prune      prune remote-tracking branches no longer on remote
    -j, --[no-]jobs[=<n>] number of submodules pulled in parallel
    --[no-]dry-run        dry run
    -k, --[no-]keep       keep downloaded pack
    --[no-]depth <depth>  deepen history of shallow clone
    --[no-]shallow-since <time>
                          deepen history of shallow repository based on time
    --[no-]shallow-exclude <ref>
                          deepen history of shallow clone, excluding ref
    --[no-]deepen <n>     deepen history of shallow clone
    --unshallow           convert to a complete repository
    --[no-]update-shallow accept refs that update .git/shallow
    --refmap <refmap>     specify fetch refmap
    -o, --[no-]server-option <server-specific>
                          option to transmit
    -4, --[no-]ipv4       use IPv4 addresses only
    -6, --[no-]ipv6       use IPv6 addresses only
    --[no-]negotiation-tip <revision>
                          report that we have only objects reachable from this object
    --[no-]show-forced-updates
                          check for forced-updates on all updated branches
    --[no-]set-upstream   set upstream for git pull/fetch

(base) rajnishatrismbp:NewConflict rajnishkhatri$ git pull origin main --allow-unrelated-histories
From github.com:NeetuSDET/NewConflict
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
(base) rajnishatrismbp:NewConflict rajnishkhatri$ git push origin main
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (8/8), 816 bytes | 816.00 KiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:NeetuSDET/NewConflict.git
   03e4d13..a853a3b  main -> main
(base) rajnishatrismbp:NewConflict rajnishkhatri$

tq
